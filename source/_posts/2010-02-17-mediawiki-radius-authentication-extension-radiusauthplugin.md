---
layout: post
title: "MediaWiki Radius Authentication Extension - RadiusAuthPlugin"
date: 2010-02-17 22:12
comments: true
categories: mediawiki radius
---

Here is an extension/plugin for MediaWiki to authenticate against a Radius
server.  I couldn’t find one anywhere else, which is surprising. I can’t believe 
I am the first person to want to do this. Anyway, this is just bare bones, but
it works for an internal MediaWiki setup.

<!--more-->

First, get Pure PHP radius class 1.2.2 from [http://developer.sysco.ch/php][0].
This does the actual radius authentication.  Put `radius.class.php` in
`wiki/extensions/` (assuming wiki is your mediawiki install).  There is probably
a better place to put it, but I was setting this up for internal use and wanted
to get it working quickly.

Next, create `wiki/extensions/RadiusAuthPlugin.php`. Make sure you fill in
`RADIUS_SERVER`, `SHARED_SECRET`, and `NAS_IP_ADDRESS` with your actual
information.

{% codeblock RadiusAuthPlugin.php %}
<?php
require_once('AuthPlugin.php');
require_once('radius.class.php');

error_reporting(E_ALL);

class RadiusAuthPlugin extends AuthPlugin
{
    function userExists($username)
    {
        return TRUE;
    }



    function authenticate($username, $password)
    {
        $username = strtolower($username);

        $radius = new Radius('RADIUS_SERVER', 'SHARED_SECRET');
        $radius->SetNasIpAddress('NAS_IP_ADDRESS'); // Needed for some devices (not always auto-detected)
        if ($radius->AccessRequest($username, $password))
        {
            return TRUE;
        }

        return FALSE;
    }



    function modifyUITemplate(&$template)
    {
        $template->set('usedomain', FALSE);
        $template->set('useemail', FALSE);
        $template->set('create', FALSE);
    }



    function autoCreate()
    {
        return TRUE;
    }



    function validDomain($domain)
    {
        return TRUE;
    }



    function updateUser(&$user)
    {
        return TRUE;
    }



    function allowPasswordChange()
    {
        return FALSE;
    }



    function setPassword($password)
    {
        return FALSE;
    }



    function updateExternalDB($user)
    {
        return FALSE;
    }


    function canCreateAccounts()
    {
        return FALSE;
    }


    function adduser($user, $password)
    {
        return FALSE;
    }



    function strict()
    {
        return TRUE;
    }



    function initUser(&$user) { }
}


$wgExtensionCredits['other'][] = array(
    'name' => 'RadiusAuthPlugin',
    'version' => '1.0.0',
    'author' => 'James Young',
    'description' => 'Automatic login with a RADIUS server'
);
{% endcodeblock %}

Lastly, put this in your `LocalSetup.php`:

{% codeblock LocalSetup.php %}
require_once("./extensions/RadiusAuthPlugin.php");
$wgAuth = new RadiusAuthPlugin();
$wgGroupPermissions['*']['createaccount'] = false;
{% endcodeblock %}



[0]: http://developer.sysco.ch/php
