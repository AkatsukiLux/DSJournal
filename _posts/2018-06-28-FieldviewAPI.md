---
layout: post
title: "Connecting to the Fieldview API: A Practical Guide"
date: 2018-06-28
categories: [api, tutorial]
tags: [fieldview, api, construction, soap, postman]
---

To address the lack of guidance that exists around the Fieldview Application Programming Interface (API), I thought I'd write up an article on how to connect and use it for loading the task lists from Fieldview. I imagine many in the construction sector using this application have experienced the horrific nature of trying to locate any information that is captured on the system. Hopefully this can end now.

## Understanding APIs

First things first, an API can be thought of as a group of functions that allows one application to interact with another. There are various ways in which one application can transfer information in order to interact with an API. The most common way is through the Hypertext Transfer Protocol (HTTP). We all commonly see part of this acronym when going onto any website (It's within that top bar of your web browser). This protocol is a standard for transferring data through Request-response methods. Using a website as an example, your web browser application makes a request with a defined method, along with a URL and a payload (like a form or query string request) which communicate to the server what action they want performed.

Phew so nearly finished with all the explainy bits and getting closer to the 'copy and paste this stuff' bit! Which is where it gets exciting!

## Using Postman

The way I recommend using and testing an API and how I will show what to be done in this post will be through the use of a Chrome app called Postman.

![Screen grab of Postman](https://atsutob.github.io/DSJournal/assets/photos/PostmanStart.png)

----
![Screen grab of Postman](https://atsutob.github.io/DSJournal/assets/photos/intro.svg)
<img src="https://atsutob.github.io/DSJournal/assets/photos/intro.svg">

----
<object data="https://atsutob.github.io/DSJournal/assets/photos/intro.svg" type="image/svg+xml"></object>

## Getting Project Task Lists

We will be calling 2 different API functions in order to get the correct information to call the `GetProjectTasksList()` function which, as the name implies, gets a list of tasks from a particular project.

The functions you first need to call are the [GetProjectTaskTypes()](https://fvdocs.viewpoint.com/Admin_web_topics/APIs/tasks_services/r_GetProjectTaskTypes.html) and [GetProjectDetails()](https://fvdocs.viewpoint.com/Admin_web_topics/APIs/project_services/r_GetProjectDetails.html)

### Getting Project Details

Endpoint: `https://www.priority1.uk.net/FieldViewWebServices/WebServices/JSON/API_ProjectServices.asmx`

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetProjectDetails xmlns="https://localhost.priority1.uk.net/Priority1WebServices/JSON">
      <apiToken>ADD_API_TOKEN_HERE</apiToken>
      <startRow>1</startRow>
      <pageSize>500</pageSize>
    </GetProjectDetails>
  </soap:Body>
</soap:Envelope>
```

> **Security Warning**: Never commit your actual API token to version control. Always use environment variables or secure credential storage.

### Getting Project Tasks List

POST request to: `https://www.priority1.uk.net/FieldViewWebServices/WebServices/JSON/API_TasksServices.asmx`

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetProjectTasksList xmlns="https://localhost.priority1.uk.net/Priority1WebServices/JSON">
        <apiToken>Add_API_Token_Here</apiToken>
        <projectId>Add_Project_ID_Here</projectId>
        <taskTypeLinkIds>ADD_Task_Type_Link_ID_Here</taskTypeLinkIds>
        <createdDateFrom>2018-06-28-02:00</createdDateFrom>
        <createdDateTo>2018-06-29-01:00</createdDateTo>
    </GetProjectTasksList>
  </soap:Body>
</soap:Envelope>
```

## Next Steps

With these API calls, you can start pulling task data from Fieldview and integrating it with your own reporting and analysis tools. In future posts, I'll cover how to process this data and build dashboards for better project visibility.
