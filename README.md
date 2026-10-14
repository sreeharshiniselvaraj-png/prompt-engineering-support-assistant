# AI Customer Support Assistant

An AI-powered customer support workflow for FlexTime that demonstrates prompt engineering, customer intent classification, policy-compliant response generation, response verification, and human escalation.

## Project Objectives

- Classify customer queries by issue category and sentiment.
- Generate empathetic, professional support replies using the CARE approach.
- Apply FlexTime's support policies consistently.
- Check drafted replies for policy violations, unsupported promises, and privacy risks.
- Create escalation tickets for cases that require human review.
- Document the prompt chain and logical routing with a Mermaid flowchart.

## Project Files

| File | Description |
|---|---|
| `support_prompt_library.md` | Reusable prompt templates for the Intent Classifier, CARE Responder, Reflection/Verification, Conversation Summarizer, and Escalation Ticket generator. |
| `conversations_portfolio.md` | Three example support scenarios showing classification, responses, and escalation handling. |
| `chatbot_documentation.md` | System manual describing the prompt chain, target personas, security guardrails, policies, and Mermaid flow diagram. |
| `README.md` | Project overview, objectives, file descriptions, policy summary, and usage guide. |

## Prompt-Chaining Workflow

1. **Intent Classifier:** Identifies the query category and customer sentiment.
2. **CARE Responder:** Drafts an empathetic, professional reply using the customer's query and relevant policy.
3. **Reflection and Verification:** Checks the draft for policy compliance, tone, unsupported claims, and privacy risks.
4. **Routing:** Sends approved replies to the customer and routes cases requiring review to human support.
5. **Summarizer / Escalation:** Summarizes the conversation and prepares a handover ticket when needed.

## FlexTime Policy Rules Used in the Examples

- **Operating hours:** Monday–Friday, 9:00 AM–5:00 PM EST.
- **Refunds:** Support agents may issue refunds up to $20 without approval. Refund disputes above $20 must be escalated.
- **Email changes:** The customer must verify their current account ID and billing ZIP code before changing their profile email.
- **Privacy:** Do not share billing API keys, database hashes, or internally marked ticket numbers with customers.

These rules are included for this training project. The chatbot should not claim that an action has been completed unless it has been verified.

## Example Scenarios

- **Scenario A — Email Change:** The chatbot asks the customer to verify their current account ID and billing ZIP code before proceeding.
- **Scenario B — Duplicate $15 Charge:** The chatbot acknowledges the customer's frustration and reviews the billing details. If the duplicate charge is confirmed, a $15 refund is within the $20 no-approval limit.
- **Scenario C — $120 Refund Request:** The requested refund exceeds the $20 limit and is routed to human support for review. The chatbot does not claim that the refund has been approved or processed.

## How to Use This Project

1. Open `support_prompt_library.md` and review the prompt templates.
2. Copy the Intent Classifier prompt into ChatGPT and provide a customer query.
3. Use the classification output as input to the CARE Responder prompt.
4. Review the drafted response using the Reflection and Verification prompt.
5. If the request exceeds policy limits or a violation is flagged, use the Escalation Ticket prompt to prepare a handover.
6. Compare the outputs with the examples in `conversations_portfolio.md`.
7. Refer to `chatbot_documentation.md` for the system design and flow diagram.

**Note:** This repository documents a prompt-engineering workflow. It does not by itself deploy a live chatbot, connect to FlexTime systems, verify real billing data, or automatically issue refunds.

## Project Presentation

- **Project name:** AI Customer Support Assistant
- **Presenter:** [Your Name]
- **Loom presentation:** [Paste your Loom video URL here]

Replace `[Your Name]` with your name and paste your shareable Loom recording URL before submitting the project.

## Repository Setup

This project uses Markdown files and can be viewed directly on GitHub.

1. Create a public GitHub repository named `prompt-engineering-support-assistant`.
2. Upload the four Markdown files listed above using **Add file → Upload files**.
3. Commit the changes to the `main` branch.
4. Open `README.md` on GitHub to confirm it renders correctly.
5. Verify that the repository is public and that the Loom link is accessible to your intended audience.

No terminal commands or software installation are required to read these files on GitHub.

## Author

**[Your Name]**  
Prompt Engineering Hands-On Project
