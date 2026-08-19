# GCAP3226 — Week 2: GitHub, Codespaces & first plots

**Purpose:** Get every student **lab ready** before Week 3 (regression).  

By the end of Week 2 you should be **lab ready**: fork → Codespace → load `week2.csv` → make a plot.

---

## What you will learn

1. What a **repo** is and how to work in **your own copy** on GitHub.  
2. Use **Codespaces** (our online classroom computer).  
3. Load a **CSV from the course folder**.  
4. Make a **first plot** with Python; use **GitHub Copilot** if enabled — and **verify** the result (CILO4).

---

## What is in the Week 2 repo

| File | Session | Purpose |
|------|---------|---------|
| `W2_S1_github_lab_ready.ipynb` | 1 | Fork, Codespace, green-light |
| `W2_S2_data_visualization.ipynb` | 2 | Bar chart, histogram, scatter |
| `week2.csv` | 1–2 | Survey data for labs |
| `README.md` | — | This file |

---

## Start here: what is a **repo**?

**You do not need a computer science background.** We begin with one word you will hear every week:

### Repository (**repo**) — plain meaning

A **repo** is a **project folder on the internet** that holds everything for one assignment or one week:

- notebooks (`.ipynb`)
- data files (`.csv`)
- instructions (`README.md`)

Think of it like:

- a **shared Google Drive folder** for one group project, or  
- a **campaign asset folder** (brief, images, copy doc) that the whole team can open — except it lives on **GitHub** and is built for version control.

**This week’s repo** is named something like `gcap3226_week2`. Your instructor puts materials there; you open it through **your fork** (below).

### Then: GitHub, fork, Codespace

| Word | Plain meaning |
|------|----------------|
| **GitHub** | The website that **hosts** repos — like the platform behind the shared folder. |
| **Fork** | **Make your own copy** of the instructor’s repo under **your** GitHub account. You work on **your copy**; the instructor’s original stays unchanged. |
| **Codespace** | A **classroom computer in the browser** that already has your repo open — you run notebooks there. |
| **Save** (in the notebook) | Keeps your edits in this session (`File → Save`) — like saving a Word doc while it is open. |
| **Commit** | Save a **named snapshot** of your files **to GitHub** (e.g. “Finished Session 2”). |
| **Push** | **Upload** that snapshot from Codespaces to **your fork** online so it is stored in the cloud. |

**Analogies (PR / communications friendly)**

| Idea | Analogy |
|------|---------|
| **Repo** | One client’s project folder (all assets in one place). |
| **Fork** | Duplicate the folder into **your** drive; you edit your duplicate. |
| **Codespace** | A lab computer that already has the folder open — no USB, no “wrong Desktop path”. |
| **Commit + Push** | Save a version and upload to **your** cloud folder so work is not lost when class ends. |

| What you did | Enough for class? |
|--------------|-------------------|
| Ran cells, no **Save** | **No** — work may disappear. |
| **Saved** in Codespace | Good during class. |
| **Download** + Moodle upload | **Yes** — easiest submit (when graded). |
| **Commit + Push** to your fork | Optional backup; only if instructor asks for a GitHub link. |

---

## Session 1 setup — fork and Codespace

Do this in **Session 1** (or before Session 2 if you miss part of Session 1).

### Step 1 — GitHub account

Create a free account at [github.com](https://github.com) if you do not have one.

### Step 2 — Fork the instructor’s Week 2 repo

1. Open the link your instructor shares (e.g. `gcap3226_week2`).  
2. Click **Fork** (top right) → create under **your** username.  
3. Check the URL: `yourusername/gcap3226_week2` — **your** name must appear.

You now have **your own repo** — a copy of the course folder.

### Step 3 — Start a Codespace from **your fork**

1. Open **your fork** (not only the instructor’s page).  
2. Click green **Code** → tab **Codespaces** → **Create codespace on main**.  
3. Wait for VS Code in the browser (about 1–3 minutes the first time).

### Step 4 — Open Session 1 notebook

1. Open `W2_S1_github_lab_ready.ipynb`.  
2. When asked, select kernel **Python 3** (see Session 1 slides — kernel / “restaurant” analogy).  
   - In **Codespace**, choose the interpreter at **`/usr/local/bin/python`** (often labelled **Python 3.x.x**).  
   - **Do not** use the **Colab** kernel for this course — it cannot see repo files and may miss libraries.  
3. Run cells from top to bottom.

### Step 5 — Green-light check (lab ready)

You are **lab ready** when you can:

- `import pandas` and `matplotlib` without error  
- Load `week2.csv` and see `shape`  
- Display at least **one plot**

If you see `FileNotFoundError`: the CSV must come from **the repo in Codespace** — do not paste a path from your laptop.

### Step 6 — GitHub Copilot (if enabled)

Sign in to Copilot in Codespaces. After it suggests code: **run** → **read output** → **edit or reject** if wrong.

---

## Session 2 — data visualization notebook

1. In the **same Codespace** (from **your fork**), open `W2_S2_data_visualization.ipynb`.  
2. Run tasks: support bar chart → distance histogram → scatter → save one figure.  
3. Survey question wording is on the **slides**; column names are in the notebook.  
4. **Save** when you finish (`File → Save`).

---

## Session 3 — co-instructor

Session 3 is led by the **co-instructor**. It may cover how to **read and communicate** data (e.g. survey context, charts as messages, course collaboration tools).  

Use the **slides and Moodle post for Session 3** — not only this README. You still need your **fork + Codespace** set up from Session 1.

---

## Optional — Commit and Push (backup on GitHub)

Not required for most Week 2 work.

1. **Save** the notebook.  
2. **Source Control** (branch icon, left sidebar) → **+** to stage your file.  
3. Write a message → **Commit** → **Sync / Push**.  
4. Refresh **your fork** on github.com.

You only push to **your fork**, never the instructor’s original repo.

---

## How to submit (if a Week 2 task is graded)

**Recommended — Moodle**

1. **Save** the notebook.  
2. Right-click the file in Codespaces → **Download…**  
3. Upload to Moodle.

No commit or push required.

---

## Troubleshooting

| Problem | What to do |
|---------|------------|
| “What is a repo?” | One **online project folder** on GitHub — see [Start here](#start-here-what-is-a-repo) above |
| `.ipynb` looks like JSON on GitHub | Open in **Codespaces**, not as raw text on the website |
| `FileNotFoundError` for CSV | Codespace from **your fork**; file must be inside the repo |
| `ModuleNotFoundError: pandas` (or matplotlib) | Wait until Codespace **finishes building** (check terminal for `postCreateCommand`). Then in the Codespace terminal run: `pip install -r requirements.txt` → **Restart kernel** → run import again. |
| Import error **not** `ModuleNotFoundError` (e.g. ipykernel, connection failed, SSL) | See **Kernel / import errors** below |
| Using **Colab kernel** in Cursor/VS Code | Switch kernel to **local/Codespace Python 3**, not Colab — or open the notebook **inside Codespaces** in the browser |
| Opened instructor’s repo by mistake | Open **your fork** (`yourusername/gcap3226_week2`) and create Codespace there |
| Missed Session 1 | Complete Session 1 steps before Session 2 |

### Kernel / import errors (not ModuleNotFoundError)

1. **Confirm where you are running**  
   - **Intended:** GitHub → your fork → **Codespaces** → open notebook.  
   - **Problem setups:** Colab kernel, or local Python without course packages.

2. **Pick the right kernel**  
   - Top right of notebook → **Select Kernel** → **Python Environments** → **`/usr/local/bin/python`** (Codespace).  
   - Avoid kernels named **Colab**, **base (conda)** on your laptop unless you installed packages there.

3. **Install packages manually (Codespace terminal)**  
   ```bash
   pip install -r requirements.txt
   ```  
   Then: **Kernel → Restart Kernel** → run `import pandas` again.

4. **Still failing?** Copy the **full red error message** (first line matters) and ask your instructor or TA.

---

## Next week (Week 3)

Fork the **Week 3 repo** → Codespace → regression notebooks.  
Week 3 assumes you already know **repo, fork, and Codespace** — it will not re-teach from scratch.
