# LinkedIn Profile Builder

A free, browser-based tool that turns a form into a ready-to-paste prompt for Claude — the prompt asks Claude to optimize your LinkedIn profile specifically for a job search: headline, About section, experience descriptions, and skills, all built around LinkedIn's real current character limits and grounded strictly in what's actually true about your background.

**No installation needed.** Open `prompt_builder.html` in any modern browser. Paste your resume (or attach it directly when you paste the prompt into Claude), fill in what applies, copy or download the generated prompt, and paste it into a Claude conversation to get the actual rewritten profile content. Nothing you enter is sent anywhere — this page only builds text locally in your browser.

## Who this is for

Built for mid-level and upper-level managers — Director, VP, and C-suite included — optimizing a LinkedIn profile specifically to be found and read by recruiters and hiring managers during an active job search. This is not a general "improve my LinkedIn presence" tool; every section is written with one job in mind: making a recruiter stop scrolling, a hiring manager see real fit, and an ATS/search index actually surface the profile in the first place.

## Standalone tool

This isn't part of the JobRadar funnel (Target Company Prompt Builder, Job Posting Finder, and so on) — it's listed on the JobRadar hub page under "Also useful," alongside LinkedIn Article Share Builder and the Recruiter Message & Job Posting Sanity Check, since all three are things you'd use independent of where you are in an active application funnel, not steps in a fixed sequence.

## How it works

The page is a single form with two fieldsets:

1. **Your background** — paste your resume/professional background (required, unless you're attaching a file — see below), your current LinkedIn profile text (optional, helps preserve your existing voice), your target role and industry, your management level, and an optional preferred custom URL.
2. **What to generate** — seven independent checkboxes: Headline, About/Summary, Experience rewrites (with an adjustable count of positions), Skills, Custom URL suggestion, Recommendation request guidance, and three profile banner images.

The live output panel updates as you type. Copy the prompt or download it as a `.txt`, then paste it into a Claude conversation.

## Attaching files instead of pasting text

You don't have to paste your resume or LinkedIn profile as text. Check **"I'll attach my resume and/or LinkedIn profile PDF directly to the Claude message"** and skip the text fields — Claude reads an attached file directly once you paste the prompt in and attach the file to that same message.

To get a PDF export of your current LinkedIn profile: open your profile → click **"More"** (just below your headline) → **"Save to PDF."**

## What the generated prompt asks for

1. **Headline** *(optional toggle)* — max 220 characters desktop / 240 mobile, with an explicit instruction to front-load the strongest role + value signal into the first ~70 characters, since that's roughly all that shows in search results and mobile previews.
2. **About / Summary section** *(optional toggle)* — max 2,600 characters, structured as two short paragraphs, three bullets, and a contact line. The prompt flags that LinkedIn only shows roughly the first 200–300 characters before the "See more" cutoff, so the opening sentence has to work as a real hook on its own.
3. **Experience section rewrites** *(optional toggle, adjustable count)* — job title (max 100 characters) and description (max 2,000 characters) for your most relevant/recent positions, each following the same paragraph-plus-bullets structure as the About section.
4. **Skills section** *(optional toggle)* — not a static "top skills" list. The prompt instructs Claude to research what's actually in current demand for your specific target role and industry (real job postings, category data), and to only list a skill if something in your real background actually supports it.
5. **Custom Vanity URL** *(optional toggle)* — a suggestion within LinkedIn's 5–30 character limit, using your stated preference if you gave one.
6. **Recommendation Request Guidance** *(optional toggle, off by default)* — explicitly **not** ghostwritten recommendation text. Suggests who to ask and what real talking points to hand them, since writing words and presenting them as if a real colleague said them would be a fabrication problem, not a writing-quality one.
7. **Three profile banner images** *(optional toggle, off by default)* — three distinct `.png` banners via Claude's own image-generation capability. Only works when the prompt is run directly in Claude, not other AI tools.

## Important notes

- This tool **generates a prompt** — it does not itself call any AI model or produce any file. You paste the output into a separate Claude conversation to get the actual rewritten content.
- Every section instructs Claude to state its own character count, so you can confirm it fits LinkedIn's real limit before pasting it in.
- Nothing is invented. Quantify only where a real number, dollar figure, or percentage genuinely exists in your background — a strong qualitative bullet is always the correct substitute for a fabricated metric, never the other way around.
- Banner image generation and the skills-research step both depend on capabilities specific to Claude — running this prompt in a different AI tool will still produce the text sections, but likely not those two.

## Files in this repo

| File | Purpose |
| --- | --- |
| `index.html` | Redirects the bare repo URL straight to the tool |
| `prompt_builder.html` | The tool itself — open it in a browser |
| `Prompt_Builder_User_Guide.md` / `.docx` | Full user guide, same content in both formats |
| `sample_prompt.txt` | Real example of the generated prompt, filled in with a sample background |

## About

LinkedIn Profile Builder — a standalone job-search tool for optimizing a LinkedIn profile specifically to be found and read by recruiters and hiring managers, built around LinkedIn's real current character limits.
