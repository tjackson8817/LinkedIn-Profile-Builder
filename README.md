# LinkedIn Profile Builder

A free, browser-based tool that turns a form into a ready-to-paste prompt for Claude — the prompt asks Claude to optimize your LinkedIn profile specifically for a job search: headline, About section, experience descriptions, and up to 100 skills, all built around LinkedIn's real current character limits and grounded strictly in what's actually true about your background.

**No installation needed.** Open `prompt_builder.html` in any modern browser. Paste your resume (or attach it directly when you paste the prompt into Claude), fill in what applies, copy or download the generated prompt, and paste it into a Claude conversation to get the actual rewritten profile content. Nothing you enter is sent anywhere — this page only builds text locally in your browser.

## Who this is for

Built for mid-level and upper-level managers — Director, VP, and C-suite included — optimizing a LinkedIn profile specifically to be found and read by recruiters and hiring managers during an active job search. This is not a general "improve my LinkedIn presence" tool; every section is written with one job in mind: making a recruiter stop scrolling, a hiring manager see real fit, and an ATS/search index actually surface the profile in the first place.

It works as a **first step** in a job search: no job postings or even a settled target role are required. Leave the target role blank and Claude identifies the 2–3 roles your background most credibly supports, then builds the profile around them.

## Standalone tool

This isn't part of the JobRadar funnel (Target Company Prompt Builder, Job Posting Finder, and so on) — it's listed on the JobRadar hub page under "Also useful," alongside LinkedIn Article Share Builder and the Recruiter Message & Job Posting Sanity Check, since all three are things you'd use independent of where you are in an active application funnel, not steps in a fixed sequence.

## How it works

The page is a single form with two fieldsets:

1. **Your background** — paste your resume/professional background (required, unless you're attaching a file — see below), your current LinkedIn profile text (optional), your target role and industry (optional), tools/platforms/certifications you've used (optional), job postings you're aligned to (optional), your management level, your location and work arrangement (optional), and an optional preferred custom URL.
2. **What to generate** — eight independent checkboxes: Headline (1–5 options), About/Summary, Experience rewrites (adjustable count of positions), Skills (full 100-skill build or a focused list), Custom URL suggestion, Open to Work settings, Recommendation request guidance, and profile banner images (1–5, four styles).

The live output panel updates as you type. Copy the prompt or download it as a `.txt`, then paste it into a Claude conversation. A downloaded `.txt` can be loaded back into the form later with **Load .txt to edit**.

**Step 2 (100-skill build only):** the results end with numbered yes/no questions about skills you probably have but didn't document. Below the prompt, a **Copy follow-up prompt** card gives you a ready-made reply: fill in your answers, paste it into the same Claude conversation, and Claude adds every confirmed skill and regenerates the document.

## Attaching files instead of pasting text

You don't have to paste your resume or LinkedIn profile as text. Check **"I'll attach my resume and/or LinkedIn profile PDF directly to the Claude message"** and skip the text fields — Claude reads an attached file directly once you paste the prompt in and attach the file to that same message.

To get a PDF export of your current LinkedIn profile: open your profile → click **"More"** (just below your headline) → **"Save to PDF."**

## What the generated prompt asks for

1. **Headline** *(optional toggle, 1–5 options)* — each option takes a genuinely different angle (accomplishment-led, keyword-led, scope/seniority-led). Max 220 characters desktop / 240 mobile, with the strongest role + value signal front-loaded into the first ~70 characters, since that's roughly all that shows in search results and mobile previews.
2. **About / Summary section** *(optional toggle)* — max 2,600 characters, structured as two short paragraphs, three bullets, and a contact line. The opening sentence has to work as a hook before LinkedIn's "See more" cutoff.
3. **Experience section rewrites** *(optional toggle, adjustable count)* — job title (max 100 characters) and description (max 2,000 characters) for your most relevant/recent positions.
4. **Skills section** *(optional toggle, two modes)*:
   - **Full build — up to 100 skills** *(default; LinkedIn's maximum)* — ranked into four tiers (core role skills → supporting skills → proven tools/platforms/methods → search-coverage alternates and differentiators), with the demand signal, the evidence from your background, and which position or certification to attach each skill to. Also picks your Top 5 to feature, flags skills to remove from your current profile, lists gaps (with numbered yes/no questions, Q1, Q2…, when you likely have a skill but didn't document it), keeps your top 10 skills consistent across the headline/About/experience text, and ends with a copy-ready one-per-line list. It never pads: if your background honestly supports fewer than 100, it says how many slots remain and what would earn them.
   - **Focused list (15–25)** — the original, shorter skills section.
   
   Both modes research live demand for your target role. Pasted job postings are optional; when provided, Claude counts which skills recur across them and weights the list toward those. A generic reference pool is included only as a fallback for sessions with no live search.
5. **Custom Vanity URL** *(optional toggle)* — a suggestion within LinkedIn's 5–30 character limit.
6. **Open to Work settings** *(optional toggle, on by default)* — exactly what to enter under Open to → Finding a new job, which recruiters filter on directly: up to 5 job titles your background credibly supports, location types and locations (from your stated preference, or a flagged placeholder), start date and employment types, and a visibility recommendation ("Recruiters only" vs. "All LinkedIn members") with LinkedIn's caveat that a recruiters-only setting can't be guaranteed hidden from recruiters at your current employer.
7. **Recommendation Request Guidance** *(optional toggle, off by default)* — explicitly **not** ghostwritten recommendation text. Suggests who to ask and what real talking points to hand them.
8. **Profile banner images** *(optional toggle, off by default, 1–5 banners)* — programmatically generated `.png` files (Python's Pillow library via Claude's code execution, 1584×396px) — not photorealistic or stock images. Only works when the prompt is run directly in Claude.

## Important notes

- This tool **generates a prompt** — it does not itself call any AI model or produce any file.
- Every section instructs Claude to state its own character count.
- Nothing is invented. Every skill must trace to your resume, profile, or tools/certifications list; job postings count as demand signal only, never as evidence of what you've done.
- Every result comes back as a downloadable Word document — this requires the **Code execution and file creation** setting in Claude (Settings → Capabilities).
- Banner images, the Word document, and live skills research depend on Claude-specific capabilities — running this prompt in a different AI tool will still produce the text sections, but likely not those.

## Files in this repo

| File | Purpose |
| --- | --- |
| `index.html` | Redirects the bare repo URL straight to the tool |
| `prompt_builder.html` | The tool itself — open it in a browser |
| `Prompt_Builder_User_Guide.md` / `.docx` | Full user guide, same content in both formats |
| `sample_prompt.txt` | Example generated prompt (Director → VP, all positions, 2 banners) |
| `sample_output.md` / `.docx` | What Claude returns for `sample_prompt.txt` |
| `sample_prompt_100_skills.txt` | Example generated prompt using the current defaults: full 100-skill build with no job postings, plus Open to Work |
| `sample_output_100_skills.md` / `.docx` | What Claude returns for `sample_prompt_100_skills.txt` (41 honestly supported skills, 9 gap questions) |

## About

LinkedIn Profile Builder — a standalone job-search tool for optimizing a LinkedIn profile specifically to be found and read by recruiters and hiring managers, built around LinkedIn's real current character limits.
