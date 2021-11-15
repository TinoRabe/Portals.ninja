---
title: "Setup Guide"
date: 2021-11-15T14:53:11+01:00
draft: true
---

1. Install Homebrew
2. Install Git
3. Install Hugo
4. Install Visual Studio Code
5. Create directory in file system
6. In GitHub, fork theme of choice to personal account
7. from VS Code, create new Hugo Site "Sample":

```bash
hugo new site Sample
```

7. Jump to site folder via VS Code Terminal:
```bash
cd Sample
```

8. Jump to theme folder via VS Code Terminal:
```bash
cd themes
```

9. from VS COde Terminal, add theme from repo as submodule
```bash
git submodule add https://github.com/YOURACCOUNT/THEMEREPO
```

10. Initialize GIT repo
```bash
git init
```

11. ENsure that main branch is used in GIT
```bash
git branch -M main
```

12. Commit changes in GIT
```bash
git add -A
git commit -m "initial commit"
```

13. Add perosnal GitHub repository as a remote to your local repo
```bash
git remote add origin https://github.com/YOURACCOUNT/REPO
```

14. Push your local repo up to GitHub
```bash
git push --set-upstream origin main
```

15. In Azure Portal, craete new Static Web App Service in Resource Group & link Github repo