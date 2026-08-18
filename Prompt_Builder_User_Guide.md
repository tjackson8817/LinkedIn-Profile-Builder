# LinkedIn Profile Builder — User Guide

## What this tool is for

Optimizes your LinkedIn profile specifically for a job search — not general networking content, not "polish my presence." Every section is written to be genuinely impactful to three audiences at once: a recruiter scanning quickly, a hiring manager evaluating fit, and LinkedIn's own (and any employer's) ATS/search indexing — while still reading as a real, specific person instead of a keyword-stuffed template.

Built for mid-level and upper-level management specifically, regardless of industry or function — Director, VP, and C-suite included.

This is a standalone tool, not part of the JobRadar funnel. It's listed on the JobRadar hub page under "Also useful," since it's something you'd reach for independent of where you are in an active application process.

## Before you start

Have ready:

- Your resume, or a detailed written summary of your career (or plan to attach the file directly — see below)
- Your current LinkedIn profile text, if you want Claude to preserve existing phrasing or details not on your resume (optional)
- A target role and industry, if you know them — sharpens the headline, About section, and skills list considerably

## Attaching files instead of pasting text

You have two ways to give Claude your background:

1. **Paste text** into the "Your resume" and/or "Your current LinkedIn profile text" fields, or
2. **Attach a file directly** to the Claude message when you paste the generated prompt in — check the box under the resume field first, so the generated prompt tells Claude to expect an attachment.

To get a PDF export of your current LinkedIn profile: open your profile → click **"More"** (just below your headline) → **"Save to PDF."** Claude reads that file directly — no need to copy each section out by hand.

You can also do both — paste some text and attach a file — the generated prompt handles that combination correctly.

## Field-by-field

### Your background

**Your resume or professional background** *(required, unless you check the attach-instead box)* — paste your resume or a detailed written summary. This is the only source of truth for what's actually true about you, so more specific detail (real numbers, real accomplishments) produces a sharper result than a thin summary.

**"I'll attach my resume and/or LinkedIn profile PDF..."** checkbox — check this if you're skipping the text fields in favor of attaching a file when you paste the prompt into Claude.

**Your current LinkedIn profile text** *(optional)* — paste your existing headline, About section, and experience descriptions if you have them. Helps Claude preserve details or phrasing already on your profile that isn't on your resume.

**Target role or title** *(recommended)* — anchors your headline, About section, and skills list to what recruiters searching for this specific role actually type. Skipping this doesn't break anything, but the result will be more generic.

**Target industry** *(optional)* — sharpens the skills research and overall framing further.

**Management level** — Mid-level management, Upper-level management (Director+), or Executive (VP/C-suite). Calibrates tone and scope; an executive headline and About section genuinely read differently than a director-level one, even describing similar substance.

**Preferred custom URL text** *(optional)* — 5–30 characters. Leave blank and Claude suggests one from your name.

### What to generate

Seven independent checkboxes — check any combination for a given run:

1. **Headline** *(220 characters desktop / 240 mobile)* — but only roughly the first 70 characters show in search results and mobile previews, so the generated prompt explicitly instructs Claude to front-load the strongest role + value signal there, using the rest of the space for additional searchable keywords.

2. **About / Summary section** *(2,600 characters max)* — structured as:
   - **Paragraph 1** — who you are and what you do, written to grab a recruiter's attention. LinkedIn only shows roughly the first 200–300 characters before the "See more" cutoff, so this opening sentence has to work as a genuine hook on its own, not just a topic sentence.
   - **Paragraph 2** — how you help, why someone should want you — not just a restatement of your job title.
   - **Three bullets** — each supporting and expanding on how you deliver. A real number, dollar figure, or percentage leads each bullet *where one genuinely exists* in your background for that specific point. Where it doesn't, Claude writes a strong, specific qualitative bullet instead of inventing a metric.
   - **Contact line** — closes with how to reach you.

3. **Experience section rewrites** — how many positions to rewrite is a three-way choice: **3 most recent** (default), **All positions**, or a **Custom number** (reveals a number field, 1–20). "All positions" produces a longer response — worth it for a shorter work history, slower to generate for a long one. For each position rewritten: job title (100 characters, your real title plus a more current/searchable framing if one genuinely applies) and description (2,000 characters, opening with a short company/department blurb, then three bullets in the same real-number-or-strong-qualitative style as the About section).

4. **Skills section** *(80 characters per skill)* — not a static or generic "top skills" list. The generated prompt instructs Claude to research what recruiters, hiring managers, and ATS systems are actually searching for right now, specifically for your stated target role and industry — grounded in real current signal (live postings, category demand), not a list memorized from training. Skills are only included if something in your real background actually supports them.

5. **Custom Vanity URL** *(5–30 characters)* — uses your stated preference if you gave one, adjusting minimally if needed to fit the limit.

6. **Recommendation Request Guidance** *(off by default)* — this does **not** write recommendation text as if it came from someone else. Putting fabricated words in a real colleague's or manager's mouth isn't acceptable under any framing, full stop. Instead, this suggests 2–3 real types of people worth asking (a direct manager, a cross-functional peer, a direct report) and, for each, specific talking points grounded in your actual accomplishments that you could suggest they touch on — making their real recommendation more specific and useful than a generic "great to work with" note.

7. **Profile banner images** *(off by default)* — checking this reveals two more choices: **how many banners** (1–5, default 3) and a **visual style** — Let Claude decide (default), Abstract/geometric, Industry motif (e.g. a skyline, network, or circuit pattern, rendered abstractly rather than as a literal photo), or Minimalist. These are **programmatically generated** — geometric shapes, gradients, and line patterns built with Python's Pillow library, the same mechanism the LinkedIn Article Share Builder tool uses for its artwork, not an attempt at a photorealistic image or stock photo. This only works when you paste the prompt directly into Claude — it depends on Claude's own code execution capability and won't produce anything in a different AI tool.

### Output format

A separate choice from the checkboxes above: **Text in chat** (default) or **Downloadable Word document**. Word document requires the Code execution and file creation setting (Settings → Capabilities) and, like the banners, only works when run directly in Claude — pasting into another AI tool falls back to a chat response regardless of this choice. Banner images, if requested, always come through as separate `.png` files either way — a Word document can't hold them as editable images the way LinkedIn actually needs them uploaded.

## What you'll get back

A response organized by whichever sections you toggled on, each with its character count stated so you can confirm it fits before pasting into LinkedIn, formatted as either a chat response or a downloadable Word document per your Output Format choice above — plus separate banner image files, if requested, regardless of that choice.

## A note on honesty

Every section is bound by the same non-negotiable rule: nothing gets invented. No fabricated metric, title, employer, or credential — a strong qualitative bullet is always the correct substitute for a number that doesn't actually exist in your background. No fabricated recommendation text presented as someone else's words. No skill claimed as "the most in-demand" unless Claude can actually ground that in real, current research rather than reciting a memorized list.

If any generated content feels like it's stretching beyond what you actually gave Claude, push back on it directly in the conversation and ask for the specific evidence behind that claim.
