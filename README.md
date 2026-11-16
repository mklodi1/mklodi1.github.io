# Personal site

A simple, single-column personal page with a blog built with Jekyll for GitHub Pages. GitHub builds it for you, so you never run a build step yourself.

## Put it online (about 10 minutes)

1. **Create the repo.** On GitHub, click **New repository** and name it exactly `<your-username>.github.io` (for example `mlodi.github.io`). Make it **Public**. Don't add a README.
2. **Upload the files.** On the new repo's page, click **uploading an existing file**. Drag in *everything inside* this folder, including the folders whose names start with `_` (`_layouts`, `_posts` and so on). Click **Commit changes**.
   - On a Mac, files starting with `.` are hidden in Finder. Press `Cmd + Shift + .` to show `.gitignore`. It's optional, so skipping it is fine.
3. **Turn on Pages.** Go to **Settings → Pages**. Under *Build and deployment*, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, then click **Save**.
4. **Wait a minute,** then visit `https://<your-username>.github.io`. The **Actions** tab shows build progress, and a red ✗ there means a build error with details.

If you prefer the command line:

```bash
cd site
git init && git add . && git commit -m "First version of my site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
git push -u origin main
```

## Make it yours

Search the project for `TODO`. Every spot you need to fill in has one.

| What | Where |
|---|---|
| Name, role, affiliation, email, links, quote | `_config.yml` |
| Bio and "Outside of work" text | `index.html` |
| News items | `_data/news.yml` |
| Selected work | `_data/work.yml` |
| Photos | add files to `assets/img/`, then turn on `portrait:` / `place_photo:` in `_config.yml` |
| CV | add `assets/resume.pdf`, or delete the `resume:` line in `_config.yml` |
| Anonymous message box | make a free form at formspree.io, then put its ID in `formspree_id:` in `_config.yml` |
| Link color | `--link` at the top of `assets/css/style.css` |

In the `.yml` files, keep the indentation exactly as it is, and wrap text in "double quotes" if it contains a colon.

## Write a post

Add a file to `_posts/` named `YYYY-MM-DD-title.md`:

```markdown
---
title: My post title
---

Write in Markdown here.
```

Commit it, and it shows up under Writing, on the home page, and in the RSS feed at `/feed.xml`.

## Preview on your computer (optional)

This needs Ruby installed. Run `bundle install`, then `bundle exec jekyll serve`, and open http://localhost:4000.

## Custom domain (optional)

In **Settings → Pages → Custom domain**, enter your domain and follow GitHub's DNS instructions. Then update `url` in `_config.yml`.
