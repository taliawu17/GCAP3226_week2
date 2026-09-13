# Copilot for documents

**Purpose:** practise steering an AI agent on a real public document, then verifying the output.  

**Tool:** GitHub Copilot in Codespaces only  
**Input (already in the repo):** `W2_S3_text_summary/policy-full_en.pdf`  
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



## 2. Prompt-writing tips — then write your own prompts

Use these **four principles**. Then **modify the example prompts** below.

1. **Define the role clearly**
  Say who Copilot should act as, and who the page is for. If you know the goal but not the details, tell it to **ask you questions one by one**, and to **say why** each question matters, until your intention is clear enough to start.
2. **Use input–process–output to define the task**
  - **Input:** which file (`W2_S3_text_summary/policy-full_en.pdf/policy-full_en.pdf`), not general knowledge. 
  - **Process:** what to do (e.g. start from Contents; group priorities by theme; do not invent). 
  - **Output:** what to build (here: one simple interactive HTML page you can open and check).
3. **Verification instruction**
  Tell Copilot what to do when unsure: flag the gap and **prefer asking back over guessing**.
4. **After the first answer**
  Open the page, check 2–3 bullets in the PDF, then send a short follow-up: remove, rewrite, or add a chapter cue.



### Example prompts

**If you are not ready to specify everything yet:**

> I want a simple interactive HTML summary of `/W2_S3_text_summary` for a GE student. Before you build, ask me questions **one by one**, and say **why** you are asking each question, until my intention is clear enough.

**First build prompt:**
>
> **Input:** use only `policy-full_en.pdf`. Start from the Contents / chapter titles. Do not use general knowledge about Hong Kong.
>
> **Process:** summarise policy priorities by theme. Each bullet must be checkable against the PDF. Do not invent measures that are not in the Contents or the sections I name.
>
> **Output:** one interactive HTML file at `output/policy_priorities.html` — tabs or buttons by theme; 3–6 bullets per theme; each bullet with a chapter or section cue; a search box; a footer caution (summary only; not official advice). Plain HTML + CSS + a little JS is enough.
>
> If anything is unclear, ask me back and say why. Prefer asking back over guessing.

**After the first answer:**

> I cannot find this bullet in the PDF: “[paste the sentence]”. Remove it or rewrite it using only the PDF, and add a chapter cue.

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

