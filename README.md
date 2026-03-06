# Security Engineer Live Coding Assessment

Our call is 60 minutes total. We expect about 40 minutes of that to be coding time. You'll likely need the other 20 minutes for setup and Q&A.

We do NOT expect you to create a polished solution in this short amount of time. We want to see how you approach solving one of the tasks below. Briefly explain your choices as you build. You may ask questions at any point. Nothing in this repo is intended to trick you or trip you up. If you're confused or would like clarificaiton, please ask.

This assessment is open book. You are free to use any of the resources below just like you would at work:
- Use docs and internet search
- Use AI tools (Cursor, ChatGPT, Claude, etc.)

You will be evaluated based on:
- Solution approach and tradeoffs (why did you build it that way and what you would improve if you had more time?)
- Communication (clear reasoning, assumptions, and decisions)
- Security/compliance reasoning

Please share your screen first then pick **one** task below to work on.

## Task 1 - SOC 2 to ISO 42001 Mapping

You are given a vendor SOC 2 Type II report and asked to map evidence to internal ISO 42001 controls by end of day.

Goal: show how you would use AI to do ~90% of this quickly. Try implementing traceability, validation, confidence flags, human review.

Use these files for this task:
- `task-1-soc2-mapping/soc2-report.md` - sample vendor SOC 2 report to extract controls/evidence from.
- `task-1-soc2-mapping/iso-42001-controls.md` - internal ISO 42001 control set to map findings to.

## Task 2 - AI Governance Proxy (Prompt Fairness Gate)

ISO 42001 requires ongoing AI impact checks (bias, fairness, transparency). Manual review does not scale.

Goal: design/build an automated gate that checks system prompt changes and blocks risky updates before production (script, LLM checker, policy engine, or workflow automation).

Use these files for this task:
- `task-2-ai-governance-proxy/fairness-controls.md` - policy rules your checker should enforce.
- `task-2-ai-governance-proxy/sample-prompt-changes/` - baseline + safe/risky prompt edits to test your gate logic.

## Task 3 - Security Questionnaire Automation

You must answer 50 customer security questionnaires by EOD across mixed formats.

Goal: build a tool/workflow that extracts questions, maps them to a knowledge base, and drafts responses for review while preventing hallucinated capabilities.

Use these files for this task:
- `task-3-security-questionnaires/questionnaires/` - sample customer questionnaires across CSV, XLSX, and DOCX formats.
- `task-3-security-questionnaires/knowledge-base.md` - approved answer source to match against and avoid hallucinations.

## Task 4 - Compliance-as-Code for AI Impact Assessment

Engineers currently complete AI impact forms manually for prompt/data changes.

Goal: automate impact-assessment drafting from Pull Request changes (detect triggers, summarize risk, prefill fields, route for approval).

Use these files for this task:
- `task-4-compliance-as-code/impact-assessment-template.md` - fields your automation should pre-fill for reviewers.
- `task-4-compliance-as-code/sample-pr/` - mock PR artifacts (changed prompt/data config + diff) to scan for impact triggers.
