# AI-Chatbot

This project is a Python-based chatbot that uses Google Generative AI (Gemini) and Langchain to help answer questions related to Governance, Risk, and Compliance (GRC). It leverages knowledge extracted from multiple PDF documents on key GRC topics to provide informed responses.

## Features

- **PDF Text Extraction**: Extracts content from multiple PDF files related to GRC, including frameworks like COSO, NIST, GDPR, and the Sarbanes-Oxley Act.
- **Generative AI Model**: Uses the Google Generative AI (Gemini) model to provide context-aware responses to user queries.
- **Chat History**: Maintains a conversation history, which helps the assistant provide more accurate and relevant responses over time.
- **API Integration**: Connects to the Google Generative AI model using an API key, which must be set in the environment.
- **Response Formatting**: The chatbot's responses are structured in JSON format, displaying the topic, summary, sources, and tools mentioned.

## Data Used
- **GDPR**
- **COSO** - Enterprise Risk Management (ERM) Framework
- **NIST Cybersecurity Framework**
- **The Sarbanes-Oxley Act**
- **The Federal Reserve’s Supervisory Guidance on Managing Risks**
- **The Institute of Internal Auditors (IIA) Standards**
- **The Basel III Framework**
- **OECD** Guidelines for Corporate Governance
- **Risk Management for IT Systems**

## Requirements

- Python 3.x
- Required Python packages:
  - `langchain`
  - `python-dotenv`
  - `pydantic`
  - `langchain-google-genai google-generativeai`
  - `PyPDF2`
  
## Code
Two variations were created: one where the PDF data is directly included in the prompt, and another where the data is stored separately as a knowledge base.
`Code1` is data in prompt 
`Code2` is data stored in knowlage base 

# Outputs 
Each version is asked ten questions, with their token usage, response times, and answers recorded for comparison.

## Code1


### Key Points in Risk Management for IT Systems

**User:** What are the key points in Risk Management for IT Systems

**Assistant:** Risk Management for IT Systems is a crucial process involving risk assessment, mitigation, and continuous evaluation. Key points include:

**Risk Management Overview:**
- Risk management is essential for protecting an organization's mission by securing IT systems.
- It should be integrated into the System Development Life Cycle (SDLC) at every phase.
- Key roles include Senior Management, CIO, System Owners, Business Managers, ISSOs, and IT Security Practitioners, all playing vital parts.

**Risk Assessment (a nine-step process):**
- **System Characterization:** Defining the scope of the IT system, including hardware, software, interfaces, data, personnel, mission, criticality, and sensitivity.
- **Threat Identification:** Identifying potential threat-sources (natural, human, environmental) and compiling a threat statement.
- **Vulnerability Identification:** Identifying system weaknesses through vulnerability sources, security testing, and checklists.
- **Control Analysis:** Analyzing implemented or planned controls to minimize threats.
- **Likelihood Determination:** Rating the probability of a threat exploiting a vulnerability (High, Medium, Low).
- **Impact Analysis:** Assessing the potential damage (High, Medium, Low) to confidentiality, integrity, and availability.
- **Risk Determination:** Calculating the overall risk level using a risk matrix (e.g., High, Medium, Low).
- **Control Recommendations:** Suggesting feasible and cost-effective controls to mitigate identified risks.
- **Results Documentation:** Documenting the entire risk assessment process and findings in a report.

**Risk Mitigation:**
- Involves prioritizing, evaluating, and implementing controls to reduce risk to an acceptable level.
- Mitigation options include risk assumption, avoidance, limitation, planning, transference.
- A risk mitigation strategy prioritizes actions based on risk levels, evaluates control options for feasibility and effectiveness, and conducts cost-benefit analysis.
- Control implementation should be cost-effective and minimally impact mission capabilities.
- Control categories are Technical (Supporting, Preventive, Detect & Recover), Management, and Operational.
- Residual risk remains after implementing controls, requiring DAA authorization.

**Evaluation and Assessment:**
- Risk management is an ongoing, iterative process requiring continuous evaluation and assessment.
- Regular reviews are necessary due to evolving threats, technologies, and organizational changes.
- Senior management commitment, IT team support, competent risk assessment teams, user awareness, and continuous evaluation are key to a successful program.

---

### What rights do children have under GDPR

**User:** What rights do children have under GDPR

**Assistant:** Under GDPR, children are recognized as vulnerable data subjects who merit specific protection. This enhanced protection is particularly relevant to online services, marketing, and profiling. Key aspects include the requirement for clear and plain language in communications addressed to children, the necessity of parental consent for processing children's personal data for information society services (especially for those under 16, with Member States having the option to lower the age to 13), and the right to erasure (right to be forgotten), especially concerning data collected when they were children. Automated decision-making and profiling that produce legal effects or significantly affect a child are restricted. These measures aim to ensure children are aware of risks, consequences, and safeguards related to the processing of their personal data.

---

### What countries does GDPR apply to

**User:** What countries does GDPR apply to

**Assistant:** The General Data Protection Regulation (GDPR) applies to the processing of personal data in the context of an establishment of a controller or a processor in the European Union, regardless of whether the processing takes place in the Union or not. It also applies to the processing of personal data of data subjects who are in the Union by a controller or processor not established in the Union, where the processing activities are related to offering goods or services to data subjects in the Union or monitoring their behavior within the Union. Furthermore, GDPR applies to the processing of personal data by a controller not established in the Union, but in a place where Member State law applies by virtue of public international law.

---

### Summarize the key areas of NIST Cybersecurity Framework

**User:** Summarize the key areas of NIST Cybersecurity Framework

**Assistant:** The NIST Cybersecurity Framework (CSF) 2.0 is structured around six core functions that represent the fundamental principles of a robust cybersecurity program. These functions are:

*   **Govern (GV):** Establishes and monitors the organization's cybersecurity risk management strategy, expectations, and policies. It emphasizes incorporating cybersecurity into broader enterprise risk management and understanding organizational context.
*   **Identify (ID):** Focuses on understanding the organization's current cybersecurity risks by identifying assets, suppliers, and the surrounding risk landscape. This function also includes the identification of improvement opportunities.
*   **Protect (PR):** Involves implementing appropriate safeguards to manage cybersecurity risks. This includes access control, awareness and training, data security, platform security, and technology infrastructure resilience.
*   **Detect (DE):** Enables the timely detection and analysis of cybersecurity events. This function encompasses continuous monitoring and adverse event analysis to identify potential incidents.
*   **Respond (RS):** Outlines actions to be taken once a cybersecurity incident is detected. Key elements include incident management, analysis, mitigation, and reporting and communication.
*   **Recover (RC):** Focuses on the restoration of assets and operations affected by a cybersecurity incident. This involves incident recovery planning and communication to ensure business continuity.

---

### How do The Federal Reserve’s Supervisory Guidance on Managing Risks and NIST differ

**User:** How do The Federal Reserve’s Supervisory Guidance on Managing Risks and NIST differ

**Assistant:** The Federal Reserve’s Supervisory Guidance on Managing Risks, as exemplified by Operating Circular 1, focuses on operational and compliance risks specific to financial institutions interacting with the Federal Reserve System, particularly concerning Master Accounts, overdrafts, and operational security within that system. It's prescriptive in nature, outlining rules and conditions for account relationships and financial services. In contrast, NIST, represented by the Cybersecurity Framework (CSF) 2.0 and SP 800-30, offers broader, non-prescriptive frameworks and guidelines for risk management, especially in cybersecurity and IT systems. NIST CSF 2.0 is a framework for managing cybersecurity risks across any organization, emphasizing desired outcomes and adaptability, while NIST SP 800-30 provides a detailed methodology for risk assessment and mitigation within IT systems, applicable across the System Development Life Cycle (SDLC). The Federal Reserve guidance is operational and regulatory, aimed at financial institutions' specific risks within the FRB ecosystem, while NIST documents are strategic and methodological, offering adaptable frameworks for broader risk management, particularly in cybersecurity.

---

### Which of the documents are Legal requirements and which are advisory

**User:** Which of the documents are Legal requirements and which are advisory

**Assistant:** Based on the provided PDF documents, some are legal requirements that organizations must comply with, while others are advisory, offering best practices and guidance. Specifically, CELEX_32016R0679_EN_TXT.pdf (GDPR), sarbanes_oxley_act_of_2002.pdf (Sarbanes-Oxley Act), and 090123-operating-circular-1.pdf (Federal Reserve Operating Circular No. 1) are legal requirements. Compliance-Risk-Management-Applying-the-COSO-ERM-Framework.pdf (COSO ERM Framework) and NIST.CSWP.29.pdf (NIST Cybersecurity Framework) are advisory documents.

---

### Is company data and personal data treated differently

**User:** Is company data and personal data treated differently

**Assistant:** Yes, company data and personal data are treated differently, especially within the context of GRC. Personal data, as defined and heavily regulated by GDPR (CELEX_32016R0679_EN_TXT.pdf), receives specific and stringent protection due to fundamental rights concerns for natural persons. GDPR establishes detailed rules for processing personal data, emphasizing consent, lawfulness, fairness, transparency, and data subject rights. Company data, while also subject to protection and risk management considerations within frameworks like COSO ERM (Compliance-Risk-Management-Applying-the-COSO-ERM-Framework.pdf) and NIST CSF (NIST.CSWP.29.pdf), is primarily viewed in terms of organizational risk, financial reporting accuracy (Sarbanes-Oxley Act), and business continuity. These frameworks emphasize the importance of managing risks to all types of organizational data, including compliance risks related to personal data, but the legal and regulatory emphasis on the fundamental rights associated with personal data creates a distinct and heightened level of protection and differentiated treatment compared to company data.

---

| **User** | **Response Time** | **Input Tokens** | **Output Tokens** |
|----------|-------------------|------------------|-------------------|
| What are the key points in Risk Management for IT Systems | 8.99s | 299303 | 578 |
| What rights do children have under GDPR | 7.91s | 299299 | 225 |
| What countries does GDPR apply to | 10.39s | 299298 | 194 |
| Summarize the key areas of NIST Cybersecurity Framework | 5.84s | 299301 | 331 |
| How do The Federal Reserve’s Supervisory Guidance on Managing Risks and NIST differ | 10.41s | 299307 | 397 |
| Which of the documents are Legal requirements and which are advisory | 7.49s | 299304 | 311 |
| Is company data and personal data treated differently | 11.02s | 299301 | 362 |


## Code2

### Key Points in Risk Management for IT Systems

**User:** What are the key points in Risk Management for IT Systems

**Assistant:** Risk Management for IT systems is a crucial process for organizations to protect their information assets and ensure business continuity. Key points include establishing a risk management framework encompassing risk assessment, response, and monitoring. This involves identifying IT-related risks, analyzing their potential impact and likelihood, and developing appropriate mitigation strategies. Continuous monitoring and review are essential to adapt to evolving threats and vulnerabilities. Effective risk management also requires clear communication, stakeholder engagement, and integration with overall enterprise risk management. 

---

### What rights do children have under GDPR
**User:** What rights do children have under GDPR  

**Assistant:** The GDPR pays special attention to the rights of children, recognizing their vulnerability and the need for specific protection regarding their personal data.  Key aspects include:  
   * **Parental Consent for Information Society Services:** For online services offered directly to children (information society services), consent for processing their personal data is lawful only if given or authorized by the child's parent or guardian. The age of consent is set by individual member states but cannot be lower than 13 years old and no higher than 16 years old. Below this age, parental consent is required.  
   * **Right to Erasure ('Right to be Forgotten'):** Children have the same rights as adults, including the right to erasure. This is particularly important online where children may have created content or shared personal data without fully understanding the long-term implications. The GDPR strengthens the right to be forgotten, making it easier for individuals, including children (through their parents or guardians), to request the deletion of their personal data.  
   * **Right to Information and Access:** Children, or their parents/guardians on their behalf, have the right to be informed about the processing of their personal data in a clear and transparent manner. This includes information about the purposes of processing, categories of data, recipients, and rights related to their data. They also have the right to access this data.  
   * **Data Protection by Design and Default:** The GDPR encourages data protection by design and by default, which is particularly relevant for services used by children. This means that data protection should be integrated into the design of systems and processes, and that default settings should be the most privacy-friendly.  
   * **Consideration in Data Protection Impact Assessments (DPIAs):** When processing is likely to result in a high risk to the rights and freedoms of natural persons, especially when using new technologies, a DPIA is required. Processing data of children often necessitates a DPIA due to their vulnerability.  
   
   In summary, the GDPR enhances the rights of children regarding their personal data, primarily through the requirement of parental consent for online services, strengthening the right to erasure, ensuring transparent information and access, and emphasizing data protection by design and default. 

---

### What countries does GDPR apply to

**User:** What countries does GDPR apply to  

**Assistant:** The GDPR applies to all organizations operating within the European Union (EU) and the European Economic Area (EEA). It also applies to organizations outside of the EU and EEA if they process the personal data of individuals within the EU or EEA, regardless of the organization's location or the citizenship of the data subject.  This extra-territorial reach is a key aspect of GDPR. 

---

### Summarize the key areas of NIST Cybersecurity Framework

**User:** Summarize the key areas of NIST Cybersecurity Framework  

**Assistant:** The NIST Cybersecurity Framework (CSF) is structured around five core functions that are designed to be concurrent and continuous activities to enable an organization to dynamically manage cybersecurity risk. These five functions are: Identify, Protect, Detect, Respond, and Recover.  
   * **Identify:** This function focuses on developing an organizational understanding to manage cybersecurity risk to systems, assets, data, and capabilities. Activities include identifying assets, business environment, governance, risk assessment, and risk management strategy.  
   * **Protect:** This function outlines appropriate safeguards to ensure the delivery of critical infrastructure services. Activities include access control, awareness and training, data security, information protection processes and procedures, maintenance, and protective technology.  
   * **Detect:** This function defines the appropriate activities to identify the occurrence of a cybersecurity event in a timely manner. Activities include anomalies and events detection, security continuous monitoring, and detection processes.  
   * **Respond:** This function includes appropriate activities to take action regarding a detected cybersecurity incident. Activities include response planning, analysis, mitigation, improvements, and communication.  
   * **Recover:** This function involves appropriate activities to restore capabilities or services that were impaired due to a cybersecurity incident. Activities include recovery planning, improvements, and communications. 

### How do The Federal Reserve’s Supervisory Guidance on Managing Risks and NIST differ

**User:** How do The Federal Reserve’s Supervisory Guidance on Managing Risks and NIST differ

**Assistant:** The Federal Reserve’s Supervisory Guidance on Managing Risks and the NIST Cybersecurity Framework are both important frameworks related to risk management, but they differ significantly in scope and focus. The Federal Reserve’s guidance is specifically designed for financial institutions under its supervision and takes a broad enterprise-wide approach to risk management, encompassing all types of risks including credit, market, operational, and compliance risks. It emphasizes the roles of boards and senior management in overseeing and managing these risks within the financial sector.  In contrast, the NIST Cybersecurity Framework is narrowly focused on cybersecurity risks and is applicable to a wider range of organizations across all sectors, not just financial institutions. NIST provides a voluntary, yet widely adopted, framework to help organizations improve their cybersecurity posture by describing a structured and repeatable approach to identify, protect, detect, respond to, and recover from cyber threats. While the Federal Reserve guidance is supervisory and aimed at ensuring regulatory compliance within the financial industry, NIST is more of a general best practice framework for cybersecurity risk management that organizations can voluntarily adopt or may be required to implement as part of broader regulatory requirements. In essence, the Federal Reserve’s guidance is broader in risk scope but narrower in industry application, while NIST is narrower in risk scope (cybersecurity) but broader in industry application. 

---

### Which of the documents are Legal requirements and which are advisory
 
**User:** Which of the documents are Legal requirements and which are advisory  
 
**Assistant:** Within the provided GRC documents, some are legal requirements that organizations must comply with, while others are advisory frameworks or guidelines that offer best practices and recommendations.  
   **Legal Requirements:**  
   * **GDPR (General Data Protection Regulation):**  A regulation in EU law on data protection and privacy, legally binding for organizations operating within the EU or processing EU citizens' data.  
   * **The Sarbanes-Oxley Act (SOX):** A US federal law that mandates certain practices primarily for publicly traded companies to improve financial disclosures and corporate governance.  
   * **The Basel III Framework:**  An internationally agreed set of measures to strengthen the regulation, supervision, and risk management of banks. While initially an agreement, its implementation into national law makes it a legal requirement for financial institutions in many jurisdictions.  
   
   **Advisory Documents:**  
   * **COSO - Enterprise Risk Management (ERM) Framework:** A widely recognized framework for establishing and improving enterprise risk management practices. It is advisory, providing guidance on how organizations can effectively manage risk, but not legally mandated.  
   * **NIST Cybersecurity Framework:** A voluntary framework developed by the National Institute of Standards and Technology to help organizations manage and reduce cybersecurity risks. It is advisory and provides a structured approach to cybersecurity risk management.  
   * **The Federal Reserve’s Supervisory Guidance on Managing Risks:**  Guidance issued by the Federal Reserve to banks and financial institutions. While not law itself, it represents regulatory expectations and strongly influences supervisory practices, making it effectively advisory with significant practical implications.  
   * **The Institute of Internal Auditors (IIA) Standards:** Professional standards for the practice of internal auditing. These standards are advisory, outlining best practices for internal audit functions but are not legal mandates.  
   * **OECD Guidelines for Corporate Governance:**  Recommendations and principles for corporate governance developed by the Organisation for Economic Co-operation and Development. These guidelines are advisory, aiming to promote good corporate governance practices globally but are not legally binding laws. 

---

### Is company data and personal data treated differently

**User:** Is company data and personal data treated differently  

**Assistant:** Yes, company data and personal data are treated differently, primarily due to varying legal, ethical, and risk considerations. Personal data, especially as defined under regulations like GDPR, receives significantly more stringent protection and is subject to specific legal requirements regarding collection, processing, storage, and disposal. This is because personal data relates to identifiable individuals and its misuse can lead to privacy violations, identity theft, and other harms. Frameworks like GDPR, OECD Guidelines for Corporate Governance, and general risk management principles emphasize the need for robust controls and accountability for personal data. Company data, while also requiring protection for business continuity, competitive advantage, and regulatory compliance (e.g., SOX for financial data), does not typically fall under the same strict privacy-focused regulations as personal data. The level of control and security applied to each type of data is driven by the potential impact of its breach or misuse, with personal data breaches often carrying higher risks related to individual rights and regulatory penalties. 

---

| **User** | **Response Time** | **Input Tokens** | **Output Tokens** |
|----------|-------------------|------------------|-------------------|
| What are the key points in Risk Management for IT Systems | 2.10s | 456 | 149 |
| What rights do children have under GDPR | 4.30s | 452 | 509 |
| What countries does GDPR apply to | 1.80s | 451 | 125 |
| Summarize the key areas of NIST Cybersecurity Framework | 2.88s | 454 | 313 |
| How do The Federal Reserve’s Supervisory Guidance on Managing Risks and NIST differ | 4.69s | 460 | 339 |
| Which of the documents are Legal requirements and which are advisory | 4.41s | 456 | 548 |
| Is company data and personal data treated differently | 5.11s | 453 | 278 |


# Comparison
This section compares two different response models, **Code 1** and **Code 2**, based on various factors like content depth, response structure, response time, and quality. It aims to highlight the strengths and differences between the two models to help users choose the most suitable one for their needs.

---

## Content & Detail

**Code 1** provides very detailed and comprehensive responses, often outlining processes and frameworks extensively. For example, it goes into great detail when explaining the **nine-step risk assessment process**, **GDPR rights for children**, and various **regulatory frameworks**. These responses tend to offer a broader view on topics like **risk management** and **legal requirements**, often breaking them down into multiple categories or steps for greater clarity.

On the other hand, **Code 2** presents more concise responses that focus on the key points without delving deeply into each area. For instance, in the **NIST Cybersecurity Framework** section, Code 2 provides a brief summary of the five functions, while Code 1 elaborates on each function in a more structured, methodical manner, providing a deeper understanding.

---

## Response Structure

The response structure of **Code 1** tends to break down complex topics into more digestible parts. It often uses bullet points, clear divisions, and longer explanations. This methodical approach makes it more suitable for detailed research or study, where a thorough understanding of each aspect is required. In contrast, **Code 2** presents the information in a more streamlined way, focusing on summarizing the key points without diving into excessive detail. Code 2’s concise style makes it more appropriate for quick overviews or situations where a basic summary is sufficient.

---

## Response Times

In terms of response times, **Code 1** typically takes longer, with responses averaging around **8.99 seconds** for a topic like "Risk Management for IT Systems." This delay is due to the in-depth analysis and more comprehensive explanations that Code 1 provides. On the other hand, **Code 2** delivers responses much faster, with response times averaging **2.10 seconds** for the same topic. The speed is largely due to Code 2’s concise and simpler structure, which does not require as much elaboration.

---

## Length of Responses

The length of responses in **Code 1** is generally much longer, often exceeding **300 words**. This is because Code 1 tends to offer detailed and thorough explanations, occasionally elaborating on each point to provide a more complete understanding of the subject. In contrast, **Code 2** offers shorter responses, usually under **150 words**, as it provides high-level summaries or focuses on the most important points without going into as much detail.

---

## Legal & Advisory Clarifications

Both models clarify the difference between **legal requirements** and **advisory documents**. However, **Code 1** offers more context and examples, providing a deeper explanation of these distinctions. **Code 2**, in contrast, keeps the clarification simple and straightforward, providing only the basic difference between legal and advisory sources, without the additional context that Code 1 includes.

---

## Response Quality & Tone

The tone and response quality of **Code 1** is more formal and detailed. This makes it well-suited for **academic** or **professional** settings where thorough understanding and deep explanations are needed. On the other hand, **Code 2** uses a more informal, to-the-point tone, making it ideal for users who need quick answers or summaries without diving into too much detail. Code 2 is more user-friendly for casual users who require fast insights.

---
