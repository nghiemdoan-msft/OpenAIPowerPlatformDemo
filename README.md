# OpenAI and Power Platform Demo

## Summary
This is a demo app to show how we can connect and use OpenAI API and Azure OpenAPI inside Power Platform.

## Features
This solution includes OpenAI API Connector, Azure OpenAI API Connector and Canvas App to show how to use these connectors.

**OpenAI Custom Connector**:
* Create Completion https://platform.openai.com/docs/api-reference/completions 
* Create Image https://platform.openai.com/docs/api-reference/images/create  

**Azure OpenAI Custom Connector**:
* Azure OpenAI Service REST API reference https://learn.microsoft.com/en-us/azure/cognitive-services/openai/reference 

**Canvas Apps**:

OpenAI Email Screen
* Using Completion API (Link) to improve email composition: 
    - Rewrite an email input or create a draft response for an Email’s input in a pre-desired format. 
    - Summarize or extract key points from an Email

OpenAI Images Screen
* Using Create Image API (Link) to generate new image(s) based on an input image.

Azure openAI Email Screen (only in **OpenAI Intergration with Power Apps V2**)
* Introduce how to replace the OpenAI powered Email Screen with Azure OpenAI service (if you do not have access to Azure Open API, you can just use the )

## Prerequisite
* Sign up for an OpenAI API https://platform.openai.com/overview 
* Sign up for Azure Open API https://oai.azure.com/portal 
* Power Platform Environment. You can get Developer license here. https://powerapps.microsoft.com/en-us/developerplan/  

## Demo
[![OpenAI and Power Platform Integration Demo App Video](https://i.ytimg.com/vi/uUj6Xjx7SSo/maxresdefault.jpg)](https://youtu.be/uUj6Xjx7SSo)

Note: If you want to learn how to create OpenAI API Custom Connector from scratch, please check out Reza Dorrani's video 
https://youtu.be/mzZLkf8pz9U

## Demo Screens
Write a draft email
![Write a draft email](/images/1-Completion-ReplyEmail.png)

Extract key points from an email
![Extract key points from an email](/images/2-ExtractKeyPoints.png)

Create a logo idea for a business
![Create a logo idea for a business](/images/3-CreateImages.png)


## Install solutions
You can find both Managed and Unmanaged solutions in Resouces folder.
Once install, create Connection for below Connectors: 

For OpenAI Custom Connector, create connection and give the API key as: Bearer {OpenAI API Key}.

For Azure OpenAI Custom Connector:
* Edit the Connector:
    - Option 1: Update with your Resource Group in the Url Template of the Policy "Set host URL" on he Definition tab
![Update Policy URL template](/images/5-UpdateHostURLPolicy.png)
    - Option 2: Edit the Host on the General Tab, you can delete the Policy "Set host URL" on he Definition tab
![Update Host URL](/images/4-UpdateHostURL.png)
* Authenticate with your Secret key from Azure OpenAI resource.

I will continue to build and add more features to this solution to show how we can leverage this in Power Automate, Power Virtual Agent and so more!