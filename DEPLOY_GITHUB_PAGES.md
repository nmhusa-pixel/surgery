# Deploying To GitHub Pages

This folder is ready to publish as a static web app.

## Option 1: GitHub Web Upload

1. Create a new GitHub repository.
2. Upload every file in this `outputs` folder to the repository root.
3. Make sure `index.html`, `manifest.webmanifest`, `service-worker.js`, and `surgical-anticoag-icon.png` are all at the root.
4. In GitHub, go to `Settings` > `Pages`.
5. Under `Build and deployment`, choose `Deploy from a branch`.
6. Select branch `main` and folder `/root`, then save.
7. Open the GitHub Pages URL after the deployment finishes.

## Option 2: Git Command Line

```bash
git init
git add .
git commit -m "Add anticoagulant hold helper app"
git branch -M main
git remote add origin https://github.com/YOUR-USER/YOUR-REPO.git
git push -u origin main
```

Then enable GitHub Pages from `Settings` > `Pages`.

## Installable App Behavior

The app includes a web manifest and service worker. After it is served over HTTPS by GitHub Pages, supported browsers can install it as an app. The local `file://` version still works, but install/offline behavior only works from a web URL.
