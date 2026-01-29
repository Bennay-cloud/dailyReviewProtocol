
**📘 How to Use the Daily Review Protocol Template**

This repository contains a **template** you can use to write your daily learning or work protocols. The goal is:

* Each day = one protocol file
* You copy the template
* Fill it with your own notes
* Save it
* Push it back to GitHub

---
## 📋 Daily Review Protocol Rules

|  | Rule |
|---|------|
| 1 | The person responsible for the protocol is the **moderator** of the meeting. |
| 2 | After opening the meeting, the moderator must **explain the summarized topic**. |
| 3 | Once the explanation is done, the moderator **opens the discussion**. |
| 4 | The moderator is also responsible for **closing the discussion**. |
| 5 | The **stand-up meeting duration is 30 minutes**. |
| 6 | After all questions are clarified and the discussion is closed, the moderator must **save any changes made to the document**. |
| 7 | Finally, the moderator must **push the updated document back to GitHub**. |
---

# **🧰 Step 1 — Install Git (only once)**

Check if git is installed:

```
git --version
```

If not installed, install it from:

https://git-scm.com

---

# **📥 Step 2 — Clone (Download) the Repository**

1. Open your terminal
2. Go to the folder where you want to store your protocols:

```
cd ~/Documents
```

3. Clone the repo:

```
git clone https://github.com/USERNAME/REPO_NAME.git
```

4. Enter the folder:

```
cd REPO_NAME
```

---

# **📄 Step 3 — Create Your Daily Protocol File**

1. Copy the template:

```
cp protocol_template.md day_01.md
```

(or for another day)

```
cp protocol_template.md day_02.md
```

2. Open the file in VS Code or any editor:

```
code day_01.md
```

or

```
nano day_01.md
```

---

# **✍️ Step 4 — Fill in Your Notes**

Inside the file:

* Change the date at the top
* Replace the grey text with **your own content**
* You can delete all **`<span style="color:grey">`** parts (GitHub ignores them anyway)
* Keep the structure, just replace the text

Example:

```
# Day 03, 27.01.2026

## Basic Overview
- Learned Terraform modules
- Practiced AWS EC2 deployment
- Fixed IAM credential issues
```

---

# **💾 Step 5 — Save Your File**

Just save the file in your editor.

---

# **📤 Step 6 — Send (Push) Your Changes Back to GitHub**

1. Check what changed:

```
git status
```

2. Add your new file:

```
git add day_01.md
```

(or all changes)

```
git add .
```

3. Create a commit:

```
git commit -m "Add protocol for day 01"
```

4. Push to GitHub:

```
git push
```

---

# **🔄 Step 7 — Next Day Workflow**

Every new day:

```
git pull
cp protocol_template.md day_XX.md
# edit file
git add .
git commit -m "Add protocol for day XX"
git push
```

---

# **🧠 How the Template Works**

* The template is just a **structured note file**
* You:
  * Copy it
  * Rename it
  * Fill it
* The sections help you:
  * Structure your day
  * Write better notes
  * Keep everything consistent

---

# **📁 Suggested Folder Structure**

```
daily-review-protocols/
├── protocol_template.md
├── day_01.md
├── day_02.md
├── day_03.md
└── README.md
```

---

# **✅ Rules / Best Practices**

* One file per day
* Use clear file names
* Commit every day
* Don’t edit the template — only copy it
* Keep notes simple and structured

---

# **🎯 Goal**

After some weeks, you will have:

* **A ****complete learning diary**
* Searchable notes
* **A ****personal knowledge base**
* Proof of your learning journey
