---
title: Exmaple post
date: 2023-08-01 22:44:00 +0100
categories: [Intune, Logic Apps, PowerShell]
tags: [Intune, Logic Apps, PowerShell]
---

*App Request* is a solution to allow end users to request applications that require some form of approval, directly from Company Portal.

As we know there is no native request feature with Company Portal, so while we wait and hope Microsoft will add this capability, this solution allows a user to use the Company Portal as the single app portal to easily find, request and install apps.

## Overview
For an app that requires some from of approval, for example requires a license, you create a *request* Win32 app and an *install* Win32 app. The *request* app allows the user to request the app and the *install* app is the actual app installation.

The *request* app is deployed to all users to allow them to request the app. When the user installs the *request* app via Company Portal, they are prompted to enter a justification and submit the request. This will start an Azure Logic App that will perform the request workflow.
Once the request has been approved, the user is added to an Azure AD group which deploys the *install* app 

 and deploy it to all users. Users install this app from Company Portal which prompts the user to request the associated app.

To use this solution you need to use the contents of the **Win32App** folder to create a Win32 app that prompts 


# 
