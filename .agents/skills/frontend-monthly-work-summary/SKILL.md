---
name: frontend-monthly-work-summary
description: Accepts an online URL containing front-end project monthly work records, reads and parses page content, extracts key work content, progress, problems, achievements, and outputs a concise, professional, focused output result summary report. Use when users need to summarize front-end monthly work logs from a web page link.
metadata:
  author: user-custom
  version: "1.0.0"
  category: front-end-work
allowed-tools: Read Fetch
---

# Frontend Monthly Work Summary Skill

## Function Overview
This skill is used to automatically generate a clean, professional, key-pointed work summary report from an online document URL that records front-end project monthly work content.

## Input
- A valid online URL (HTTP/HTTPS) that contains front-end developer monthly work logs, task records, or work notes.

## Processing Steps
1. Verify the input URL validity and access availability.
2. Fetch and read the full text content of the page.
3. Parse and extract front-end related work information, including but not limited to:
   - Completed development tasks
   - Page/component reconstruction & optimization
   - Bug fixes & online issues
   - Performance optimization (loading speed, runtime, bundle size)
   - Collaboration & cross-team support
   - Technical research & tool upgrading
   - Unfinished work & next-month plan
4. Filter redundant descriptions, retain core results and key data.
5. Organize into structured, concise, professional summary language.
6. Output a clean, readable final work summary report.

## Output Rules
- Keep language concise, business-oriented, result-oriented.
- Highlight achievements and quantifiable results.
- Avoid trivial daily descriptions.
- Structure: Overview → Key Outputs → Risks & Support → Next Plan (optional).
- Keep total length moderate, suitable for work reports or monthly summaries.

## Example Output Structure
### Frontend Development Work Summary (Month)
1. **Core Outputs**
   - Completed XX page development & XX component encapsulation
   - Optimized page loading performance by XX%
   - Fixed XX online bugs & XX requirement adjustments
   - Completed technical research on XX
2. **Collaboration & Support**
   - Cooperated with back-end/design/test to complete XX joint debugging
3. **Next Month Plan**
   - Focus on XX function iteration & performance optimization

## Edge Cases
- If the page content cannot be accessed, return a friendly prompt.
- If the content is too short or irrelevant to front-end work, remind and extract available information as much as possible.
- If there are no obvious achievements, summarize according to actual completion status objectively.