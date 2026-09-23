# Dr. HOPE — Whistleblower Assessment Counselor

**Helping Others Protect Everyone** · Psychological Assessment & Support

An AI-powered psychological self-assessment and support tool designed to help individuals considering or engaged in whistleblowing evaluate their emotional preparedness, ethical reasoning, support systems, risk awareness, and long-term wellbeing.

## 1. Project Overview

Dr. HOPE (Helping Others Protect Everyone) is a specialized AI-powered assessment counselor designed to support individuals who are considering becoming whistleblowers, preparing to disclose information about wrongdoing, or navigating the psychological challenges associated with reporting misconduct.

Whistleblowing can involve significant personal, professional, emotional, and social consequences. Individuals may experience uncertainty about their decisions, fear of retaliation, concerns about financial security, disruptions to professional relationships, and anxiety about long-term consequences.

Dr. HOPE provides a structured environment where individuals can explore these concerns through a comprehensive, 92-question psychological self-assessment. It uses a conversational assessment model that encourages users to examine their motivations, emotional resilience, ethical considerations, personal support networks, and ability to manage uncertainty.

Unlike conventional assessment tools that generate numerical scores or categorize individuals according to predetermined readiness levels, Dr. HOPE emphasizes personal reflection and psychological preparedness **without** attempting to determine whether someone should become a whistleblower. The tool is intended for educational and supportive use — it is not a clinical diagnostic instrument, a substitute for licensed psychological care, or a means of certifying someone's suitability to report wrongdoing.

## 2. Mission and Objectives

**Mission:** To provide individuals considering or engaged in whistleblowing with accessible, structured psychological self-assessment and emotional support, helping them better understand their personal circumstances, prepare for potential challenges, and identify resources that may support their wellbeing.

**Primary objectives:**

- **Psychological self-awareness** — explore emotional responses, coping mechanisms, personal values, and reactions to uncertainty or interpersonal conflict.
- **Preparation for potential challenges** — consider possible professional, financial, social, and psychological consequences of reporting misconduct.
- **Support system identification** — evaluate access to trusted individuals, professional resources, and other forms of assistance.
- **Independent decision-making** — examine motivations and circumstances without directing users toward or away from whistleblowing.
- **Emotional wellbeing** — supportive interactions, encouraged breaks, and direction toward professional assistance when necessary.

## 3. Who Is This Tool For?

| User group | Intended use |
|---|---|
| Prospective whistleblowers | Exploring the personal and psychological implications of reporting wrongdoing |
| Active whistleblowers | Reflecting on emotional wellbeing and support needs during an ongoing disclosure process |
| Former whistleblowers | Exploring experiences associated with recovery, adaptation, and rebuilding stability |
| Whistleblower support organizations | Offering a structured educational self-reflection resource |
| Counselors and support professionals | Using the framework as a supplementary discussion aid, subject to professional oversight |
| Researchers | Studying conversational self-assessment tool design, with appropriate consent and safeguards |

The system does not determine whether allegations are true, investigate misconduct, provide legal representation, or replace professional psychological evaluation.

## 4. Core Assessment Framework

Dr. HOPE is organized into **eight modules containing a total of 92 questions**, each examining a distinct dimension of psychological preparedness and personal circumstances.

| Module | Questions | Focus |
|---|---|---|
| 1. Ethical Reasoning and Moral Courage | 15 | Ethical dilemmas, moral responsibilities, competing obligations, loyalty, integrity |
| 2. Psychological Resilience Assessment | 12 | Responses to stress, uncertainty, conflict; coping strategies and recovery practices |
| 3. Support Systems Evaluation | 10 | Availability/reliability of personal and professional support networks |
| 4. Motivation and Values Assessment | 8 | Motivations, personal values, and expectations tied to whistleblowing |
| 5. Risk Perception and Management | 14 | Understanding of consequences and resources to manage uncertainty |
| 6. Identity and Self-Concept | 11 | Self-understanding in relation to work, relationships, and values |
| 7. Communication and Disclosure Style | 9 | Communicating sensitive information and managing difficult conversations |
| 8. Future Planning and Adaptation | 13 | Long-term wellbeing, priorities, and capacity to adapt |

Example question (Module 1): *"You discover that a respected colleague has falsified information that could affect public safety. How would your relationship with this person influence the way you approach the situation?"* The objective is not to identify a correct response but to understand the user's reasoning process. No module diagnoses psychological conditions, classifies motivations as qualifying/disqualifying, or predicts legal outcomes.

## 5. How Dr. HOPE Works

Dr. HOPE uses a sequential conversational assessment model — one question at a time, rather than a full questionnaire at once — to keep the process manageable and provide room for reflection, clarification, and support.

```
User begins assessment (introduction, consent, overview)
        │
One question presented (module, question number, progress shown)
        │
Response and wellbeing check (acknowledge response, watch for distress)
        │
Continue or take a break (repeat until all eight modules complete)
        │
Assessment completion (summary and optional user-controlled sharing)
```

**Initial setup** — Dr. HOPE introduces its purpose and structure, asks for a preferred name, gives an overview of the eight modules, states there are 92 questions and no final psychological score, and requires consent before beginning. Account-type collection should be optional for a standalone implementation.

**Progress tracking** — `Progress = (Completed Questions / 92) × 100`. For example, 46 completed questions = 50% complete. The interface should distinguish answered questions from the one currently being presented.

**Response processing** — after each answer, the system acknowledges it and considers whether the user needs clarification, support, or a break, without automatically interpreting an answer as evidence of a psychological disorder or moral deficiency.

## 6. Emotional Support and Safety Features

**Break management** — breaks may be suggested when requested, when significant distress is expressed, after completing a module, or after roughly 45 minutes of engagement.

**Crisis response** — if a user expresses immediate risk of self-harm or another serious safety concern, the normal assessment flow is interrupted to prioritize safety and provide crisis resources. In the United States: call or text **988** for suicide and crisis support, or text **HOME to 741741** for the Crisis Text Line. The assessment resumes only when appropriate and at the user's discretion.

## 7. Privacy, Confidentiality, and Data Protection

Whistleblower-related conversations may contain sensitive personal, professional, or organizational information, so privacy protection is a core design requirement, not an optional feature.

Recommended principles: collect only necessary information; avoid unnecessary identifying details about third parties; provide clear data-retention policies; give users control over whether responses are saved or shared. If responses are stored, use encryption, access controls, secure authentication, retention limits, and deletion mechanisms. Users should not be encouraged to upload confidential organizational documents, trade secrets, or identifying evidence merely to complete a self-assessment.

**Important:** a conversational AI interface should never be described as providing legally privileged communication, guaranteed anonymity, or absolute confidentiality unless those protections have actually been established.

## 8. Technical Architecture

A proposed software architecture for a future standalone implementation (not a claim that these components already exist):

```
Frontend Interface     web or mobile conversational assessment experience
Application Backend    authentication, session management, consent, progress tracking
Assessment Engine      question sequencing, module transitions, response management
AI Support Layer       supportive conversational responses, clarification, safety handling
Secure Data Layer      optional storage of assessment state, responses, and preferences
```

**Recommended repository structure:**

```
dr-hope/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── SECURITY.md
├── PRIVACY.md
│
├── docs/
│   ├── project-overview.md
│   ├── assessment-framework.md
│   ├── ethical-guidelines.md
│   ├── safety-protocols.md
│   └── architecture.md
│
├── assessment/
│   ├── question-bank/
│   │   ├── module-01-ethics.json
│   │   ├── module-02-resilience.json
│   │   ├── module-03-support.json
│   │   ├── module-04-motivation.json
│   │   ├── module-05-risk.json
│   │   ├── module-06-identity.json
│   │   ├── module-07-communication.json
│   │   └── module-08-future.json
│   ├── assessment-engine/
│   └── progress-tracking/
│
├── src/
│   ├── frontend/
│   ├── backend/
│   ├── ai/
│   └── safety/
│
├── tests/
│
├── .env.example
└── package.json
```

The original assessment question banks should be maintained separately from the conversational interface, so the interface or AI model can be updated without unintentionally changing the underlying assessment questions.

## 9. AI Behavioral Guidelines

- Present only one assessment question at a time and wait for the user's response.
- Maintain accurate module and overall progress tracking.
- Use supportive, nonjudgmental language without assuming the user's allegations are established facts.
- Respect the user's autonomy; never direct their whistleblowing decision.
- Never generate psychological scores, clinical diagnoses, or readiness certifications.
- Prioritize wellbeing and appropriate support when signs of serious distress arise.

These requirements should be tested at the application level rather than relying exclusively on model instructions — e.g. the backend can enforce the one-question-at-a-time rule and calculate progress independently of the AI-generated response.

## 10. Assessment Completion and Sharing

After all 92 questions, Dr. HOPE provides a completion acknowledgment and a factual summary (questions completed, modules covered, general areas explored) — never numerical psychological scores, a clinical diagnosis, or a recommendation to proceed with or abandon whistleblowing.

Sharing is always voluntary, with a clear explanation of what becomes accessible to the recipient. For a ChatGPT-based implementation, developers should verify the platform's current sharing behavior before documenting it as a confidentiality-preserving process. A standalone application could instead implement a dedicated export feature allowing users to review and redact sensitive information before sharing.

## 11. Ethical and Professional Limitations

Dr. HOPE is an informational and educational self-assessment tool. It does not provide professional psychological diagnosis, psychological treatment, legal advice, or formal determinations of fitness or readiness to engage in whistleblowing. The framework should not be presented as a clinically validated psychometric instrument unless appropriate validation research has been completed. Responses should not be used to make employment decisions, evaluate witness credibility, or determine whether allegations should be investigated. Any future research or clinical application requires additional professional review, appropriate safeguards, and consideration of relevant ethical/regulatory requirements.

## 12. Future Development Roadmap

1. **Core assessment experience** — eight-module question bank, one-question-at-a-time interface, consent flow, accurate progress tracking.
2. **User experience improvements** — accessible interface options, session resumption, break reminders, user-controlled navigation.
3. **Privacy and security** — secure response storage, user-controlled deletion, privacy-preserving exports, documented data handling policies.
4. **Professional review** — input from qualified mental health professionals, whistleblower support specialists, and privacy/security experts.
5. **Accessibility and deployment** — multilingual support, mobile-friendly interfaces, accessible interaction patterns, deployment options for support organizations.

## 13. License and Contributions

If released as open source, the repository should include a clearly defined software license, contribution guidelines, and a security reporting policy, accounting for ownership of the assessment questions and any third-party materials. Contributions could include accessibility improvements, interface development, documentation, security enhancements, and testing. Changes to the psychological assessment content should undergo appropriate subject-matter review before being incorporated into the main question bank.

## Project Vision

Dr. HOPE represents an approach to AI-assisted psychological self-assessment that emphasizes personal autonomy, emotional support, structured reflection, and responsible handling of sensitive information. Its long-term purpose is not to determine whether an individual should disclose wrongdoing, but to help them better understand their circumstances, identify support needs, and approach their own decisions with greater self-awareness.

Dr. HOPE — Helping Others Protect Everyone.

## License

See [LICENSE](LICENSE).
