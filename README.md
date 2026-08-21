# GCAP3226 — Week 2: GitHub, Codespaces & first plots

**Purpose:** Get every student **lab ready** before Week 3.  

By the end of Week 2 you should be **lab ready**: fork → Codespace → load `week2.csv` → make a plot.

---

## What you will learn

1. What a **repo** is and how to work in **your own copy** on GitHub.  
2. Use **Codespaces** (our online classroom computer).  
3. Load a **CSV from the course folder**.  
4. Make a **first plot** with Python; use **GitHub Copilot** if enabled — and **verify** the result (CILO4).



## Start here: what is a **repo**?

### Repository (**repo**) — plain meaning

A **repo** is a **project folder on the internet** that holds everything for one assignment or one week:

- notebooks (`.ipynb`)
- data files (`.csv`)
- instructions (`README.md`)

**This week’s repo** is named as `gcap3226_week2`. Your instructor puts materials there; you open it through **your fork** (below).

### Then: GitHub, fork, Codespace

| Word | Plain meaning |
|------|----------------|
| **GitHub** | The website that **hosts** repos — like the platform behind the shared folder. |
| **Fork** (verb) | Click **Fork** to **make your own copy** of the instructor’s repo under **your** GitHub account. |
| **Fork** (noun) | **Your fork** = **your own copy of the course folder** on github.com. You work there; the instructor’s original stays unchanged. |
| **Codespace** | A **classroom computer in the browser** that already has your repo open — you run notebooks there. |
| **Save** (in the notebook) | Keeps your edits on the **Codespace** while it is open (`File → Save`) — like saving a Word doc on the classroom computer you are using. |
| **Commit** | **Stamp this version on the Codespace** — a named snapshot in Git history (e.g. “Finished Week 2 plots”). Still on the Codespace until you Push. |
| **Push** | **Send those stamped versions to your fork (your own copy of the course folder) on github.com** so they are stored online. |


**Analogies**

| Idea | Analogy |
|------|---------|
| **Repo** | One client’s project folder (all assets in one place). |
| **Fork** | Duplicate the folder into **your** drive; you edit your duplicate. |
| **Codespace** | A lab computer that already has the folder open — no USB, no “wrong Desktop path”. |
| **Save** | Save the file on that lab computer. |
| **Commit** | Stamp a named version **on the Codespace** (not yet on github.com). |
| **Push** | Send those stamped versions to **your fork (your own copy of the course folder) on github.com**. |


---

## Class 1 — fork and Codespace

### Step 1 — GitHub account

You should already have a GitHub account from **Week 1** (register, turn on **2FA**, apply for **GitHub Education**).

If you do not have an account yet, create one now at [github.com](https://github.com), then continue.

### Step 2 — Fork the instructor’s Week 2 repo

1. Open the link your instructor shares (e.g. `gcap3226_week2`).  
2. Click **Fork** (top right) → create under **your** username.  
3. Check the URL: `yourusername/gcap3226_week2` — **your** name must appear.

You now have **your own repo** — a copy of the course folder.

### Step 3 — Start a Codespace from **your fork**

1. Open **your fork** (not only the instructor’s page).  
2. Click green **Code** → tab **Codespaces** → **Create codespace on main**.  
3. Wait for VS Code in the browser (about 1–3 minutes the first time).

### Step 4 — Open Class 1 notebook

1. Open `W2_S1_github_lab_ready.ipynb`.  
2. When asked, select kernel **Python 3** .  
   - In **Codespace**, choose the interpreter at **`/usr/local/bin/python`** (often labelled **Python 3.x.x**).  
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

## Class 2 — data visualization notebook

1. In the **same Codespace** (from **your fork**), open `W2_S2_data_visualization.ipynb`.  
2. Run tasks: support bar chart → distance histogram → scatter → save one figure.  
3. Survey question wording is on the **slides**; column names are in the notebook.  
4. **Save** when you finish (`File → Save`).

---

## Troubleshooting

| Problem | What to do |
|---------|------------|
| `.ipynb` looks like JSON on GitHub | Open in **Codespaces**, not as raw text on the website |
| `FileNotFoundError` for CSV | Codespace from **your fork**; file must be inside the repo |
| `ModuleNotFoundError: pandas` (or matplotlib) | Wait until Codespace **finishes building** (check terminal for `postCreateCommand`). Then in the Codespace terminal run: `pip install -r requirements.txt` → **Restart kernel** → run import again. |
| Import error **not** `ModuleNotFoundError` (e.g. ipykernel, connection failed, SSL) | See **Kernel / import errors** below |
| Opened instructor’s repo by mistake | Open **your fork** (`yourusername/gcap3226_week2`) and create Codespace there |

### Kernel / import errors (not ModuleNotFoundError)

1. **Confirm where you are running**  
   - **Intended:** GitHub → your fork → **Codespaces** → open notebook.  
   - **Problem setups:** Colab kernel, or local Python without course packages.

2. **Pick the right kernel**  
   - Top right of notebook → **Select Kernel** → **Python Environments** → **`/usr/local/bin/python`** (Codespace).  
   - Avoid kernels named **Colab**, **base (conda)** on your laptop.

3. **Install packages manually (Codespace terminal)**  
   ```bash
   pip install -r requirements.txt
   ```  
   Then: **Kernel → Restart Kernel** → run `import pandas` again.

4. **Still failing?** Copy the **full red error message** (first line matters) and ask your instructor or TA.


---

## Optional — Commit and Push (backup on GitHub)

Not required for most Week 2 work.

Remember: **Commit** = stamp this version on the Codespace; **Push** = send those stamped versions to your fork (your own copy of the course folder) on github.com. Commit alone does **not** update the GitHub website.

1. **Save** the notebook.  
2. **Source Control** (branch icon, left sidebar) → **+** to stage your file.  
3. Write a message → **Commit** (stamp on Codespace) → **Sync / Push** (send to github.com).  
4. Refresh **your fork** on github.com — you should see the update only after Push.

You only push to **your fork**, never the instructor’s original repo.
---

## Next week (Week 3)

Fork the **Week 3 repo** → Codespace → regression notebooks.  
Week 3 assumes you already know **repo, fork, and Codespace** — it will not re-teach from scratch.
