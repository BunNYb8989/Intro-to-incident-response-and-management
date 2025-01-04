# Intro-to-incident-response-and-management
Intro to IR & IM

Incident Response

Incident Response covers the technical aspect of dealing with an incident. This is the portion that is responsible for answering the primary question:

What happened?

To answer this question, the incident response team uses several techniques and technologies. These investigations often begin in the SOC by reviewing the information provided with the event that triggered the alert. This could be provided with one of the following tools:

EDR or AV Alert - Usually these tools would create an alert for anomalous activity that has occurred on a specific host. For example, the EDR could alert that there were attempts made to monitor the keystrokes of a user.
Network Tap Alert - Network taps provide alerts for anomalous network activity. For example, there could be an alert that a host is scanning other hosts in the estate.
SIEM Alert - The Security Information and Event Management (SIEM) system could alert on a custom rule that was created by the analysts. For example, an impossible travel rule where a user's account is being logged in from two different countries simultaneously.
When an alert is created, a lot of information is provided to the analyst. The first step is to investigate this information to better understand what is happening. In these systems, when an alert is generated, other key pieces of information are also attached to the alert. For example, in the case of the SIEM alert, the analyst would be able to review not only the latest logon events with the user's account, but the history of their logon events for the last couple of months.

However, sometimes the alert information is not sufficient and we have to gather more information than what is currently provided. This process is usually referred to as Digital Forensics. Here, we perform a much more hands-on investigation that can include the following:

Recovering the hard disk from the infected host to investigate how the malware got on there in the first place.
Recovering the data from volatile memory (such as from the computer's RAM) from the infected host to investigate how the malware works.
Recovering system and network logs from several devices to uncover how the malware spread.
The overall goal of Incident Response is to try and understand the scope of the incident. If we do not accurately understand the scope, the Incident Management process cannot take adequate steps to close off the incident. Both extremes can be incredibly damaging. If we misunderstand the scope to be larger than what it is, we could authorise more drastic actions than required, which would disrupt the business. If we misunderstand the scope to be smaller than what it is, we could take insufficient actions against the threat actor, meaning the incident would not be over.

Incident Management

Incident Management covers the process aspect of dealing with an incident. This is the portion that is responsible for answering the primary question:

How do we respond to what happened?

Once we understand the scope of the incident, the next question is how we will manage the incident. Incident Management has to take care of several things, such as:

Triaging the incident to accurately update the severity of the incident as new information becomes available and getting more stakeholders involved to help deal with the incident, such as Subject Matter Experts (SMEs).
Guiding the incident actions through the use of playbooks.
Deciding which containment, eradication, and recovery actions will be taken to deal with the incident.
Deciding the communication that will be sent internally and externally while the team deals with the incident.
Documenting the information about the incident, such as the actions taken and the effect that they had on dealing with the incident.
Closing the incident and taking the information to learn from the incident and improve future processes and procedures.
Effective incident response and management are required to deal with an incident. It is often mistaken that only technical skills are required to deal with incidents. The management aspect is just as important.

We will use an example in this case: A user has reported a phishing email

Level 1: SOC Incident

At level one, these are often not even classified as incidents. Usually, these require a purely technical approach. At this level,  upon investigation of our example, the analyst finds that it is an isolated event and therefore simply updates the mail filtering rules to block the sender. These levels of incidents can happen several times a day and are usually quick to deal with and the analyst deals with this themselves.

However, in our example, a Computer Emergency Readiness Team (CERT) Incident may be invoked if the investigation found that several users received the email.

Level 2: CERT Incident

At level two, several analysts in the SOC may be involved in the investigation. A CERT Incident is one where we don't yet have enough to raise the alarm bells. Still, we are concerned and therefore performing additional investigation to determine the scope of the incident. Usually, the analyst would request assistance and more members of the SOC team would get involved. In our example, at this point, we would be investigating if any of those users interacted with the email. We would also like to better understand what the email does.

If we were able to stop the incident before any of the users interacted with the email, we would usually stop at this level. However, if we discover that the email contains malware and that some of the users actually interacted with the email, we would invoke a Computer Security Incident Response Team (CSIRT) incident.

Level 3: CSIRT Incident

At level three, the entire SOC is placed on high alert and actively working to resolve the incident. At this point, the entire SOC team will focus on the single incident to deal with it. Analysts and the forensic team work to uncover the full scope of the incident and the management team is taking action against the threat actor to contain the spread of the malware, eradicate it from hosts where it is discovered, and recover affected systems.

If the team is able to stop the spread of the attack before any disruptions can occur or the threat actor can escalate their privileges within the estate, the CSIRT team will close the incident. However, if it is determined that the scope is larger through investigation, we would invoke a Crisis Management Team (CMT) Incident.

Level 4: CMT Incident

At level four, it is all hands on deck and officially a full-scale cyber crisis. The CMT would usually consist of several key business stakeholders such as the entire executive suite, members from the legal and communication teams, as well as other external parties, such as the regulator or police. Furthermore, at this level, we start to move into the territory of what is called "nuclear" actions. Rather than simple actions to contain, eradicate, and recover, this team can authorise the use of nuclear actions, such as taking the entire organisation offline to limit the incident's damage.

# Task 1
At what level (number only) of an incident would the SOC be placed at high alert and to deal with an incident?

```
3
```

At what level (number only) of an incident would it be classified as a cyber crisis?

```
4
```

Which component (IR or IM) is responsible for trying to answer the question: How do we respond to what happened?

```
IR
```

Which component (IR or IM) is responsible for trying to answer the question: What happened?

```
IM
```

# Task 2


