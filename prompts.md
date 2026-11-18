# Prompts

## Tier 3: LLM zero-shot sentiment classification

**Model:** claude-haiku-5-5
**Settings:** max_tokens=10, thinking disabled

**Prompt sent for each review (test set and hard cases):**

    Is this review positive or negative? Reply with one word only.

    <review text>

**How the reply is read:**
- If the reply contains "positive", the label is positive.
- If it contains "negative", the label is negative.
- Anything else is counted as "invalid", which is scored as wrong.

**Cost calculation:** Input tokens at $0.10 per million and output tokens at
$0.50 per million, using the token counts returned by the API.

**Notes:**
- Zero-shot: no examples are given in the prompt.
- The prompt was written once and not changed after seeing test results.