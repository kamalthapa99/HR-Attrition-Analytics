# How to Push This Repo to GitHub

Follow these steps exactly. You only do steps 1–2 once; the rest you reuse every time you update the project.

---

## Step 1 — Create the repository on GitHub

1. Go to https://github.com/new
2. **Repository name:** `hr-attrition-analytics`
3. **Description:** `End-to-end HR attrition analysis — synthetic data generation, Python data cleaning, and a 4-page interactive Power BI dashboard.`
4. Set to **Public**
5. **Do NOT** check "Add a README" / "Add .gitignore" / "Add license" — this repo already has them
6. Click **Create repository**

---

## Step 2 — Push from your computer

Open a terminal **inside the `hr-attrition-analytics` folder** and run these commands one by one.
Replace `YOUR_USERNAME` with your actual GitHub username.

```bash
# Initialize git
git init

# Stage all files
git add .

# First commit
git commit -m "Initial commit: HR attrition analytics end-to-end project"

# Rename branch to main
git branch -M main

# Connect to your GitHub repo
git remote add origin https://github.com/YOUR_USERNAME/hr-attrition-analytics.git

# Push
git push -u origin main
```

That's it — refresh your GitHub page and everything will be there.

---

## Adding the Power BI file (.pbix)

The `.pbix` file isn't included here because it lives on your machine. To add it:

```bash
# Copy your .pbix into the dashboard folder, then:
git add dashboard/hr_attrition_dashboard.pbix
git commit -m "Add Power BI dashboard file"
git push
```

> **Note:** If your `.pbix` is larger than 100 MB, use [Git LFS](https://git-lfs.github.com/):
> ```bash
> git lfs install
> git lfs track "*.pbix"
> git add .gitattributes
> ```

---

## Making future updates

Whenever you change something:

```bash
git add .
git commit -m "Describe what you changed"
git push
```

---

## Professional touches (optional but recommended)

1. **Add topics** — on your repo page, click the ⚙️ next to "About" and add tags:
   `python` `pandas` `power-bi` `data-analytics` `data-cleaning` `hr-analytics` `dashboard`

2. **Pin the repo** — go to your GitHub profile → "Customize your pins" → select this repo.

3. **Set the About section** — add the description and check "Releases" / "Packages" off if unused.

4. **Add a release** — once stable, go to Releases → "Create a new release" → tag `v1.0.0`.
