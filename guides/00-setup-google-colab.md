# Guide 00 · Setting up Google Colab (and meeting its AI assistant)

Google Colab ("Colaboratory") is a free website from Google where you can write and run Python in your browser. Nothing is installed on your computer: your code runs on a Google computer in the cloud, and your notebooks are saved in your Google Drive.

We use Colab for the whole course because:

- it is **free** and works on any computer with a modern browser (Chrome, Edge, Firefox, Safari);
- popular data libraries (pandas, seaborn, Plotly, SciPy…) are **already installed**;
- your work is **saved to Google Drive** and easy to share with your facilitator;
- it has a built-in **AI assistant** (Gemini) that we will learn to use responsibly.

---

## Step 1 · Get a Google account

If you already use Gmail, you have a Google account. Skip to Step 2.

1. Go to <https://accounts.google.com/signup>.
2. Fill in your name, choose a username and a strong password.
3. Add a phone number for recovery (recommended, so you never get locked out).

> **Tip:** Use a personal account rather than a work or school account. Some organisations block Colab or its AI features.

## Step 2 · Open Colab

1. Go to <https://colab.research.google.com>.
2. Sign in with your Google account (top-right corner).
3. A window titled **"Open notebook"** appears. Click **"+ New notebook"** (bottom of the window).

You now have an empty notebook called something like `Untitled0.ipynb`.

4. Click the name at the top-left and rename it to `session1-first-program.ipynb`.

## Step 3 · Tour of the Colab screen

```
┌────────────────────────────────────────────────────────────────────────────┐
│ CO  session1-first-program.ipynb   ☆           [Share]  [Gemini ✦]  (You) │  ← title bar
│ File Edit View Insert Runtime Tools Help                                   │  ← menus
├────┬───────────────────────────────────────────────────────────────────────┤
│ ☰  │ + Code   + Text                                    RAM ▮▮▯ Disk ▮▯▯   │  ← toolbar + connection
│ 🔍 │ ┌───────────────────────────────────────────────────────────────────┐ │
│ {x}│ │ ▶ │ print("Hello, Kenya!")                                        │ │  ← a CODE cell
│ 🔑 │ └───────────────────────────────────────────────────────────────────┘ │
│ 📁 │     Hello, Kenya!                                                     │  ← its OUTPUT
│    │ ┌───────────────────────────────────────────────────────────────────┐ │
│    │ │ ## My notes  (a TEXT cell, written in Markdown)                    │ │
│    │ └───────────────────────────────────────────────────────────────────┘ │
└────┴───────────────────────────────────────────────────────────────────────┘
  ↑ left sidebar: Table of contents, Find, Variables {x}, Secrets 🔑, Files 📁
```

| Part | What it does |
|------|--------------|
| **Code cell** | A box where you type Python. Run it with the ▶ button or **Shift + Enter**. |
| **Text cell** | A box for notes, headings and explanations (written in *Markdown*). Double-click to edit. |
| **+ Code / + Text** | Add a new cell below the current one. |
| **Runtime menu** | Controls the Python "engine": *Run all*, *Restart session*, *Disconnect and delete runtime*. |
| **RAM / Disk indicator** | Shows you are connected to a cloud computer. Click it for details. |
| **Files 📁 (left)** | Upload data files, see files you created. These files are **temporary**: they disappear when the runtime resets. |
| **Variables {x} (left)** | Shows the variables Python currently remembers. Handy later in the course. |
| **Secrets 🔑 (left)** | A safe place for passwords and API keys. We use this in Session 8. |
| **Gemini ✦ (top right)** | Opens the AI assistant chat panel. |

### Keyboard shortcuts worth learning today

| Shortcut | Action |
|----------|--------|
| **Shift + Enter** | Run the cell and move to the next one |
| **Ctrl + Enter** (⌘ + Enter on Mac) | Run the cell and stay on it |
| **Ctrl + M, then B** | Insert a code cell below |
| **Ctrl + M, then M** | Turn the current cell into a text cell |
| **Ctrl + M, then Y** | Turn the current cell into a code cell |
| **Ctrl + /** | Comment / un-comment the selected lines |
| **Ctrl + S** | Save |

## Step 4 · Run your first cell

1. Click inside the first code cell.
2. Type:

   ```python
   print("Hello, Kenya!")
   ```

3. Press **Shift + Enter**.

The first time, Colab takes a few seconds to **connect** to a cloud computer (you will see "Connecting…" then a green tick ✓). Then the output `Hello, Kenya!` appears under the cell.

🎉 You just ran a Python program.

## Step 5 · Save your work properly

- Notebooks you create from **File → New notebook** are saved automatically in **Google Drive → My Drive → Colab Notebooks**.
- Notebooks you open from GitHub or someone else's link are **not** saved for you. Always use **File → Save a copy in Drive** first.
- Download a copy any time with **File → Download → Download .ipynb**.

## Step 6 · Open the course notebooks from this private repository

1. In Colab choose **File → Open notebook**.
2. Click the **GitHub** tab.
3. Tick **"Include private repos"**. A GitHub sign-in window opens. Sign in and click **Authorize**. (Allow pop-ups if your browser blocks the window.)
4. In the search box type `chia55` and pick this repository, e.g. `chia55/Session-1-Programming-in-the-Age-of-AI`.
5. Click `notebooks/01-lesson-first-program.ipynb`.
6. Immediately do **File → Save a copy in Drive**.

The "Open in Colab" badge at the top of each notebook also works once you have authorised GitHub in step 3.

**Alternative (no GitHub account):** download the `.ipynb` file from the facilitator, then in Colab use **File → Upload notebook**.

---

## Meeting the AI assistant in Colab

Colab includes Google's **Gemini** AI. Menu positions change from time to time, but you will usually find it in three places:

1. **The Gemini button (✦) at the top right** opens a chat panel. You can ask questions about Python or about your notebook.
2. **"Generate" in an empty code cell.** An empty cell shows a prompt such as *"start coding or generate with AI"*. Click *generate*, describe what you want in plain English, and Colab writes code for you.
3. **"Explain error" button.** When a cell fails, a button appears under the red error message. It asks the AI to explain what went wrong.

> AI features may need you to accept terms the first time, may be limited on the free tier, and may not be available in every country or on every account. Nothing in this course *depends* on them.

### Our three rules for using AI in this course

1. **Ask it to explain, not just to do.** "Explain what this line does" teaches you more than "write it for me".
2. **Read and run everything it gives you.** AI can be confidently wrong. *You* are responsible for the code you run.
3. **Try first, then compare.** In exercises, write your own attempt *before* asking AI. Then compare the two and decide which is better and why.

### Try it now (5 minutes)

In a new code cell, click *generate* and type:

> *print a short welcome message for new Python learners in Kenya*

Look at what it produced. Then ask the Gemini chat:

> *Explain the code in my last cell line by line for a complete beginner.*

Discuss: Did it do what you asked? Would you have written it the same way? Is there anything you don't understand yet? (That's fine, write it down and ask.)

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| "Connecting…" never finishes | Refresh the page. Then try **Runtime → Disconnect and delete runtime**, and run the cell again. |
| "You cannot currently connect to a GPU" | You don't need a GPU for this course. **Runtime → Change runtime type → CPU**. |
| Output from earlier cells is gone after a break | Colab disconnects idle sessions. Run cells again from the top: **Runtime → Run all** or **Run before**. |
| My uploaded file disappeared | Files in the 📁 panel are temporary. Keep originals on your computer or in Google Drive. |
| I can't see private repos from GitHub | Make sure you ticked *Include private repos*, authorised Colab in GitHub, and that your facilitator added your GitHub account to the `chia55` organisation. |
| The Gemini button is missing | Your account or region may not have it yet. Use any AI chat in another tab, or skip. |

Next: [01-optional-install-python-locally.md](01-optional-install-python-locally.md) (optional) or [02-what-is-a-program.md](02-what-is-a-program.md).
