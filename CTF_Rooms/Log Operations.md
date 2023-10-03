## Task 1: Introduction

### Log Operations
The first thing that comes to mind regarding log analysis is to open the door to the adventure of looking for a needle in a haystack. In case of an incident investigation, are you lost in the log space and wasting your precious time? If so, it's time to do something about log configuration.

In this room, you will learn the configuration approaches required to manage and analyse logs in an operational context and the log information you learned in the previous introductory room.

### Learning Objectives

- Understanding the logic of log management and configuration
- Familiarise with log configuration approaches
- Experience the log configuration process

## Task 2: Log Configurations

"Do you dare to configure your logs, or are you happy to be lost in the madness of the thousands of lines?" In log operations, there are multiple concerns about configuration approaches, and identifying the suitable configuration approach could be a pain point. 

Log configuration is a multifaceted operation that addresses security, operational stability, regulatory compliance, and debugging needs. Adequately configured logs are crucial in cyber security, operational efficiency, regulatory compliance, and software development, providing organisations with comprehensive system, asset, and resource management statistics. Let's look at and understand the scopes and differences of common purposes of log configuration. 

### Security Purposes

Logging and configuration for security purposes are typically planned to detect and respond to anomalies and security issues. For example, configuration to verify the authenticity of user activity to ensure authorisation control and timely detection of unauthorised access. The main focus areas of this approach are:

- Anomali and threat detection
- Logging user authentication data
- Ensuring the system's integrity and data confidentiality

### Operational Purposes

Logging and configuring for operational purposes is usually planned to detect and respond to system errors and identify action points to enhance the system's performance, continuity, and reliability. The main focus areas of this approach are:

- Proactively creating reports and notifications for on-system and component status
- Troubleshooting
- Capacity planning
- Service billing

  ### Legal Purposes

Logging and configuring for legal purposes is similar to security purposes; it is usually planned to stay compliant and increase the alignment with regulations and obligations. Here, the laws, regulations, and compliance standards will vary depending on the work's scope, the data being processed, and the service area being provided. Therefore, each enrollment will come with a set of responsibilities and guidelines to follow. The main focus areas of this approach are:

- Alignment with standards, compliance, regulations, and laws
- `E.g. ISO 27001, COBIT, GDPR, PCI DSS, HIPAA, FISMA`

Legal Compliance Example: A company must have an active central log management system, adequate log configuration, 12-month log retention for logs and affiliated system logs (last three months data must always be ready to search), system and component security checks, and overall yearly audit checks to meet PCI logging compliance.

### Debug Purposes
Logging and configuring for debug purposes is usually planned to boost the system's reliability and enhance provided features by discovering the bugs and potential fault conditions. This configuration scope is not always implemented in the production environment and is mostly used for testing and developing purposes. The main focus areas of this approach are:

- Increasing visibility for the application debugging
- Enhancing efficiency
- Speeding up the development process

  ### Task 3 Challenge:
  - Which of the given log purposes would be suitable to measure the cost of using a service `Operational`
  - Which of the given log purposes would be suitable for investigating application logs for enhancement and stability `Debug`
 
  ## Task 3: Where To Start and What To Do After Deciding the Log Purpose?

  If you already have an objective and scope plan but need help knowing how and where to start, you can use the meeting and brainstorming methods with your team. The meeting might sound like a passive action, but it will start the ball rolling for brainstorming, which will help consider multiple aspects and create a draft plan.

Remember, each log configuration purpose is planned and implemented to fulfill a different goal. Questioning is one of the most common ways to identify needs and facilitate planning. Remember, each implementation is unique, but common base questions must be answered in almost any log configuration planning session. You can use the following questions as a starting point and broaden the list according to the answers. Remember, you will need additional steps like creating a detailed plan, choosing tools/technologies, establishing monitoring and review/analysis processes after answering the initial questions.

### Questions To Ask In Planning Meeting/Session

- What will you log, and for what (asset scope and logging purpose)?
- `Is additional commitment or effort required to achieve the purpose (requirements related to the purpose)?`
- How much are you going to log (detail scope)?
- How much do you need to log?
- How are you going to log (collection)?
- How are you going to store collected logs?
- `Is there a standard, process, legislation, or law that you must comply with due to the data you log?`
- How are you going to protect the logs?
- How are you going to analyse collected logs?
- Do you have enough resources and workforce to do logging?
- Do you have enough budget to plan, implement, and maintain logging?
  
 ### Task 3 Challenge:

- Which question's answer can be "as much as mentioned in the PCI DSS requirements - `How much do you need to log`

## Task 4: Configuration Dilemma: Requirements, Aspirations, Resources, and Investment 

Configuration dilemma reflects the challenges of implementation. As highlighted in the previous task, each log configuration scope comes with responsibilities, guidelines, and challenges. This means that the log configuration and logging are more than a simple practice of enabling logging from the assets and surviving among thousands of lines.

Each log configuration plan results from a unique analysis of the scope, assets, objectives, requirements, and expectations to be applied. Expectations, requirements, and limits are determined with the involvement of system administrators, legal and financial advisors, and managers, if possible. In summary, the main source of the dilemma is finding the balance between requirements, scope, details, and price (financial and labour costs, risks, and investment). During the meeting, there might be some points where participants get off the point, but it is vital to keep in mind that the main objective of the meeting is:

- Meeting specific operational and security requirements (non-negotiable) while also considering the feasibility of improving the capability by implementing additional data and insights.

Last but not least, a comprehensive risk assessment, prioritising security, compliance, and legal needs will be helpful to navigate this dilemma. Finding the balance in "operational and management" level decisions and achieve secure, efficient, proactive, resilient, and sustainable outcomes in the ever-evolving threat/IT landscape and technical operations.

### Translating "Requirements" and "Aspirations" To Operational Level

![Screenshot 2023-10-02 at 23 46 03](https://github.com/Jawonlaya/TryHackMe-Projects/assets/115058054/ea2a63e8-94b5-477e-b66b-72d75c29939a)

While the main focus is the same, two question sets represent two distinct dimensions of logging and analysis:

- The base part heavily relies on an incident detection mindset. Still, it provides a solid framework for logging and analysis but is reactive. The requirements are a good place to start, but it is primarily helpful against known threats.
- The aspirations part is more focused on a threat-hunting mindset. Therefore, it is proactive and requires more resources due to the need to go above and beyond. Therefore, this part is more helpful against advanced and sophisticated threats.

The baseline part is necessary for a solid incident detection and response scope foundation. However, adopting proactive aspirations by adding them to the operational vision is strongly recommended, given the ever-evolving threat landscape. 

### Task 4 Challenge:
- Which requirements are non-negotiable - `operational and security requirements`

## Task 5 Principles and Difficulties

Logging is a critical aspect of the cyber-security and IT operations. It is a process that is as burdensome as functional and requires active resource utilisation. Therefore, it is crucial to implement a proper logging operation and ensure its effectiveness and efficiency. There are multiple principles which help achieve the mentioned goal. The table below highlights some of the essentials.

![Screenshot 2023-10-02 at 23 50 40](https://github.com/Jawonlaya/TryHackMe-Projects/assets/115058054/a2f31b63-634b-49ad-b945-aa3c7088fe98)

### Challenges

Challenges are as much a part of log management as principles. However, most of them can be addressed in the planning section. The table below highlights the main challenges of logging.

![Screenshot 2023-10-02 at 23 51 41](https://github.com/Jawonlaya/TryHackMe-Projects/assets/115058054/8c8b7740-99c5-4b6c-8a87-00c01c3eda71)

### Where To Go From Here

The mentioned principles and challenges are common and can vary according to your case. However, the main point is adhering to logging principles and proactively addressing challenges.

- Your team is working on policies to decide which logs will be stored and which portion will be available for analysis.
Which of the given logging principles would be implemented and improved - `Archiving and Accessibility`

- Your team implemented a brand new API logging product. One of the team members has been tasked with collecting the logs generated by that new product. The team member reported continuous errors when transferring the logs to the review platform.
In this case, which of the given difficulties occurs - `Process and Archive`


