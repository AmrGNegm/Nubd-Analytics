# Daily Data Engineering Learning Routine

## Context (read first on every run)

I am Amr Negm — Senior Expert Data Analytics Engineer. I am building a free, 
public, end-to-end data engineering learning platform at:

  GitHub repo  : https://github.com/AmrGNegm/Learning-Data-Engineering
  Live site    : https://amrgnegm.github.io/Learning-Data-Engineering

The site uses a specific interactive HTML lab format we built together:
- Single standalone .html files per lab (no frameworks, no CDN)
- Light background for student labs, dark background for cheat sheets
- 3-tier interactive steps: Instructions → 💡 Hint (skeleton with blanks) 
  → ✅ Answer (collapsed by default)
- Knowledge check quizzes after major steps (multiple choice, instant feedback)
- Step checkboxes with a live progress bar in the lab header
- Completion card appears when all steps are checked off
- Bronze / Silver / Gold / Platinum medallion layer naming
- Naming convention: section_XX_labname.html

---

## Step 1 — Identify today's topic

Access https://roadmap.sh/data-engineer and identify one topic or skill gap 
not yet covered in the GitHub repo. Search the internet for all needed 
details, official documentation, and real-world use cases to fully understand 
the topic before writing anything.

Criteria for choosing the topic:
- Fills a gap in the existing roadmap coverage
- Has a practical, hands-on angle (not just theory)
- Can be taught in one 20–30 minute lab session
- Connects to real tools: Microsoft Fabric, Azure, PySpark, SQL, Power BI, dbt, etc.

---

## Step 2 — Build the lab files (follow this exact sequence)

### 2a. Plan the lab first
Before writing any code or HTML, define:
- Lab title and layer (Bronze / Silver / Gold / Platinum / Standalone)
- 3–5 learning objectives (what the student can DO after completing)
- The data source (free, public, no authentication)
- 4–6 code challenges students will solve themselves
- Real-life scenario that frames the whole lab

### 2b. Test ALL code before building HTML
Write every Python, PySpark, SQL, or DAX code block for this lab.
Run compile checks and logic assertions using available tools.
Fix all bugs found. List what was fixed and why.
Do NOT write any HTML until all code tests pass.

### 2c. Build the student lab HTML (section_XX_labname.html)
Build section by section — do not build everything at once.
Each section must follow the 3-tier format:

  TASK (always visible when step is expanded)
    ↓ student tries it first
  💡 HINT button → reveals skeleton code with _____ blanks
    ↓ if still stuck
  ✅ ANSWER button → reveals full tested solution (collapsed by default)
  
  After each major code step: add a knowledge check quiz.

HTML style rules:
- Background: #F0F4F8 | Cards: white, #E2E8F0 border, 12px radius
- Hint block: amber (#FFFBEB / #FDE68A)
- Answer block: purple (#F5F3FF / #C4B5FD), display:none by default
- Progress bar color: Bronze=#F59E0B, Silver=#94A3B8, Gold=#D97706, Platinum=#3B82F6
- All PySpark chains wrapped in outer ()
- DQ assertions before every Delta write
- Audit column _ingestion_ts on every table

### 2d. Build the instructor cheat sheet (section_XX_cheatsheet_name.html)
Dark background (#0F172A). All code copy-paste ready with Copy buttons.
Hint pills above each block: amber=warning, green=expected output, blue=tip.
Quick reference table at top. Common errors + fixes table at bottom.

### 2e. Update index.html
Add a new lab card following the exact same style as existing cards:
layer color top stripe, badge, icon, title, description, duration, tags, arrow.

### 2f. Update README.md
Add a new row to the workshop table:
| [Section X](filename.html) | Lab title | Duration |

---

## Step 3 — Create GitHub Pull Request

Create a pull request on https://github.com/AmrGNegm/Learning-Data-Engineering
with:

Title format:  "Add [Lab Title] — [key concepts covered]"

Description must include:
  - What topic this lab covers and why it was chosen from the roadmap
  - List of new files added
  - List of files updated (index.html, README.md)
  - Expected row counts / benchmark values students should see
  - Testing summary: what code was tested, what bugs were fixed
  - Link to the live GitHub Pages preview once merged:
    https://amrgnegm.github.io/Learning-Data-Engineering

Label the PR: enhancement · lab · [layer name]

---

## Step 4 — Write 2 LinkedIn posts

Write two versions of a LinkedIn post about today's topic.

### Post 1 — English (Easy Peasy Lemon Squeezy style)
- Hook in the first line (a question, surprising fact, or relatable pain point)
- Real-life scenario that non-technical people can understand
- Max 3 practical takeaways in a clean list
- Call to action: link to the live lab
- 3–5 relevant hashtags
- Tone: casual, energetic, a little fun — not corporate

### Post 2 — Egyptian Arabic accent
- Same structure as Post 1 but written in Egyptian colloquial Arabic
- Hook must land culturally — use a local analogy or relatable workplace scenario
- Keep technical terms in English (e.g. PySpark, Delta Lake, DAX)
- Tone: friendly, a bit witty, like explaining to a colleague over coffee

Store both posts in Notion:
- Database: "LinkedIn Posts — Data Engineering"
- Properties: Title, Date, Topic, Language (English / Arabic), Status (Draft), 
  Lab Link, Post Text
- Tag both posts with today's topic for easy historical lookup

---

## Step 5 — Send email to Gmail

Send one email summarising everything done today to amr.negm@gmail.com

Subject: [Daily DE Learning] [Topic Name] — PR + LinkedIn posts ready

Body must include:
  1. Topic covered today (1–2 sentences, why it matters)
  2. GitHub PR link to review
  3. Files changed (new lab + cheat sheet + index + README)
  4. English LinkedIn post (full text, ready to copy-paste)
  5. Arabic LinkedIn post (full text, ready to copy-paste)
  6. Live lab URL once merged:
     https://amrgnegm.github.io/Learning-Data-Engineering
  7. Suggested next topic from the roadmap (1 sentence)

---

## Quality rules — apply to every single run

□ Code must be tested before it goes into any HTML file
□ Answers are always collapsed (display:none) by default  
□ Hints show skeletons with blanks — never the full answer
□ Every lab has at least one knowledge check quiz with instant feedback
□ The cheat sheet is always a separate file from the student lab
□ index.html gets a new card every time
□ README.md gets a new row every time
□ PR description explains the testing done and any bugs fixed
□ LinkedIn posts must have a hook — no boring intros like "Today I learned..."
□ Notion entries must be tagged and searchable
□ Email must be ready to act on — no vague summaries
