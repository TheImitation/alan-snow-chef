# Quick Git Workflow

## First time: clone the repo to your machine

```bash
git clone https://github.com/YOUR_USERNAME/alan-snow-catering
cd alan-snow-catering
```

## Every time you edit

1. Make your changes to `index.html` (or other files)
2. Check what changed:
   ```bash
   git status
   ```
3. Stage your changes:
   ```bash
   git add index.html
   ```
   (Or `git add .` to stage everything)

4. Commit with a message:
   ```bash
   git commit -m "Update contact email and about section"
   ```
   (Keep messages short and clear)

5. Push to GitHub:
   ```bash
   git push
   ```

That's it. Cloudflare detects the push automatically and redeploys the site in ~30 seconds.

## View deployment status

- **On Cloudflare:** Workers & Pages → alan-snow-catering → **Recent deployments**
- **On GitHub:** Your repo page → green checkmark means successful build

## Undo a change

If you pushed something wrong, revert the last commit:

```bash
git revert HEAD
git push
```

Or go back to a previous version without committing:

```bash
git checkout HEAD -- index.html
```

## See your commit history

```bash
git log --oneline
```

Shows all past commits with short messages. Easy to spot what changed when.

---

**Tip:** Git saves your work locally *and* on GitHub. If your machine crashes, your code is safe on GitHub. Always push.
