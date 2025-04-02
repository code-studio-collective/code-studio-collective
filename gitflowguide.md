# 🛠️ Gitflow Guide — Code Studio Collective

This guide outlines how we work with Git, branches, and PRs for Code Studio Collective.

---

## 🚧 Working on Features

1. **Start from the latest `main`**
   ```bash
   git checkout main
   git pull origin main
   ```

2. **Create a new branch**  
   Name your branch using a clear convention:

   | Type      | Example                        |
   |-----------|--------------------------------|
   | Feature   | `feature/auth-flow`            |
   | Bugfix    | `bugfix/fix-email-validation`  |
   | Refactor  | `refactor/session-handler`     |
   | Hotfix    | `hotfix/broken-build`          |
   | UI        | `ui/signin-page-styles`        |

   ```bash
   git checkout -b feature/your-branch-name
   ```

3. **Make changes and commit**
   - Commit often with meaningful messages.
   - Keep commits focused.

   ```bash
   git commit -m "Add server-side validation for sign-in"
   ```

4. **Push your branch**
   ```bash
   git push origin feature/your-branch-name
   ```

---

## 🔁 Opening a Pull Request (PR)

Once your feature is complete:

1. Go to GitHub and open a PR targeting `main`.
2. Use a clear title (e.g., `Add login form error handling`).
3. In the PR description:
   - Explain what your changes do.
   - Mention anything to test.
   - Link to related issues if applicable.

---

## ✅ Reviewing PRs

If you're reviewing a PR:

- Read through the code and description.
- Add comments or suggestions where needed.
- Approve or request changes.

> Tip: Small PRs are easier and faster to review. ❤️

---

## ⬇️ Merging PRs

- We use **Squash and Merge** to keep `main` clean.
- Clean up the commit message before merging if needed.

After merging:

```bash
git checkout main
git pull origin main
```

---

## 🧼 Cleaning Up

Delete merged branches to keep the repo tidy:

```bash
git branch -d feature/your-branch-name             # local
git push origin --delete feature/your-branch-name  # remote
```

---

## 🧠 Best Practices

- One feature or fix per branch.
- Never commit directly to `main`.
- Rebase or merge from `main` regularly to resolve conflicts early.
- Add `[WIP]` in your PR title if it’s not ready to review.

---

## 🧪 Testing Your Work

Make sure your feature works locally:

```bash
npm run dev
```

If you added environment variables, ensure your `.env` is correctly set up.

---

## 🧭 Need Help?

Ask in the team Discord channel or ping a reviewer on your PR. We're here to help!

---

Happy coding! 🚀
