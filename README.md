# COVID-19 CHATBOT

This chatbot is an Indian extension for the Chatbot created under COVID Crisis Communication Starter Kit as mentioned downwards.

## The chatbot provides the user with following features-

1.  Necessary information about the virus, how it can spread, and the appropriate preventive measures.
2.  Timely updated COVID 19 cases with the death figure, recovery figure and the active figure of the cases on three levels   
    a. WorldWide(Cases in the world as well as different countries)
    b. NationWIde in India (Cases in various states of India)
    c. State Wise for states of India ( Cases in the districts of India)
3.  Information regarding segregated Zonal and state-level information of various resources complementing the people fight       the    COVID and their contact details along with what services they provide. (Updated daily) These resources include-
    a. Hospitals that are nearby treating various ailments.
    b. Testing facilities set up by the ICMR(Indian Council of Medical Research) and various state and central governments.
    c. Police services.
    d. Contacts to Free food services and Community Kitchens funded by governments and various private/social bodies.
    e. Government Helplines details.
    f. Various NGOs and fundraisers information.Information on the efforts made by the government for the social and mental          well     being of the citizens.
4.  Testing details updated daily on how many testings have been done in a specific country up to date. (Updated as per the       records provided by the government).
5.  We also provide the user with the feature to search the Top N[1-50] affected Countries (sorted by the number of cases) by     the COVID19 as well as Top N(1-25) affected States or Union Territories in India along with the details of incidents in       them.
6.  The chatbot gives access to the people to search for various COVID19 related terminologies such as social distancing and     comorbidity.
7.  The chatbot is capable of answering basic communicating questions such as hello, bye, I am bored, and more.
8.  We provide a unique and interactive way of representing the information.
9.  The chatbot answers queries regarding the effect on various age groups in society.
10. It also queries regarding the importance of preventive measures and how the virus is transmitted.
11. It also addresses the people queries regarding the go-to terms in India, such as aatmnirbhar.
12. If any information is not present, uses IBM discovery to fetch related news articles regarding the query asked by the         user.
13. It also answers queries regarding its name and info about its creator.
14. Respond by sharing consistent, accurate COVID-19 information.
15. Dynamically update information with the latest developments and recommendations.

## Preview Link -
- LINK( https://web-chat.global.assistant.watson.cloud.ibm.com/preview.html?region=eu-gb&integrationID=e319bc77-1902-4b54-8ec1-8a1bccb9f4c8&serviceInstanceID=d7840b8d-807d-4606-9e56-15cb66afe6ba )

## Overview

### What's the problem?
In times of crisis, communications systems are often overwhelmed with people trying to find basic information about testing, symptoms, community response, and other resources. When communication lines get clogged, people who need real help can't get through. Chatbots help respond to tens, even hundreds, of thousands of messages a day.
In India the problem is much deeper as due to the geopolitical and polulation density of the country.

### How can technology help ?

Whether via text, phone, websites, or communication apps, conversing with chatbots and other AI-enabled resources can play a critical role in helping communities quickly understand crucial information and free up customer service resources to focus on higher-level issues.

IBM Watson Assistant service helps you build, train, and deploy conversational interactions into any application, device, or channel. Creating a chatbot using Watson Assistant can help address the issues that our users face while trying to gather accurate, relevant information. Whether you're trying to learn the latest news about Covid-19 or learn where there's testing in your area, a chatbot can play a major role in helping communities quickly understand crucial information and free up customer service resources to focus on higher-level issues.


## The idea

COVID-19 has citizens looking for answers about symptoms and testing sites as well as current status of schools, transportation, and other public services. Using Watson Assistant, this Call for Code Starter Kit has designed a virtual assistant pre-loaded to understand and respond to common questions about COVID-19, scan COVID-19 news articles using Watson Discovery and respond to COVID statistics inquires with data from trusted sources.

With this Watson Assistant powered Crisis Communications Starter Kit you can integrate a chatbot into your Call for Code solution in an IBM Cloud hosted web server, using a Slack integration or via a Node-RED Dashboard. 

## How it works


## Diagrams

### Website integration with COVID-19 crisis communication chatbot

![Crisis Comms Architecture diagram](/images/Crisis-Comms-Architecture-Nodejs-WebServer.png)

1. User visits a website with the COVID-19 chatbot and asks a question.
2. Node.js web server calls the Watson Assistant service hosted in IBM Cloud.
3. Watson Assistant uses natural language understanding and machine learning to extract entities and intents of the user question.
4. Source COVID-19 FAQ information from trusted CDC data.
5. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
6. IBM Cloud Function calls the Watson Discovery service running in IBM Cloud.
7. Watson Discovery scans news articles and responds with relevant articles.
8. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
9. IBM Cloud Function calls the COVID-19 API to get statistics.
10. Watson Assistant replies to the user inquiry.
11. Node.js web server displays the chat answer to the user.

### Slack integration with COVID-19 crisis communication chatbot

![Crisis Comms Architecture diagram](/images/Crisis-Comms-Architecture-Slack-Integration.png)

1. User invokes a COVID-19 Slack integration chatbot app and asks a question.
2. Slack app calls the Watson Assistant service hosted in IBM Cloud.
3. Watson Assistant uses natural language understanding and machine learning to extract entities and intents of the user question.
4. Source COVID-19 FAQ information from trusted CDC data
5. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
6. IBM Cloud Function calls the Watson Discovery service running in IBM Cloud.
7. Watson Discovery scans news articles and responds with relevant articles.
8. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
9. IBM Cloud Function calls the COVID-19 API to get statistics.
10. Watson Assistant replies to the Slack application.
11. Slack app displays the chat answer to the user.

### Voice enabled COVID-19 crisis communication chatbot using Node-RED

![Crisis Comms Architecture diagram](/images/Crisis-Comms-Architecture-Node-RED.png)

1. User visits a voice-enabled Node-RED website with the COVID-19 chatbot and asks a question.
2. Node-RED records the speech wav file and calls the Watson Speech to Text service hosted in IBM Cloud.
3. Watson Speech to Text uses machine learning to decode the user's speech.
4. Watson Speech to Text replies with a transcript of the COVID-19 question and Node-RED calls Watson Assistant service hosted in IBM Cloud.
5. Watson Assistant uses natural language understanding and machine learning to extract entities and intents of the user's question.
6. Source COVID-19 FAQ information from trusted CDC data
7. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
8. IBM Cloud Function calls the Watson Discovery service running in IBM Cloud.
9. Watson Discovery scans news articles and responds with relevant articles.
10. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
11. IBM Cloud Function calls the COVID-19 API to get statistics.
12. Watson Assistant replies to the user inquiry and Node-RED sends the text transcript to Watson Text to Speech.
13. Watson Text to Speech encodes the message in the user's language.
14. Node-RED plays the chat answer wav file to the user.
15. User listens to the chat answer.

## Documents

### Tutorials and documentation:

- [How-to guides for chatbots](https://www.ibm.com/watson/how-to-build-a-chatbot)
- [Learning path: Getting started with Watson Assistant](https://developer.ibm.com/series/learning-path-watson-assistant/)
- [Chatbot with Watson Discovery](https://github.com/IBM/watson-discovery-sdu-with-assistant)
- [Chat Bot Slack Deployment](https://cloud.ibm.com/docs/assistant?topic=assistant-deploy-slack)
- [Node-RED Slack Integration](https://www.ibm.com/cloud/blog/create-a-chatbot-on-ibm-cloud-and-integrate-with-slack-part-1)
- [Train a speech-to-text model](https://developer.ibm.com/patterns/customize-and-continuously-train-your-own-watson-speech-service/)
- [Making Programmatic Calls from Watson Assistant](https://cloud.ibm.com/docs/assistant?topic=assistant-dialog-webhooks)
- [IBM Cloud Voice Agent with Twilio](https://developer.ibm.com/recipes/tutorials/ibms-voice-agent-with-watson-and-twilio/)
- [Watson Assistant](https://cloud.ibm.com/docs/assistant?topic=assistant-getting-started)

## Datasets

- [covid19api](https://covid19api.com/)

## Technology

### IBM technology

- [IBM Watson Assistant](https://www.ibm.com/cloud/watson-assistant/)
- [Watson Discovery](https://www.ibm.com/cloud/watson-discovery)
- [Watson Speech to Text](https://www.ibm.com/cloud/watson-speech-to-text)
- [Watson Text to Speech](https://www.ibm.com/cloud/watson-text-to-speech)
- [IBM Cloud Functions](https://cloud.ibm.com/functions/)

### Open source technology

- [Node.js](https://nodejs.org/en/)
- [Apache OpenWhisk](https://openwhisk.apache.org/)
- [Node-RED](https://nodered.org/)

## Getting started

### Prerequisite

- Register for an [IBM Cloud](https://www.ibm.com/account/reg/us-en/signup?formid=urx-42793&eventid=cfc-2020?cm_mmc=OSocial_Blog-_-Audience+Developer_Developer+Conversation-_-WW_WW-_-cfc-2020-ghub-starterkit-communication_ov75914&cm_mmca1=000039JL&cm_mmca2=10008917) account.

### Set up an instance of Watson Assistant

Log in to IBM Cloud and provision a Watson Assistant instance.

**Step 1.** From the [IBM Cloud catalog](https://cloud.ibm.com/catalog/services/watson-assistant), provision an an instance of **Watson Assistant**.
  ![Watson Assistant Catalog](/starter-kit/assistant/WA-Photo1.png)

**Step 2.**  Launch the Watson Assistant service.

**Step 3.** Click **Create assistant** and follow [these detailed instructions](https://cloud.ibm.com/docs/assistant?topic=assistant-assistant-add) for how to create an assistant.
  ![Watson Assistant Photo2 ](/starter-kit/assistant/WA-Photo2.png)

**Step 4.** Name the Watson Assistant instance **COVID Crisis Communication**
  ![Watson Assistant Photo3 ](/starter-kit/assistant/WA-Photo3.png)

**Step 5.** Click **Add Dialog skill** to add this to your assistant. Follow [the documentation](https://cloud.ibm.com/docs/assistant?topic=assistant-skill-dialog-add) if you have questions.
  ![Watson Assistant Photo4 ](/starter-kit/assistant/WA-Photo4.png)

**Step 6.** Click **Import skill > Choose JSON file** and import the [`skill-CDC-COVID-FAQ.json`](./starter-kit/assistant/skill-CDC-COVID-FAQ.json) file.
  ![Watson Assistant Photo5 ](/starter-kit/assistant/WA-Photo5.png)

**Step 7.** Go back to the All Assistants page. From the action menu ( **`⋮`** ), open **Settings**.
  ![Watson Assistant Photo6 ](/starter-kit/assistant/WA-Photo6.png)

**Step 8.**  On the Settings tab, click **API Details** on the left and make a note of the `Assistant ID` and `Api Key` for future use.
  ![Watson Assistant Photo7 ](/starter-kit/assistant/WA-Photo7.png)

**Step 9.** Go back to the All Assistants page and click on the **Skills** link.
  ![Watson Assistant Skills ](/starter-kit/assistant/WA-Skills.png)

**Step 10.** On the Skill page, click on the action menu ( **`⋮`** ), open **View API Details**.
  ![Watson Assistant Skill Properties](/starter-kit/assistant/WA-SkillAPIProperties.png)

**Step 11.** On the Skill Details page, make note of the `Skill ID` for future use.
  ![Watson Assistant Skill Details](/starter-kit/assistant/WA-SkillDetails.png)

**Step 12.**  Go back to your dialog skill and click on the **Preview Link** button on the side to get a link to test and verify your assistant.
  ![Watson Assistant Photo9 ](/starter-kit/assistant/WA-Photo91.png)

**Step 13.** Ask the Watson Assistant chatbot some questions about COVID-19.
<p align="center">
<img width="50%" height="50%" src="https://raw.githubusercontent.com/Call-for-Code/Solution-Starter-Kit-Communication-2020/master/starter-kit/assistant/WA-Photo101.png">
</p>


### Connect your chatbot to data sources via a webhook

Now that you’ve created your Watson Assistant-enabled chatbot, you need to connect it to a data source. With Watson Assistant, you need to do this via a webhook.

A webhook is a mechanism that allows you to call out to an external program based on something happening in your program. When used in a dialog skill, a webhook is triggered when the assistant processes a node that has a webhook enabled. The webhook collects data that you specify or that you collect from the user during the conversation and save in context variables. It sends the data as part of a HTTP POST request to the URL that you specify as part of your webhook definition. The URL that receives the webhook is the listener. It performs a predefined action using the information that you pass to it as specified in the webhook definition, and can optionally return a response.

[Follow these instructions for setting up webhook](./starter-kit/webhook/README.md) with the Watson Assistant chatbot you just provisioned.

### Integrate your COVID-19 chatbot with Slack

Now that you have a functioning Watson Assistant, let's deploy it to Slack. Slack is a cloud-based messaging application that helps people collaborate with one another. After you configure a dialog skill and add it to an assistant, you can integrate the assistant with Slack.

When integrated, depending on the events that you configure the assistant to support, your assistant can respond to questions that are asked in direct messages or in channels where the assistant is directly mentioned.

[Read these instructions](/starter-kit/slack/README.md) to learn how to integrate your COVID-19 chatbot with Slack.

![Slack Gif](/starter-kit/slack/readme_images/Slack.gif)

### Integrate your COVID-19 chatbot with Node-RED

Want to create a voice-enabled chatbot? This tutorial teaches you how to [create a voice enabled chatbot using Node-RED](./starter-kit/node-red/README.md) and the Watson Assistant, Watson Speech to Text, and Watson Text to Speech nodes.

### Embed your COVID-19 chatbot on a Node.js website

Finally, you can embed your COVID-19 crisis communication chatbot on a Node.js website.

- Follow the [COVID-Simple installation instructions](./starter-kit/covid-simple/README.md)

## License

This solution starter is made available under the [Apache 2 License](LICENSE).
