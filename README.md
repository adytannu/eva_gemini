# Eva Gemini Apps

Static site for hosting Eva's web apps/games without depending on Gemini.

## Structure

- `index.html` - app directory homepage.
- `assets/apps.js` - list of apps shown on the homepage.
- `apps/<app-folder>/index.html` - each app's entry page.

## Add a New App

1. Create a new folder: `apps/my-new-app/`
2. Put that app's files in the folder (at least an `index.html`).
3. Add a new item in `assets/apps.js`:

```js
{
  title: "My New App",
  description: "Short description",
  path: "apps/my-new-app/",
  status: "Live"
}
```

## Publish on GitHub Pages (Free)

1. Create a new GitHub repository (for example `eva_gemini`).
2. From this folder, run:

```bash
git init
git add .
git commit -m "Initial static site"
git branch -M main
git remote add origin git@github.com:<your-username>/eva_gemini.git
git push -u origin main
```

3. On GitHub: `Settings -> Pages`
4. Under `Build and deployment`, choose:
   - `Source: Deploy from a branch`
   - `Branch: main`
   - `Folder: /(root)`
5. Save. Your site URL will appear in about 1-2 minutes.

## Other Free Static Hosting

- Cloudflare Pages
- Netlify
- Vercel (static)

All can deploy this exact folder without code changes.
