# Ruby HQ

A mobile-friendly home base for Ruby. Plain HTML, CSS, and JavaScript; no build step, API keys, or backend needed.

## Put it on GitHub Pages

1. Create a repository named `ruby-hq` on GitHub. A public repository is the simplest option for free Pages hosting.
2. Upload the **contents** of this folder to the repository root. `index.html` must be at the top level, not inside another `ruby-hq` folder. Keep `styles.css`, `app.js`, and `icon.svg` beside it. Include `.nojekyll` if uploading with Git (it is hidden in Finder).
3. Commit the files to `main`.
4. Open the repository's **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**, then **main** and **/ (root)**. Save.
6. Wait for the deployment to finish. The Pages settings show your website address, typically `https://YOUR-USERNAME.github.io/ruby-hq/`.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

You do not need to upload the ZIP itself. Unzip it and upload its contents. The included .gitignore excludes downloaded backup files from normal Git commits; never manually upload personal backups into the public repository.

## Included

- Today dashboard with potty, walking, meal, and training summaries
- Twelve activity types, timestamps, optional durations, notes, edit, and delete
- Activity history with date and type filters
- Editable daily schedule with date-specific checkmarks
- Veterinary contact details, medication instructions, and care notes
- Training skills, cues, progress, and practice logs
- JSON backup export and validated import
- Responsive phone and desktop layouts, keyboard navigation, and reduced-motion support

The default schedule and training cards are editable starter examples. There are no sample activity records or prefilled medical details. Routine checkmarks and activity logs are independent.

## Data and privacy

Records stay in localStorage in the browser you use. They are not sent to GitHub and do not automatically sync across devices or browsers. Clearing site data, using private browsing, changing the website address, or changing devices may make records unavailable. Export a backup from Settings regularly. Importing a backup replaces the current records and settings after confirmation.

Anyone who can use that browser profile can access its saved records. This is not an account-based or encrypted medical records service. Google Fonts supplies the optional typefaces; system fonts are used if they cannot load. No analytics are included.

Dates use your device's local timezone. Daily checkmarks reset by date; activity history remains. There are no background reminders, push notifications, or guaranteed offline loading.

## Local preview

From this folder, run `python3 -m http.server 8080` and visit `http://localhost:8080`. Use the published HTTPS website for everyday use; browser storage behavior for files opened directly can vary.

## Customize

- `index.html`: page shell, navigation, activity dialog
- `styles.css`: colors, spacing, and responsive layout
- `app.js`: views, default routine, logging, and storage
- `icon.svg`: Ruby HQ icon

Changing defaults in code affects new browsers only; existing users edit their routine and training cards in the dashboard. Export a backup before changing storage-related code.
