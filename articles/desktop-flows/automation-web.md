---
title: Automation in the web | Microsoft Docs
description: Automation in the web
author: mariosleon
ms.service: power-automate
ms.subservice: desktop-flow
ms.topic: article
ms.date: 09/22/2020
ms.author: marleon
ms.reviewer: 
search.app: 
  - Flow
search.audienceType: 
  - flowmaker
  - enduser
---
# Automate web flows



The flow designer includes a number of actions under the **Browser automation** category, each of them corresponding to an interaction between a user and a web browser.

Four web browsers are currently supported:

* Internet Explorer
* A chromium-based version of Edge
* Firefox
* Chrome

Browser automation is achieved by launching, or attaching to, one of the aforementioned browsers, then performing browser automation actions on them. Development may be performed manually, or through the use of the web recorder.

## Building a browser automation flow

To begin a browser automation flow, use one of the Launch web browser actions (**Launch new Internet Explorer**, **Launch new Edge**, **Launch new Firefox**, or **Launch new Chrome**) to start a new browser session, or attach to an already existing one:

![Launch web browser.](.\media\web-automation\launch-web-browser-action.png)

> [!NOTE]
> Some browsers may require configuration before they can be used in Power Automate. Refer to the [relevant article](using-browsers.md) for more information.

After the browser session is stored in a variable, add other browser automation actions to interact with the browser's content. The **Web form filling** action group focuses on providing input to web pages, while **Web data extraction** actions draw data from web pages, to be used in the flow.

Most browser automation actions require a browser instance as input, as well as a web element with which to interact:

![Web action inputs.](.\media\web-automation\web-action-inputs.png)

Existing web elements may be added from the repository, while new ones may also be added directly from the action's properties:

![Adding new elements through a web action.](.\media\web-automation\adding-new-elements-through-a-web-action.png)

To add a new element, highlight it and press **Ctrl & left-click**:

![Capturing new elements.](.\media\web-automation\capturing-new-elements.png)

After adding all the required elements, select **Done** to save them to the repository.

## Data population on the web

To provide input to a web page, select the appropriate **Web form filling** action depending on the nature of the element to interact with, and specify the browser instance:

![Set drop down list value on web page action.](.\media\web-automation\set-drop-down-list-value-on-web-page-action.png)

![Populate text field on web page action.](.\media\web-automation\populate-text-field-on-web-page-action.png)

## Web data extraction

To extract a piece of data from a web page, use the appropriate action, depending on whether the data in question concerns the entire web page, or an element inside it:

![Get details of web page action.](.\media\web-automation\get-details-of-web-page-action.png)

![Get details of element on web page action.](.\media\web-automation\get-details-of-element-on-web-page-action.png)

To extract larger amounts of data, use the **Extract data from web page** action, then right-click on the required data on the web page to view the available options:

![Extracting data from web page.](.\media\web-automation\extracting-data-from-web-page.png)

 Note that any lists or tables of data will be automatically identified after two of their elements are designated for extraction:

![Extracting data table from web page.](.\media\web-automation\extracting-data-table-from-web-page.png)


You'll find the list of browser automation actions available in the [Actions reference](actions-reference/webautomation.md).


## Interacting with the web and web services

It is possible to communicate directly with web resources, such as web pages, files, and APIs, without using a web browser.

## Downloading web resources

Use the **Download from web** action to directly download web page content, or files on the web:

![The Download from web action.](./media/interacting-web-services/download-from-web-action.png)

Both the **GET** and **POST** methods may be used with this action; files can be downloaded directly to the disk, while web page contents are saved into a variable.

## Accessing web APIs

Use the **Invoke web service** action to access web APIs:

![The Invoke web service action.](./media/interacting-web-services/invoke-web-service-action.png)

A variety of methods are compatible with this action, which is fully customizable in order to accommodate virtually any API.


You'll find the list of web related actions available in the [Actions reference](actions-reference/web.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]