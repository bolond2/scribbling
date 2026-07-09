# Writing Site

A minimal Jekyll site set up for GitHub Pages. Twice-weekly practice posts on kid questions,
home/garden projects, and professional ideas as they come up.

## One-time setup (GitHub Pages)

1. Create a new **public** repo on GitHub (e.g. `yourusername.github.io` if you want it at the
   root domain, or any name like `writing` if you're fine with it living at
   `yourusername.github.io/writing`).
2. Push everything in this folder to that repo:
   ```
   cd writing-site
   git init
   git add .
   git commit -m "Initial site setup"
   git branch -M main
   git remote add origin https://github.com/YOURUSERNAME/YOURREPO.git
   git push -u origin main
   ```
3. On GitHub: go to the repo → **Settings → Pages** → under "Build and deployment," set
   **Source** to "Deploy from a branch," branch `main`, folder `/ (root)`. Save.
4. Wait a minute or two, then your site is live at the URL GitHub shows you on that same page.

No local Jekyll install is required — GitHub builds it for you automatically. If you *do* want
to preview locally before pushing, you'd need Ruby + Jekyll installed, but it's optional.

## Adding a new post

1. Create a new file in `_posts/` named exactly: `YYYY-MM-DD-short-title.md`
2. Add front matter at the top (see `_posts/2026-07-09-why-is-the-sky-orange.md` for the format):
   ```
   ---
   layout: post
   title: "Your Title Here"
   date: YYYY-MM-DD
   categories: [kid-questions]   # or [home], [garden], [work], etc — optional, flexible
   ---
   ```
3. Write the post in plain markdown below the front matter.
4. Commit and push. GitHub rebuilds the site automatically within a minute or two.

## Structure

```
writing-site/
├── _config.yml       site title/description
├── index.md          homepage
├── about.md           about page
├── _posts/            all posts go here, one file per post
└── docs/
    └── im-blocked.md  reference doc for when you're stuck on what to write
```

## Notes to self

- Tags/categories are flexible — don't overthink taxonomy up front, it can be cleaned up later.
- Anything with real work/confidential detail: keep the full version in a private note first,
  only publish a genericized version here.
- Delete or replace the example post once you've got a real first one up.
