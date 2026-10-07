# Guide 01 · (Optional) Installing Python on your own computer

**You can complete the entire course in Google Colab without installing anything.** Install Python locally only if you want to keep working offline, run scripts on your own files, or you are curious how professional developers work.

You will install three things:

| Tool | What it is | Analogy |
|------|-----------|---------|
| **Python** | The language interpreter that runs your code | The engine |
| **VS Code** | A free code editor from Microsoft | The dashboard and steering wheel |
| **Jupyter extension** | Lets VS Code open `.ipynb` notebooks like Colab does | A Colab-style view inside VS Code |

Recommended version: **Python 3.12 or newer** (any current 3.x release from python.org is fine).

---

## Windows 10 / 11

### 1. Install Python

1. Go to <https://www.python.org/downloads/> and click the big yellow **Download Python 3.x.x** button.
2. Open the downloaded installer (`python-3.x.x-amd64.exe`).
3. ⚠️ **On the first screen tick "Add python.exe to PATH".** This is the most common mistake. Without it, the terminal cannot find Python.
4. Click **Install Now**, wait, then click **Close**.

> Alternatively, install Python from the **Microsoft Store** (search "Python 3.13" or newer). It sets up PATH automatically.

### 2. Check it worked

1. Press the **Windows key**, type `cmd`, press Enter. A black window (the *Command Prompt*) opens.
2. Type the command below and press Enter:

   ```
   python --version
   ```

   You should see something like `Python 3.13.5`.
3. Also check pip, the tool that installs Python packages:

   ```
   python -m pip --version
   ```

**If you see** `'python' is not recognized…` → re-run the installer, choose **Modify**, and make sure "Add Python to environment variables" is ticked. Close and reopen Command Prompt afterwards.

**If the Microsoft Store opens** when you type `python` → you didn't tick "Add to PATH". Either install from the Store, or go to *Settings → Apps → Advanced app settings → App execution aliases* and switch off the two "python" aliases, then reinstall from python.org with the PATH box ticked.

## macOS

1. Go to <https://www.python.org/downloads/macos/> and download the **macOS 64-bit universal2 installer**.
2. Open the `.pkg` file and click through the installer.
3. At the end, a Finder window opens. Double-click **Install Certificates.command** (this lets Python download things securely).
4. Open **Terminal** (press ⌘ + Space, type `Terminal`, Enter) and check:

   ```bash
   python3 --version
   python3 -m pip --version
   ```

> On macOS the command is **`python3`**, not `python`. Older Macs have a built-in system Python, so don't remove or change that one.

## Linux (Ubuntu / Debian)

Most Linux systems already have Python 3. Open a terminal and run:

```bash
python3 --version
sudo apt update
sudo apt install python3-pip python3-venv
```

## ChromeOS / tablets / phones

Use Google Colab in the browser. On a Chromebook you *can* enable the Linux environment and follow the Linux steps, but Colab is simpler.

---

## Install VS Code

1. Download from <https://code.visualstudio.com/> and install with the default options. On Windows, tick **"Add to PATH"** and **"Open with Code"** if offered.
2. Open VS Code. Click the **Extensions** icon on the left (four squares) or press **Ctrl + Shift + X**.
3. Search for and install:
   - **Python** (publisher: Microsoft)
   - **Jupyter** (publisher: Microsoft)

## Create a course folder and run your first script

1. Make a folder, e.g. `Documents/chia-python`.
2. In VS Code: **File → Open Folder…** and choose it.
3. **File → New File**, name it `hello.py`, and type:

   ```python
   print("Hello from my own computer!")
   ```

4. Save (**Ctrl + S**), then click the ▶ **Run Python File** button at the top-right.
   The output appears in the **Terminal** panel at the bottom.

If VS Code asks you to **"Select Interpreter"**, choose the Python version you just installed.

## Open a notebook in VS Code

1. Download a `.ipynb` file from this repository (or create one with **File → New File → Jupyter Notebook**).
2. Open it in VS Code. Click **Select Kernel** (top-right) → **Python Environments** → your Python.
3. VS Code may ask to install `ipykernel`. Click **Install**.
4. Run cells with **Shift + Enter**, just like Colab.

---

## A preview: virtual environments (you'll use these from Session 5)

Real projects keep their packages in a *virtual environment*: a private box of packages for one project, so projects don't fight over versions.

```bash
# inside your course folder
python -m venv .venv            # macOS/Linux: python3 -m venv .venv

# activate it
.venv\Scripts\activate          # Windows (Command Prompt)
source .venv/bin/activate       # macOS / Linux

# install packages into it
python -m pip install pandas

# leave it
deactivate
```

When the environment is active your prompt starts with `(.venv)`. VS Code usually detects `.venv` automatically and offers to use it.

> **Faster alternative (optional):** many professionals now use [`uv`](https://docs.astral.sh/uv/), a very fast tool that installs Python and packages in one go (`uv venv`, `uv pip install pandas`). It's great, but the standard tools above are all you need for this course.

---

## Troubleshooting checklist

- Close and reopen the terminal after installing anything: terminals only read PATH when they start.
- Use `python -m pip install …` rather than plain `pip install …`. It guarantees pip installs into the same Python you are running.
- On macOS/Linux, use `python3` and `python3 -m pip`.
- Corporate laptops sometimes block installers. Use Colab instead.

Next: [02-what-is-a-program.md](02-what-is-a-program.md)
