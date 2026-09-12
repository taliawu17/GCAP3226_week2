# Copilot for documents

**Purpose:** practise steering an AI agent on a real public document, then verifying the product — not producing a perfect Policy Address summary.  

**Tool:** GitHub Copilot in Codespaces only  
**Input (already in the repo):** `docs/policy-full_en.pdf`  
**Document:** *The Chief Executive’s 2025 Policy Address* — *Deepening Reforms for Our People; Leveraging Our Strengths for a Brighter Future* (public copy for class use; check the PDF cover for the official source)  
**Output:** one simple **interactive HTML** page that summarises **policy priorities** (by theme), with sources you can check  
**Not graded** — practice for CILO4: think → check → verify  

---

## 0. What an AI agent (here: Copilot) can do

In this lab, GitHub Copilot is not only a **chatbot** that answers in words. In Codespaces it can act more like an **agent**: it takes your request, uses files in the repo (e.g. the PDF), and **creates or edits files** for you — such as writing a full `.html` page you can open and click.

1. **You ask → it can build.**
  Example: ask it to summarise the Policy Address Contents **and** produce an interactive HTML file. It can draft the page (tabs, search, bullets) into your workspace, not only paste a short reply in the chat.
2. **Still controlled by your prompt.**
  Clear instructions (which file, what structure, what to avoid inventing) shape what it builds. Vague prompts → vague or wrong pages.
3. **Fluent work ≠ correct work.**
  A polished HTML page can still **misstate** or **invent** priorities that are not in the PDF. That is why you **verify** against the document (think → check → verify).
4. **It may not “see” the whole PDF.**
  A long Address can overwhelm context. Steer it to **Contents / named chapters**, and ask for **section cues** so you can spot-check.
5. **Building is iterative.**
  Expect several rounds (draft → open the page → check the PDF → ask for fixes). Do **not** expect an ideal page after only 1–2 chats. Use §3 “good enough” to know when to stop.

---

## 1. Class steps

1. Open `docs/policy-full_en.pdf`. Skim the **Contents** (chapter list).
2. In Copilot Chat (Codespaces), ask it to **read the Contents** and list main themes.
3. Ask it to build a **simple interactive HTML** summary (tabs or buttons by theme).
4. **Verify:** open 2–3 claims in the HTML; find them in the PDF; fix or delete overclaims.
5. Save `output/policy_priorities.html` in your fork (optional Commit/Push for practice).

---

## 2. Prompt-writing tips - then write your own prompts

Consider these **points** when you write prompts.

**A. Role + task**  
Say what you want: e.g. *read this PDF’s Contents; summarise policy priorities for a GE student.*

**B. Point to the file**  
Name the path: `docs/policy-full_en.pdf`. Ask Copilot to use **that** file (not “general knowledge about Hong Kong”).

**C. Scope for a long PDF**  
Start with **Contents / chapter titles**, then optionally **one chapter**. Say: *Do not invent measures that are not in the Contents or the sections I name.*

**D. Output shape**  
Ask for: themes as tabs/sections; 3–6 bullets each; each bullet with a **chapter or paragraph cue** for checking; footer caution (not official advice; summary only).

**E. Interactive HTML**  
Ask for a single `.html` file with simple buttons/tabs and a **search box** (plain HTML + CSS + a little JS is enough). No need for a server.

**F. Verification instruction**  
Add: *Flag any point you are unsure about; prefer omission over guessing.*

**G. After the first answer**  
Second prompt: *Here is a bullet I cannot find in the PDF — remove or rewrite it:* …

---

## 3. What “good enough” looks like

- HTML opens in the browser (Preview / Open).  
- At least **4 themes**, each with a few bullets.  
- Bullets look checkable (chapter / section named).  
- A clear caution: a summary of a public document; **not** government advice; do not overclaim.

---

## 4. Safety / academic honesty

- Use the **provided PDF copy** in the repo (no scraping in this class).  
- Do not treat Copilot’s summary as the Policy Address itself.  
- If you use this later in coursework, keep the **verify** habit and cite the official Address.

