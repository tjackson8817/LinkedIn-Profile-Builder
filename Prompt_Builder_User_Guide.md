# LinkedIn Profile Builder — User Guide

## What this tool is for

Optimizes your LinkedIn profile specifically for a job search — not general networking content, not "polish my presence." Every section is written to be genuinely impactful to three audiences at once: a recruiter scanning quickly, a hiring manager evaluating fit, and LinkedIn's own (and any employer's) ATS/search indexing — while still reading as a real, specific person instead of a keyword-stuffed template.

Built for mid-level and upper-level management specifically, regardless of industry or function — Director, VP, and C-suite included.

This is a standalone tool, not part of the JobRadar funnel. It's listed on the JobRadar hub page under "Also useful," since it's something you'd reach for independent of where you are in an active application process.

## Before you start

Have ready:

- Your resume, or a detailed written summary of your career (or plan to attach the file directly — see below)
- Your current LinkedIn profile text, if you want Claude to preserve existing phrasing or details not on your resume (optional)
- A target role and industry, if you know them — sharpens the headline, About section, and skills list considerably. Not sure yet? That's fine; this tool works as the first step in a search.
- A list of tools, platforms, certifications, and methods you've used (optional) — the fastest honest way to fill out a 100-skill list
- Job postings you're aligned to (optional) — not needed, but they sharpen the skills ranking if you have them

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

**Target role or title** *(recommended)* — anchors your headline, About section, and skills list to what recruiters searching for this specific role actually type. If you leave it blank, the prompt tells Claude to first identify the 2–3 role titles your background most credibly supports, list them at the top of the document with a line on why each fits, and build every section around them.

**Target industry** *(optional)* — sharpens the skills research and overall framing further.

**Tools, platforms, certifications & methods you've used** *(optional)* — software, systems, certifications, standards, and methodologies you've genuinely used that your resume doesn't spell out (e.g. SAP, Power BI, PMP, Lean Six Sigma). Resumes usually leave these out, and they're exactly what recruiters filter on. Claude treats this list as evidence, the same as your resume.

**Job postings you're aligned to** *(optional)* — paste one or more full postings, separated by a line of dashes (`---`). Skip it if you're just starting out; Claude researches current demand for your target role either way. When you do add postings, Claude counts which skills recur across them and weights your skills and keywords toward what those employers ask for. Five or more gives the strongest signal. Postings are treated as demand signal only — never as evidence that you've done something.

**Management level** — Mid-level management, Upper-level management (Director+), or Executive (VP/C-suite). Calibrates tone and scope; an executive headline and About section genuinely read differently than a director-level one, even describing similar substance.

**Location & work arrangement** *(optional)* — where you want to work and how (e.g. "Dallas–Fort Worth, hybrid or remote"). Used for the Open to Work settings. Leave it blank and Claude flags the location fields for you to fill in rather than guessing.

**Preferred custom URL text** *(optional)* — 5–30 characters. Leave blank and Claude suggests one from your name.

### What to generate

Eight independent checkboxes — check any combination for a given run:

1. **Headline** *(220 characters desktop / 240 mobile, up to 5 options)* — choose how many distinct headline options to generate (1–5, default 3). Each option takes a genuinely different angle — one led by a specific accomplishment/number, one led by role + target keywords, one led by scope/seniority — rather than minor rewordings of the same line, so you're actually choosing between approaches, not just wording. Only roughly the first 70 characters show in search results and mobile previews, so the generated prompt explicitly instructs Claude to front-load the strongest role + value signal there in every option, using the rest of the space for additional searchable keywords. Each option states its own character count.

2. **About / Summary section** *(2,600 characters max)* — structured as:
   - **Paragraph 1** — who you are and what you do, written to grab a recruiter's attention. LinkedIn only shows roughly the first 200–300 characters before the "See more" cutoff, so this opening sentence has to work as a genuine hook on its own, not just a topic sentence.
   - **Paragraph 2** — how you help, why someone should want you — not just a restatement of your job title.
   - **Three bullets** — each supporting and expanding on how you deliver. A real number, dollar figure, or percentage leads each bullet *where one genuinely exists* in your background for that specific point. Where it doesn't, Claude writes a strong, specific qualitative bullet instead of inventing a metric.
   - **Contact line** — closes with how to reach you.

3. **Experience section rewrites** — how many positions to rewrite is a three-way choice: **3 most recent** (default), **All positions**, or a **Custom number** (reveals a number field, 1–20). "All positions" produces a longer response — worth it for a shorter work history, slower to generate for a long one. For each position rewritten: job title (100 characters, your real title plus a more current/searchable framing if one genuinely applies) and description (2,000 characters, opening with a short company/department blurb, then three bullets in the same real-number-or-strong-qualitative style as the About section).

4. **Skills section** *(80 characters per skill)* — not a static or generic "top skills" list. The generated prompt instructs Claude to research what recruiters, hiring managers, and ATS systems are actually searching for right now, specifically for your target role and industry — grounded in real current signal (live postings, category demand, and any postings you pasted), not a list memorized from training. Skills are only included if something in your real background actually supports them. Choose one of two modes:

   **Full build — up to 100 skills** *(default)*. LinkedIn allows up to 100 skills, and recruiters filter searches by them, so more honest coverage means more searches you can show up in. Claude returns:
   - A ranked table: # · Skill · Tier · Demand signal (High / Medium / Niche, plus how many of your postings mention it if you pasted any) · Evidence from your background · Which position, education entry, or certification to attach it to on LinkedIn
   - Four tiers: **Tier 1** (about the top 25) core skills for your target role with strong evidence; **Tier 2** (26–60) supporting skills; **Tier 3** (61–85) specific tools, platforms, systems, standards, and methods you've used; **Tier 4** (86–100) legitimate alternate names recruiters also search for, plus differentiators
   - Your **Top 5** skills to feature, with a line on why
   - **Skills to remove** from your current profile (when you provided it) — outdated, generic, or off-target
   - **Gaps** — in-demand skills you don't show. Where you probably have the skill but didn't document it, Claude asks a numbered yes/no question (Q1, Q2…); where it's a real gap, it suggests the fastest credible way to close it
   - **Keyword consistency** — your top 10 skills woven into the headline, About, and experience text written in the same run
   - A **copy-ready list**, one skill per line in the order to add them

   Claude never pads to reach 100. If your background honestly supports fewer, it stops, says how many slots remain, and tells you what you'd need to document to earn them. Entering 100 skills by hand takes a while — add Tiers 1 and 2 first, since they carry the most search value, and fill in Tiers 3 and 4 over the following week or two.

   **Step 2: answer the gap questions.** When the full build is selected, a **Copy follow-up prompt** card appears below the generated prompt. After you've read your results, copy it, fill in a yes or no (plus one line of detail for each yes) beside each Q number, and send it in the **same** Claude conversation. Claude adds every confirmed skill in the right tier, drops nothing you said no to, keeps the total at 100 or fewer, updates the Headline and About if a new skill lands in your top 10, and regenerates the Word document with new skills marked (NEW). For most people this is where the list grows the most, since resumes leave out a lot of what people actually do.

   **Focused list (15–25)**. The shorter, original skills section, for when you just want the essentials.

   **Fallback reference pool.** Live research is always the primary source and should be used whenever it's available. But if you paste the generated prompt into a session or tool with no live web search access, the prompt includes a 100-skill generic reference pool (spanning leadership, strategy/operations, project management, data/analytics, digital/technical, sales, marketing, HR, finance, industry-specific operations, communication, and innovation) at the very end, for Claude to fall back on. This pool is deliberately generic across management functions and industries — it's a last-resort net, not a substitute for targeted research, and Claude is instructed to still filter it down to only what's genuinely supported by your background, and to say plainly if it had to use the fallback instead of live search.

5. **Custom Vanity URL** *(5–30 characters)* — uses your stated preference if you gave one, adjusting minimally if needed to fit the limit.

6. **Open to Work settings** *(on by default)* — exactly what to enter under your profile's **Open to → Finding a new job** preferences, which recruiters filter on directly:
   - **Job titles** (up to 5) — your target title plus the close, common variants employers actually post under, limited to titles your background credibly supports
   - **Location types and locations** — on-site, hybrid, or remote, based on your Location & work arrangement field (or a flagged placeholder if you left it blank)
   - **Start date and employment types** — sensible defaults for you to adjust
   - **Visibility** — the trade-off between "Recruiters only" and "All LinkedIn members" (which adds the green #OpenToWork photo frame) for someone at your level, with a recommendation and reasoning. Claude also passes on LinkedIn's own caveat: it tries to hide a recruiters-only setting from recruiters at your current company, but can't guarantee it.

7. **Recommendation Request Guidance** *(off by default)* — this does **not** write recommendation text as if it came from someone else. Putting fabricated words in a real colleague's or manager's mouth isn't acceptable under any framing, full stop. Instead, this suggests 2–3 real types of people worth asking (a direct manager, a cross-functional peer, a direct report) and, for each, specific talking points grounded in your actual accomplishments that you could suggest they touch on — making their real recommendation more specific and useful than a generic "great to work with" note.

8. **Profile banner images** *(off by default)* — checking this reveals two more choices: **how many banners** (1–5, default 3) and a **visual style** — Let Claude decide (default), Abstract/geometric, Industry motif (e.g. a skyline, network, or circuit pattern, rendered abstractly rather than as a literal photo), or Minimalist. These are **programmatically generated** — geometric shapes, gradients, and line patterns built with Python's Pillow library, the same mechanism the LinkedIn Article Share Builder tool uses for its artwork, not an attempt at a photorealistic image or stock photo. This only works when you paste the prompt directly into Claude — it depends on Claude's own code execution capability and won't produce anything in a different AI tool.

### Output

Every result always comes back as a **downloadable Word document (.docx)** — there's no chat-text option anymore. This requires the Code execution and file creation setting (Settings → Capabilities) and, like the banners, only works when run directly in Claude — pasting into another AI tool falls back to a chat response regardless. Banner images, if requested, always come through as separate `.png` files alongside it — a Word document can't hold them as editable images the way LinkedIn actually needs them uploaded.

## What you'll get back

A response organized by whichever sections you toggled on, each with its character count stated so you can confirm it fits before pasting into LinkedIn, formatted as a downloadable Word document — plus separate banner image files, if requested.

## A note on honesty

Every section is bound by the same non-negotiable rule: nothing gets invented. No fabricated metric, title, employer, or credential — a strong qualitative bullet is always the correct substitute for a number that doesn't actually exist in your background. No fabricated recommendation text presented as someone else's words. No skill added to your list just because a job posting asks for it — postings show demand, your background provides the evidence. No skill claimed as "the most in-demand" unless Claude can actually ground that in real, current research rather than reciting a memorized list.

If any generated content feels like it's stretching beyond what you actually gave Claude, push back on it directly in the conversation and ask for the specific evidence behind that claim.
