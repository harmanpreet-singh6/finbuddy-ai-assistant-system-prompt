# FinBuddy: Making a Bank's AI Assistant Follow the Rules with a System Prompt

**A FinTech case study on when a plain chat is enough and when a business needs a system prompt.**

**Author:** Harmanpreet Singh · BBA (FinTech), Chitkara Business School · **Tool:** ChatGPT · November 2026

## The case

**KoshBank** (fictional) is a digital bank for college students in Pune with 3 lakh users. It wants to launch **FinBuddy**, an in-app AI assistant. Its compliance team worries that a chatbot could give stock tips, ask for OTPs or invent interest rates. As a Business Analyst, I tested whether a system prompt can make the AI follow the bank's rules every time.

## The data

10 synthetic customer questions created with AI (7 English, 3 Hinglish), including 6 "trap" questions designed to make the AI break rules. I wrote the correct behaviour for each question before testing.

## Approach

| Step | Set-up | Task |
|---|---|---|
| 1 | Plain chat | One simple general question |
| 2 | Plain chat | All 10 customer questions |
| 3 | System prompt (v1) | The same 10 questions |
| 4 | System prompt (v2) | Failed questions re-tested after a fix |
| 5 | Roles | Same question with no role, an expert role and a friendly role |

## Results

| Metric | Plain chat | System prompt |
|---|---:|---:|
| Answers that followed every rule (/10) | 6/10 | 9/10 |
| Personal data handled safely | Yes | Yes |
| No investment tips | No | Yes |
| Closing line present (/10) | 3/10 | 10/10 |

## Key learnings

1. **A plain chat is enough for general questions:** It answered basic banking questions reasonably well, but its responses were not always consistent with the bank's requirements.
2. **A system prompt enforces business rules:** It improved compliance with instructions related to OTP protection, investment advice, accurate banking information and customer privacy. It corrected several failures from questions 2, 5, 7 and 9.
3. **Version 2:** I added a rule requiring the AI to admit when it doesn't know an answer, never guess bank charges or interest rates, and direct customers to official bank support for account-specific issues. This improved consistency in the re-test.
4. **Roles:** An expert role made the answers more professional and structured, while a friendly role made them easier to understand. The role mainly changed tone and presentation rather than guaranteeing greater accuracy.

## My recommendation to KoshBank

FinBuddy could be suitable for a limited pilot focused on general banking FAQs, but it is not ready
