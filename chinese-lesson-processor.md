---
name: chinese-lesson-processor
description: Extract vocabulary, grammar rules, and dialogue structures from one or more language textbook chapters into structured tables and Excel workbooks. Use when the user asks to process single or multiple language lessons, batch-format textbook chapters, generate study sheets, or build curriculum vocabulary tables.
---
# Lesson Processor

Transforms one or more raw language textbook chapters or lesson transcripts into standardized, multi-component study deliverables formatted for tabular and Excel export.

## When to Use

  - Formatting a single newly assigned textbook unit or batch-processing multiple lesson PDFs into study materials.
  - Building vocabulary and grammar reference sheets across one or more chapters.
  - Creating side-by-side bilingual dialogue guides.

## Execution Workflow

1.  **Extract Vocabulary Table**
    
      - Parse all target vocabulary words, phrases, proper nouns, and supplementary/cultural items into a structured table containing:
          - Lesson identifier (when processing multiple files)
          - Category / Level Flag (flagging any item appearing outside the core vocabulary list)
          - Target word (characters/script)
          - Phonetic representation (e.g., Pinyin with tone marks)
          - Part of speech
          - English definition
          - Contextual example sentence (Chinese, Pinyin, and English)

2.  **Summarize Grammar & Patterns**
    
      - Identify core grammatical patterns introduced in each chapter.
      - For each rule, provide:
          - Pattern formula (e.g., `Subject + Time + Verb + Object`)
          - Functional explanation (usage context and nuances)
          - 2-3 illustrative example sentences with Pinyin and English translations

3.  **Format Dialogue Alignment**
    
      - Format dialogue exchanges using a clear aligned layout:
          - Column 1: Source text with aligned phonetic guides (or separate Speaker, Chinese, and Pinyin columns in Excel)
          - Column 2: Natural English translation
      - Append a 1-paragraph synthesis summarizing the narrative context and key pragmatic objectives for each lesson.

4.  **Multi-Sheet Excel Export & Truncated Chat Output**
    
      - **Excel Deliverables (Complete Data):** Process 100% of the vocabulary, grammar rules, and dialogues for every uploaded file into Excel. Generate a multi-sheet `.xlsx` study workbook containing dedicated tabs for `Vocabulary & Phrases`, `Grammar & Patterns`, `Dialogue Alignment`, and `Lesson Overview` (for single files, or individual workbooks plus a Master Workbook for multi-file batches). Never truncate or omit data in the Excel deliverables.
      - **Chat Response Optimization (Truncated Output for Single & Multi-File):** To prevent chat output length issues and token limits, keep the chat response concise for both single-file and multi-file processing. Do NOT print massive exhaustive Markdown tables of every single vocabulary word or dialogue line in the chat window. Instead, provide:
          - A high-level overview and lesson synthesis paragraph.
          - A compact summary table (listing counts of vocabulary items and grammar points, or a representative sample of key terms/patterns).
          - Confirmation of the generated downloadable Excel study workbook(s). Full detailed data remains fully accessible inside the downloadable `.xlsx` files.

## Gotchas

  - Avoid combining phonetic transcription and target characters into a single unseparated string in Excel exports; keep them in separate columns to enable automated parsing and filtering.
  - Keep example sentences strictly at or slightly below the chapter's target reading proficiency level.
  - Never truncate or omit vocabulary items in the generated `.xlsx` files during runs, even when providing a truncated chat summary.
