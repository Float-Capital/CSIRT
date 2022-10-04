# Incident Response Plan

Process Owner: [Jason Smythe](https://github.com/JasoonS)

# Overview

Cyberattacks are increasingly becoming more prevalent, and so it is imperative to view cybersecurity holistically, from the point of view of response and recovery in addition to prevention.

Although measures / mitigations can be put in place to drastically reduce the risk from materialising (e.g. front-running protection mechanism to prevent price manipulation, multi-signature wallets to custody investment capital, smart contract audits, web application security scans, etc.), Float should still be prepared for a “worst-case” scenario or unprecedented crisis event. 

This Cybersecurity Incident Response Plan (CSIRT) is a procedural document that gives key stakeholders instructions on how to respond to a serious security incident. The response plan outlines predetermined set of instructions or procedures to detect, respond, and limit consequences of a malicious cyber attacks against Float’s information systems. 

These procedures are designed to enable security personnel to identify, mitigate, and recover from malicious incidents, such as unauthorised access to a system or data, denial of service, or changes / usage of the system affecting its integrity or expected behaviour. 

# Incident Response Lifecycle

1.  [Preparation](#preparation)
    1. Key stakeholders
    2. Incident scenarios
    3. Documenting an incident
2. [Detection and analysis](#detection-and-analysis) – **click here if you’ve identified a potential incident**
    1. Signs of an incident
    2. Assessing the impact
    3. Gathering evidence
3. [Immediate response actions](#immediate-response-actions) – **click here if you have just confirmed there is an active cyber security incident**
    1. Who to tell
    2. How to reach them
    3. Keep the incident confidential
4. [Containment, Eradication & Recovery](#containment-eradication--recovery) – **click here if you’re working to contain an active incident**
    1. Identifying the vulnerability
    2. Containing the incident
    3. Communicating with stakeholders
5. [Post-Incident Activity](#post-incident-activity)
    1. Drafting an incident report
6. [Incident runbooks](#runbooks)

# Preparation

## Objectives

- Prepare the team / organization for an incident
- Identify & define response team - key stakeholders / persons that need to be involved and/or informed
- Identify top applicable scenarios & create runbooks
- Train stakeholders in response runbooks
- How to invoke the response team
- Ensure all the right documentation is recorded

## Key stakeholders

### To be informed immediately

- Jason Smythe - Founder
    - Telegram: @Cooolkid
    - Whatsapp: <redacted>
    - Discord: Jason | float & wildcards#9999
- Jonathon Clark - Founder
    - Telegram @jonjonclark
    - Whatsapp: <redacted>
    - Discord: jonjon | float#2270
- Denham Preen - Founder:
    - Telegram: @denhampreen
    - Whatsapp: <redacted>
    - Discord: ! Denham | float.capital#5167

## Incident scenarios

These are potential scenarios, but Float may in the future be subject to other attack vectors

### Scenario 1

- Smart contract exploit due to logic bugs, lack of parameters or precondition controls, front-running, arithmetic error, etc. that leads to extraction or loss of user funds

### Scenario 2

- Market manipulation that renders the markets unusable for other traders (but is using the system by design)

### Scenario 3

- Git Hub compromise, such as hard-coded sensitive data (passwords, tokens, and authentication keys), badly configured access permissions, compromised CI/CD pipeline, etc, that results in access to private repositories

### Scenario 4

- Integration partners downtime, such as a supply-chain attack, that renders the Float App unavailable (e.g closure / freezing of a market due to not receiving any Price Feeds updates from an Oracle) . Unavailability of the Float App can cause a loss in trust / decrease in reputation / loss in users

## Documentation

It is important to maintain incident documentation to ensure a systematic record for efficient review of the incident, reporting of the incident and lessons learned.

Immediately open an incident ticket on internal notion under Policies & Procedures. Include the following:

- Status of the incident
- Summary of the incident
- Indicators of compromise related to the incident
- Actions taken to resolve the incident
- Impact assessment of the incident
- Lessons learned
- Evidence gathered

# Detection and analysis

## Objectives

- ensure timely detection of an incident and identify the scope of an incident
- identify the immediate actions to take following identification of an incident
- identify the reporting and communication guidelines to follow

## Signs of an incident

| Scenario | Indicators |
| --- | --- |
| Smart Contract Exploit | Exfiltration of funds, unexpected behaviour, unusual movements of funds  |
| Market Manipulation | Whale trader (relative to liquidity in the given market) where there is noticeable period of fluctuation in exposure |
| GitHub compromise | Malicious PRs, dangerous / vulnerable packages |
| Supply chain / integration partners down-time | Unexpected behaviour, no ChainLink oracle update for longer than expected SLA, Gelato Keeper downtime |

The common sources of precursors and indicators include:

1. Alerts (e.g. monitoring tools)
2. Logs (e.g. system logs)
3. Indicators of compromise (IoC)
4. Industry events
5. Market analysis reports
6. Publicly available information
7. Users 

## Assessing the impact of an incident

After identifying the an incident, the impact of the incident needs to be determined. Important question to consider when determining the impact of the incident 

- Are the systems or services currently affected critical?
- Are there any workarounds or mitigating actions that can be deployed?
- How many users are affected?
- Can this incident be contained effectively?
- Is this incident spreading slowly or quickly—and affecting other users or systems?
- Are there potential legal or regulatory ramifications?

Critical, High, Medium, Low

## Evidence gathering

Any collected evidence should utilize a hash activity / integrity checks to ensure the integrity of the collected data. This process can be used to verify that evidence has not been altered from its original source, and helps ensure admissibility for potential legal proceedings.

# Immediate response actions

This section contains the immediate steps to follow once an incident has been identified.

1. **Immediately notify the pod heads**
    1. Create a Telegram Group with
        1. Campbell – @CampbelFloat
        2. Denham –  @denhampreen
        3. Jason – @Cooolkid
        4. Jonjon – @jonjonclark
    2. In this group, share all evidence gathered around the incident.
    3. Make sure to communicate the severity of the incident, and the level of urgency required
    4. Send a second line of communication via WhatsApp to:
        1. Denham –  <redacted>
        2. Jason – <redacted>
        3. Jonjon – <redacted>
    5. Open an incident ticket on Notion under Policies & Procedures
    6. Continue to monitor the situation and share updates with the team
    7. Keep all information about the incident confidential – do not share with anyone outside of the Pod Heads team until it is agreed upon
    
    Follow predefined [Runbooks](#runbooks) depending on nature of the incident.
    

# Containment, eradication & recovery

## Objectives

- contain the incident to prevent further attacker activity, widespread damage
- ensure good decision-making
- define a communications plan

An essential part of containment is decision-making (e.g. shut down a system, pause a market, disconnect a device from a network, delete API keys, disable username, etc.). Such decisions are much easier to make with predetermined strategies and procedures for incident containment. To define and document the strategies and procedures, utilize playbooks and runbooks to simplify tasks.

## Containing the incident

See [Runbooks](#runbooks) 

## Incident communications

All communications around an incident must be carefully managed to mitigate fallout and negative outcomes for all stakeholders affected, internal and external. Follow the steps below before sharing any information:

### Identify the stakeholders affected

1. A broad range of stakeholders can be affected, from users, to investors, to team members.
2. Different methods of communication must be employed for different stakeholders.
3. Communications to stakeholders must be sent by the responsible individuals or teams. 
4. *Do not communicate with any stakeholders without approval from the pod heads team.*
5. A non-inclusive list can be found below:

| Stakeholder group | Communications medium | Responsible |
| --- | --- | --- |
| Team members | Discord, team syncs | Pod heads |
| Investors | Email, Telegram | Denham, Jason, Jonjon |
| Regulators | Formal reports | Legal counsel |
| Advisors | Discord, email | Denham, Jason, Jonjon |
| Float users | Discord, Twitter | Campbell |
| Technical partners | Telegram, email | Sven |

### Draft an incident communications plan

Once stakeholders have been identified, a communications plan must be drafted. This will include:

1. Who will be notified
2. How they will be notified
3. Who will notify them
4. When they will be informed
5. What information will be shared with them

### Draft the message to each stakeholder

Each stakeholder should receive very precise information. Each message should contain the following:

1. An overview of the incident
2. How the incident affects them and how severely
3. What other stakeholders have been affected
4. The nature of the incident and how it occurred
5. How the Float team responded and is continuing to respond
6. Next steps for addressing the incident
7. A disclaimer about the risks inherent to DeFi / the Float app

**For each message, pay very careful attention to the following:**

- **Remember that everything you say could have legal and or reputational ramifications. Do not worry about being nice.**
- Do not promise / offer / or imply compensation. If Float is to compensate a stakeholder, they will be informed only after funds have been allocated for this purpose.
- Use very specific language. Do not talk about exploits, vulnerabilities or hacks unless the investigations have confirmed precisely what ocurred.
- Do not take responsibility on behalf of yourself, or Float.
- Give no more information than is needed.

### Approve the message with the pod heads

Don’t send any information to anyone without express approval from the pod heads. 

### Keep comms transparent

Keep all messaging with affected stakeholders in public places. Whether email, Discord, Telegram, or whatever – do not send any comms that are not visible to all pod heads. 

# Post-incident activity

## Objectives

- emphasis on lessons learned with key stakeholders
- reports highlighting gaps and improvements

## Drafting an incident report

An incident reports should contain the following information:

- Date and time of the incident
- Date and time of incident closure
- Scope of the incident
- Name of the person who reported the incident
- Organization and business unit of the affected person
- Incident description
- Affected systems and/or providers and respective SLAs
- Incident classification (severity classification)
- Company/customer impact analysis
- Resolution
- A “lessons learned” section to determine successes and needed improvements to develop
an enhanced response to prevent future incidents

*Unless stated otherwise, incident reports, and all other information related to identified or potential cyber security incidents are considered confidential information that should not be shared with anyone.*

# Runbooks

## Scenario 1 – Smart Contract Exploit

Smart Contract Exploit due to logic bugs, lack of parameters or precondition controls, front-running, arithmetic error of integers, etc. that leads to exfiltration of funds.

Exfiltration of funds - Identified via unexpected behaviour, unusual movements of funds, user complaint.

### Immediate Steps

1. **Review exploit transactions to identify vulnerability** - [Jason Smythe](https://github.com/JasoonS)
    1. Tools Used:
        1. [Tenderly Debugger](https://dashboard.tenderly.co/tx/mainnet/0xf427afc17bd30a84f4b47dc2eaa176115cf28bdea1110245d3b0948ca3b6595c/debugger)
        2. [Foundry Transaction Replay Trace/Debugger](https://book.getfoundry.sh/reference/cast/cast-run.html#cast-run)
        3. [ethtx.info](https://ethtx.info/)
2. **Pause contracts (if possible)** or take other defensive action, consider offensive action (i.e. white hat rescues)
    1. Execute defensive action scripts → You do NOT want to be scrambling to figure out who can sign to take defensive actions - **[Jason Smythe](https://github.com/JasoonS)
    2. Review Transaction(s) - [JonJon Clark](https://github.com/moose-code)
3. **Review all contracts to identify knock-on vulnerabilities. Pause those as necessary**
4. **Update UI to reflect current status - [Denham Preen](https://github.com/DenhamPreen)
5. **Contact security partners** 
    1. ByteRocket
    2. Code4Arena
    3. Sherlock
6. **Communicate to affected users via Discord and/or Twitter - Campbell Easton**
    1. Follow [Incident communications](#incident-communications) - Update regularly (every 4 to 12 hours) as meaningful new information or developments are available - help reassure your community that you are working to address the situation
    - Run all messages by the pod heads to ensure no information is shared that inadvertently puts security at risk or commits to specific remediation before all facts are known
7. **Prepare patch for contracts, ideally following development process guidelines**
    1. Have patch reviewed and signed off on by past auditors
    2. Have patch reviewed by as many trusted members of the team and community as possible
    3. If the patch or potential interactions are complex enough to warrant it, strongly consider a short [Code4rena](https://code4rena.com/) contest (can be started within 48 hours)
    4. Deploy patch - **[Jason Smythe](https://github.com/JasoonS)
8. **Draft and post Incident Report**
    1.  See [Drafting an incident report](#drafting-an-incident-report) 
9. **Keep evidence secure**

## Scenario 2 – Market Manipulation

**Market Manipulation (e.g. whale trader) that renders the markets unusable for other traders (but is using the system by design)**

Whale trader (relative to liquidity in the given market) where there is noticeable period of fluctuation in exposure.

### Immediate Steps

1. **Review exploit transactions to identify vulnerability - [@Jason Smythe]**
    1. Tools Used:
        1. [Tenderly Debugger](https://dashboard.tenderly.co/tx/mainnet/0xf427afc17bd30a84f4b47dc2eaa176115cf28bdea1110245d3b0948ca3b6595c/debugger)
        2. [Foundry Transaction Replay Trace/Debugger](https://book.getfoundry.sh/reference/cast/cast-run.html#cast-run)
        3. [ethtx.info](https://ethtx.info/)
        4. Internal Data Modelling -[ @Woo Sung Dong]
2. **Consult with advisors** 
3. **Update UI to reflect any changes - [@Denham Preen ]**
4. **Communicate to affected users via Discord and/or Twitter - [@Campbell Easton ]**
    1. Follow [Incident communications](#incident-communications) - Update regularly (every 4 to 12 hours) as meaningful new information or developments are available - help reassure your community that you are working to address the situation
    - Run all messages by the pod heads to ensure no information is shared that inadvertently puts security at risk or commits to specific remediation before all facts are known
5. **Prepare patch for contracts, ideally following development process guidelines**
    1. Have patch reviewed and signed off on by past auditors
    2. Have patch reviewed by as many trusted members of the team and community as possible
    3. If the patch or potential interactions are complex enough to warrant it, strongly consider a short [Code4rena](https://code4rena.com/) contest (can be started within 48 hours
    4. Deploy patch - You do NOT want to be scrambling to figure out who can sign to take defensive actions - [@Jason Smythe]
6. **Draft and post Incident Report**
    1.  See [Drafting an incident report](#drafting-an-incident-report) 
7. **Keep evidence secure**

## Scenario 3 – GitHub or infrastructure Compromise

**Git Hub compromise, such as hard-coded sensitive data (passwords, tokens, and authentication keys), badly configured access permissions, compromised CI/CD pipeline, etc, that results in access to private repositories**

1. Review logs (IP address, User actions, etc.) - [Response team]
2. Sign into GitHub as Admin, remove user from Float Organization - [@Jason Smythe]
3. Change Password and Do not share password with anyone 
4. Log out / expire all sessions on all devices to log malicious actor out of account
5. Determine impact - [ Response Team]
6. Restore from backup (if applicable)

## Scenario 4 – Integration Partner Failure

**Integration partners downtime, such as a supply-chain attack, that renders the Float App unavailable (e.g closure / freezing of a market due to not receiving any Price Feeds updates from an Oracle) . Unavailability of the Float App can cause a loss in trust / decrease in reputation / loss in users**

1. **Review downtime errors  to identify cause - [@Jason Smythe]**
    1. Tools Used:
        1. [Tenderly Debugger](https://dashboard.tenderly.co/tx/mainnet/0xf427afc17bd30a84f4b47dc2eaa176115cf28bdea1110245d3b0948ca3b6595c/debugger)
2. **Consult with advisors** - [@Jonjon Moose]
3. **Update UI to reflect any changes -** [@Denham Preen ]
4. **Communicate to affected users via Discord and/or Twitter -** [@Campbell Easton ]
    1. Follow [Incident communications](#incident-communications) - Update regularly (every 4 to 12 hours) as meaningful new information or developments are available - help reassure your community that you are working to address the situation
    - Run all messages by the pod heads to ensure no information is shared that inadvertently puts security at risk or commits to specific remediation before all facts are known
5. **Manage SLA with Third Party / Integration Partner**
    1. Get continuous updates
    2. Breach of conduct / SLA
6. **Restore Operations** 
7. **Draft and post Incident Report**
    1.  See [Drafting an incident report](#drafting-an-incident-report) 
8. **Keep evidence secure**