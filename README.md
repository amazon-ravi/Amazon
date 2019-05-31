# Amazon
Build Skills with the Alexa Skills Kit
Alexa provides a set of built-in capabilities, referred to as skills. For example, Alexa's abilities include playing music from multiple providers, answering questions, providing weather forecasts, and querying Wikipedia.

The Alexa Skills Kit lets you teach Alexa new skills. Customers can access these new abilities by asking Alexa questions or making requests. You can build skills that provide users with many different types of abilities. For example, a skill might do any one of the following:

Look up answers to specific questions ("Alexa, ask tide pooler for the high tide today in Seattle.")
Challenge the user with puzzles or games ("Alexa, play Jeopardy.")
Control lights and other devices in the home ("Alexa, turn on the living room lights.")
Provide audio or text content for a customer's flash briefing ("Alexa, give me my flash briefing")
What Kind of Skill Do You Want to Create?
The first step in building a new skill is to decide what your skill will do. The functionality you want to implement determines how your skill integrates with the Alexa service and what you need to build. The Alexa Skills Kit supports building different types of skills.

To create ...	Use this skill type
A skill that can handle just about any type of request.

For example:

Look up information from a web service
Integrate with a web service to order something (order a car from Uber, order a pizza from Domino's Pizza)
Interactive games
Just about anything else you can think of
Custom skill (custom interaction model)

You define the requests the skill can handle (intents) and the words users say to invoke those requests (utterances).

A skill that lets a user control and query cloud-enabled smart home devices such as lights, door locks, cameras, thermostats and smart TVs.

For example:

Turn lights on and off
Change the brightness of dimmable lights
Change the color or color temperature of a tunable light
Change the temperature on a thermostat
Query a lock to see if it is currently locked
Ask for a smart home camera feed
Change the volume on a speaker
Change the channel of a TV
Smart Home Skill API (pre-built model)

The Smart Home Skill API defines the requests the skill can handle (device directives) and the words users say to invoke those requests (utterances).

A skill that lets a user control cloud-enabled video services.

For example:

Play a movie
Find a TV show
Change a channel
Pause, rewind, or fast forward video content
Video Skill API (pre-built model)

The Video Skill API defines the requests the skill can handle (device directives) and the words users say to invoke those requests (utterances).

A skill that provides original content for a customer's flash briefing.

Flash Briefing Skill API (pre-built model)

The Flash Briefing Skill API defines the words users say to invoke the flash briefing or news request (utterances) and the format of the content so that Alexa can provide it to the customer.

A skill that enables users to select, listen to, and control audio content streamed through an Alexa-enabled device.

Music Skill API

When you build a music skill, the voice interaction model is defined and handled for you. Alexa interprets user utterances and sends messages to your skill that communicate these requests.

For more details about the differences between different types of skills, see Understand the Different Skill Models.

What Do I Build?
You create a cloud-based service that handles the requests for the skill type and host it in the cloud. The Alexa service routes incoming requests to the appropriate service.

Different types of skills require different types of services:

For a custom skill, you code either an AWS Lambda function or a web service:

AWS Lambda (an Amazon Web Services offering) is a service that lets you run code in the cloud without managing servers. Alexa sends your code user requests and your code can inspect the request, take any necessary actions (such as looking up information online) and then send back a response. You can write Lambda functions in Node.js, Java, Python, C#, or Go.
Alternatively, you can write a web service and host it with any cloud hosting provider. The web service must accept requests over HTTPS. In this case, Alexa sends requests to your web service and your service takes any necessary actions and sends back a response. You can write your web service in any language.
Regardless of how you create your service, you also create a custom interaction model for the skill. This defines the requests the skill can handle and the words users can say to invoke those requests.
For a skill that controls smart home devices such as lights, thermostats, and entertainment devices you can use the Smart Home Skill API. In this case, you develop an AWS Lambda function that accepts device directives from Alexa:

You provide code to handle directives in an AWS Lambda function.
Your skill receives requests in the form of device directives to control a particular device. Your code then handles the request appropriately (for example, by turning on the requested light or turning up the volume).
All voice interactions with the user are handled by the Smart Home Skill API. You don't need to define the words users say to use the skill.
For a skill that controls video content you can use the Video Skill API. In this case, you develop a lambda function that accepts device directives from Alexa:

You provide code to handle directives in an AWS Lambda function.
Your skill receives requests in the form of device directives to control a video service. Your code then handles the request appropriately (for example, by playing a movie).
All voice interactions with the user are handled by the Video Skill API. You don't need to define the words users say to use the skill.
For a skill that provides content such as news, lists, or comedy for a customer's flash briefing, you can use the Flash Briefing Skill API. In this case, you create the skill in the developer console and configure one or more JSON or RSS feeds that contain the content:

To receive your content as a part of their flash briefing, a customer enables your flash briefing skill in the Alexa app, and turns on one or more content feeds.
All voice interactions with the user are handled by the Flash Briefing Skill API. You don't need to define the words users say to use the skill.
You supply one or more reliable content feeds in RSS or JSON format. The content can be audio content that Alexa plays to the customer, or text content that Alexa reads to the customer. You should own the content or have the rights to distribute it.
Next Steps
If you know what you want to build now, start with one of these:

Custom Skills
Smart Home Skills
Flash Briefing Skills
Video Skills
Music Skills
Or, learn more about the Alexa Skills Kit and how skills work:

Understand the Different Skill Models
Understand How Users Interact with Skills
Requirements to Build a Skill
Glossary
