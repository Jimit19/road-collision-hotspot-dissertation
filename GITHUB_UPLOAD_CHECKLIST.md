# GitHub Upload Checklist — Full Project

This package contains all files from the original project ZIP. Because some files exceed GitHub's normal per-file limit, push it using **Git LFS**, not GitHub's browser uploader.

## 1. Create an empty private repository

Recommended repository name:

`road-collision-hotspot-dissertation`

Do not initialise it with a README, `.gitignore`, or licence.

## 2. Install Git and Git LFS

On Windows, install Git for Windows and Git LFS if not already installed.

Then open Git Bash / terminal in this project folder and run:

```bash
git lfs install
git init
git add .
git commit -m "Add complete MSc dissertation project"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/road-collision-hotspot-dissertation.git
git push -u origin main
```

The `.gitattributes` file already routes the large GeoPackages, model artefacts, and very large CSV files through Git LFS.

## 3. Check Git LFS before the push

Run:

```bash
git lfs ls-files
```

You should see the large project files listed.

## 4. Important storage note

The full project is roughly 834 MB before Git overhead. Git LFS storage/bandwidth quotas may apply to your GitHub account. If GitHub blocks the push because of LFS quota, use the smaller GitHub-ready package instead or remove the raw/derived large data while keeping all code and final outputs.

## 5. Demo video

For the repository part of the demo, show:

- the repository homepage and README
- the notebooks folder / staged notebooks
- the outputs folders
- briefly state that large data artefacts are versioned using Git LFS

Do not spend time opening every file.
