# OpenAgent Demo

**Example Prompt:**
"Perform an analysis on Microsoft (MSFT)."

**Example Structured Output JSON:**
```json
{
  "summary": "Microsoft continues to scale its operations with mild daily market volatility, anchored heavily by the persistent adoption of its AI infrastructure.",
  "keyInsights": [
    "Yahoo Finance shows steady ticker traction around previous closes.",
    "Wikipedia notes continued mainstream usage of their Azure AI footprint."
  ],
  "risks": [
    "Broader sector cooldown regarding consumer tech hardware sales."
  ],
  "opportunities": [
    "Unmatched enterprise software lock-in driving cloud ARR."
  ],
  "sentiment": "POSITIVE",
  "confidenceScore": 96,
  "reasoningSummary": "Both Finance extraction arrays and Wikipedia historical events were synthesized to measure their active enterprise strength securely."
}
```

**What Happened Internally:**
1. The **Planner (Router)** parsed "Microsoft (MSFT)" and scheduled calls for Yahoo Finance (`query: MSFT`) and Wikipedia (`query: Microsoft`).
2. The Node APIs pulled the latest stock ticks and historical wiki text.
3. The **Extractor** compressed those messy text payloads down to high-value vectors.
4. **Plumber** validated the JSON payload from the **Analyst**, stripping away broken string escapes, and formatting the exact `keyInsights` array into the application.
