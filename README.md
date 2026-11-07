# Speed Trap Alert Zambia — updated PWA

## What's new
- Live map using OpenStreetMap tiles and Leaflet.
- Recent community reports shown on the map and in lists.
- Shared online reports through Supabase (after configuration).
- Reports expire after approximately 6 hours.
- Local-only fallback if Supabase is not configured or unreachable.
- Existing GPS speed display and speed reminder retained.

## Important: online sharing is not active until configured
1. Create a free Supabase project at https://supabase.com/.
2. Open SQL Editor in the Supabase dashboard.
3. Run the contents of `supabase-schema.sql`.
4. Open Project Settings > API (or API Keys).
5. Copy the Project URL and the `anon` / publishable public key.
6. In `index.html`, find `SUPABASE_URL` and `SUPABASE_ANON_KEY`.
7. Replace the two placeholder strings with your own Project URL and public anon/publishable key.
8. Save and upload the updated files to the root of your GitHub repository.

Never put your Supabase `service_role` or secret key in this website. Never share your Supabase password.

## Publish to GitHub Pages
Upload/replace `index.html`, `manifest.json`, `sw.js`, `icon.svg`, and `README.md` in the root of your existing repository. Also upload `supabase-schema.sql` for reference. Commit changes to `main`. Wait for Pages to deploy, then reload the app. If the installed app still shows the old version, close it fully and reopen; clear the site cache only if necessary.

## Privacy and safety
- When online sharing is configured, report type, optional note, and the selected GPS coordinates are publicly readable by app users.
- Reports are user-submitted and unverified. They may be wrong or outdated.
- The included public insert policy is a starter setup, not abuse-proof. Before a public launch, add moderation, abuse controls/rate limits, privacy information and a way to report inaccurate content.
- Do not collect names, phone numbers or personal details in report notes.
- GPS speed and location may be inaccurate. Follow posted limits and traffic laws. Never handle the phone while driving.
- OpenStreetMap map tiles require internet and are provided under OpenStreetMap's tile usage policy.
