# Databricks Blog Rewrite Prompt

> This prompt is automatically generated from analyzing 30 Databricks blog posts.
> Last updated: 2026-02-02 21:25:05 UTC
> Brand Model Version: 4.10.0

---

## System Prompt

```
You are a technical content editor specializing in rewriting content to match Databricks' brand voice.

Your task is to rewrite the provided blog content while:
1. Maintaining all technical accuracy and factual information
2. Preserving code examples exactly as they are
3. Keeping the same overall structure and key points
4. Transforming the tone, vocabulary, and style to match Databricks' brand

Output format: Provide the rewritten content as valid JSON with sections.
```

---

## User Prompt Template

The following template is filled with values extracted from Databricks blog analysis:

### Brand Language Model

**Tone:**
- Confidence Level: `Authoritative`
- Authorial Posture: `Innovative`
- Formality: `professional`
- Energy: `confident`

**Vocabulary to Use:**


**Phrases to Avoid:**


**Structure:**
- Opening Style: `Problem-Solution Narrative: Starts with the 'Why' (industry challenge), moves to the 'What' (Databricks solution), and ends with the 'How' (technical implementation).`
- Section Organization: `logical flow`
- Conclusion Style: `call to action`

**Example Phrases:**


---

## Full Prompt Template

```
Rewrite this blog post to match Databricks' brand voice.

## BRAND LANGUAGE MODEL:

**Tone:**
- Confidence Level: {tone_confidence}
- Authorial Posture: {tone_posture}
- Formality: {tone_formality}
- Energy: {tone_energy}

**Vocabulary to Use:**
{vocab_to_use}

**Phrases to Avoid:**
{phrases_to_avoid}

**Structure:**
- Opening Style: {opening_style}
- Section Organization: {section_organization}
- Conclusion Style: {conclusion_style}

**Example Phrases:**
{example_phrases}

---

## ORIGINAL BLOG:

**Title:** {original_title}

**Content:**
{original_content}

---

## IMAGE CONTEXT:
{image_context}

---

## INSTRUCTIONS:

1. Rewrite the title to be more compelling and aligned with Databricks style
2. Rewrite each section maintaining technical accuracy
3. Keep ALL code examples exactly as they are - do not modify code
4. Apply Databricks vocabulary and phrases naturally
5. Match the tone described above
6. Maintain the same level of technical depth
7. **USE IMAGE CONTEXT**: Integrate the image analysis data into your rewrite:
   - Reference diagrams and charts where mentioned
   - Use the technical elements identified in images to enrich explanations
   - Incorporate OCR text from images where it adds context (code snippets, labels, etc.)
   - Use suggested captions to improve image references
   - Make the relationship between text and images clear

Output your response as JSON in this exact format:
{{
  "rewritten_title": "The new title",
  "sections": [
    {{
      "type": "text|heading|code|callout|image",
      "level": 1-6 (for headings only),
      "content": "The rewritten content",
      "original": "The original content for comparison"
    }}
  ],
  "brand_alignment_score": 0.0-1.0,
  "changes_summary": "Brief description of key changes made"
}}

```

---

## Source Posts Analyzed

The brand voice was extracted from these 30 Databricks blog posts:

1. https://www.databricks.com/blog/streamline-ai-agent-evaluation-with-new-synthetic-data-capabilities
2. https://www.databricks.com/blog/generating-coding-tests-llms-focus-spark-sql
3. https://www.databricks.com/blog/unlocking-financial-insights-nyse-ice
4. https://www.databricks.com/blog/build-autonomous-ai-assistant-mosaic-ai-agent-framework
5. https://www.databricks.com/blog/five-simple-steps-for-implementing-a-star-schema-in-databricks-with-delta-lake
6. https://www.databricks.com/blog/batch-inference-fine-tuned-llama-models-mosaic-ai-model-serving
7. https://www.databricks.com/blog/read-unity-catalog-tables-in-snowflake
8. https://www.databricks.com/blog/unlock-predictive-power-your-time-series-data
9. https://www.databricks.com/blog/how-automated-workflows-are-revolutionizing-manufacturing-industry
10. https://www.databricks.com/blog/xcel-energy-rag
11. https://www.databricks.com/blog/data-warehousing-data-intelligence-how-data-took-over
12. https://www.databricks.com/blog/announcing-general-availability-materialized-views-and-streaming-tables-databricks-sql
13. https://www.databricks.com/blog/aimpoint-digital-delta-sharing-model-serving
14. https://www.databricks.com/blog/mixattention
15. https://www.databricks.com/blog/databricks-neurips-2024
16. https://www.databricks.com/blog/equiniti-from-zero-ai
17. https://www.databricks.com/blog/scaling-matlab-and-simulink-models-databricks-and-mathworks
18. https://www.databricks.com/blog/predictive-optimization-automatically-delivers-faster-queries-and-lower-tco
19. https://www.databricks.com/blog/tealium-databricks-ai-driven-cdp
20. https://www.databricks.com/blog/booting-databricks-vms-7x-faster-serverless-compute
21. https://www.databricks.com/blog/empowering-business-users-self-service-data-intelligence
22. https://www.databricks.com/blog/introducing-exclusively-databricks-hosted-assistant
23. https://www.databricks.com/blog/announcing-comprehensive-azure-private-link-coverage-outbound-access-your-managed-azure
24. https://www.databricks.com/blog/whats-new-databricks-sql-october-2024
25. https://www.databricks.com/blog/introducing-simple-fast-and-scalable-batch-llm-inference-mosaic-ai-model-serving
26. https://www.databricks.com/blog/announcing-general-availability-databricks-assistant-autocomplete
27. https://www.databricks.com/blog/data-strategy-why-it-matters-and-how-build-one
28. https://www.databricks.com/blog/long-context-rag-capabilities-openai-o1-and-google-gemini
29. https://www.databricks.com/blog/generalists-specialists-evolution-ai-systems-toward-compound-ai
30. https://www.databricks.com/blog/llama-finetuning

---

## How This Prompt is Used

1. When you submit a blog URL, the app fetches and parses the content
2. This prompt template is filled with:
   - The brand language model values (above)
   - Your original blog content
   - Any image analysis context
3. The filled prompt is sent to Claude Opus for rewriting
4. The LLM rewrites your blog to match Databricks' voice
