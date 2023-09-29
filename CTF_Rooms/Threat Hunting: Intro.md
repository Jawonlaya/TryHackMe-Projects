## Task 1: Introduction:

The purpose of this room is to introduce Threat Hunting as a structured concept focusing on its relationship to Incident Response, the Threat Hunting mindset, and the specific goals that Threat Hunting strives to achieve.

### Learning Objectives:

In this room, we will strive to understand what Threat Hunting is and discuss its role in helping secure the organization in contrast with Incident Response.

We will also explore different Threat Hunting goals and discuss how these goals help develop the organization’s security posture. By the end of the room, we will gain a baseline idea of what to look for, how to look for them, and when to decide to move on.

We will also gain an understanding that an Intelligence-driven approach to Threat Hunting, among others, is one of, if not the best way to move forward.

### Room Prerequisites and Expectation Setting:

There are no hard prerequisites in order to gain value from this room; however, it would be very helpful to have a basic understanding of the concept of Threat Intelligence and consequently its role in the effectiveness of Intelligence-driven activities. Knowing the basic concept behind Incident Response, how SOCs operate, and how an organisation’s Security Posture is built would also help a lot in understanding the concepts touched upon by this room.


## Task 2: Threat Hunting Introduction

Threat hunting is an approach to finding cyber security threats where there’s an active effort done to look for signs of malicious activity. In its most basic form, that is the definition of Threat Hunting; however, in order for us to really understand what it entails as well as what its actual role is in the organisation, we will start by contrasting it with Incident Response.

## Threat Hunting in Contrast with Incident Response

Incident Response (IR) is innately reactive. The action, or “response”, is triggered by an initial notification or alert. This initial notification is first triaged, then analyzed, and when enough pieces of evidence point to malicious activity, it is deemed an incident that needs to be responded to and dealt with accordingly.

Threat Hunting, on the other hand, is innately proactive. There is no actual ‘trigger’ that would mobilize a hunt, except for the pursuit of building the strength of the organization’s security posture, guided by Threat Intelligence.

A stark contrast can be seen here - while both are guided by the goal of ensuring the security of the organization, the forces that drive the reactive and proactive nature of Incident Response and Threat Hunting, respectively, hardly share the same direction. This is further steered by the specific objectives that each aims to achieve.

### Task 2 Questions/Answers: 

- What do you call the approach to finding cyber security threats where there's an active effort done to look for signs of malicious activity - `Threat Hunting`
- In this task, what are we contrasting threat hunting with - `Incident Response`
- Incident response is innately reactive. What is done first thing when an initial notification or alert is received - `triaged`
- Threat hunting is innately proactive. What is it guided by - `Threat Intelligence`
- Threat Hunting and Incident Response are two different approaches that aim to ensure one specific goal is met. It is to strengthen the organization's what - `Security Posture`

## Task 3: Threat Hunting Mindset

How you approach a task would usually dictate how successful you will be. It’s easy to rely on the most cutting-edge pieces of technology being offered out there, but across the industry, people would always be the most important part of any security team. And so, while thinking of equipping ourselves with the best tools is important, investing time (and probably money) in learning the proper mindset is as significant. 

### What's the basis for our hunt?

It is imperative that we start our hunt with leads comprised of accurate pieces of information such as known relevant malware as well as trusted Threat Intelligence. Through leads, we give threat hunters better chances of achieving amazing things, from easy wins like looking for malicious binaries to more complex hunting projects like finding patterns of activity of certain groups that target organisations similar to us or industries we’re part of.

### Threat Intelligence

Since we’re talking about dictating the direction of a hunt, it’s essential that we arm ourselves with critical information that will let us know more about the threat(s) that we may be dealing with. Understanding the bad that we may be dealing with is akin to knowing how they might behave within our environment, possibly allowing us to narrow down our search to specific sweet spots such as specific pieces of data they might be interested in, or even knowing which groups or APTs might be particularly interested in targeting us.

### Unique Threat Intelligence

Intelligence on threats that you are able to develop internally is a very valuable asset to have. Not many organizations have the kind of intrusion experience that would allow them to study and develop usable intelligence from said intrusion and even fewer have the capability of developing it internally. Furthermore, intelligence of this kind may have the characteristic of being ultimately unique to your organisation.

Indicators of Compromise (IOCs) specifically documented on previous intrusions would be the most obvious and straightforward example for this one. IOCs immediately give value not only to your threat hunters but also to your detection mechanism, as they’re actual traces of an adversary. Through this, re-intrusions of that specific adversary or other adversaries that employ the same tactics would be easier to spot.

### Threat Intelligence Feeds

As touched upon above, not a lot of organizations are capable of developing valuable and actionable Threat Intelligence internally. While a lot of organizations have their fair share of intrusions, not everyone has that kind of experience under their belt which allows them a front-row seat to a specific adversary’s IOCs, among others. More so, it involves a lot of money, skill, and effort to be able to become an efficient Threat Intelligence producer.

It is not the end for the rest of us, as we can learn from other Threat Intelligence producers via Threat Intelligence feeds. There exist intelligence feeds that are both readily and publicly available. One of the most popular examples of this one is the MISP, an open-source Threat Intelligence and sharing platform. 

On the other hand, there are also paid resources that specialize in producing intelligence, some of which are capable of creating tailored intelligence for your organization.

### Task 3 Questions/Answers: 

- What is the most obvious and straightforward example of a Unique Threat Intelligence - `Indicators of Compromise`
