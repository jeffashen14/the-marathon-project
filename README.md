# The Marathon Project

A mobile-first personal training log and marathon progress dashboard.

## Publish on GitHub Pages
1. Open repository **Settings → Pages**.
2. Under Build and deployment, choose **Deploy from a branch**.
3. Select branch **main** and folder **/(root)**, then Save.
4. Wait for deployment. Site: https://jeffashen14.github.io/the-marathon-project/
5. On iPhone, open the site in Safari, tap Share, then **Add to Home Screen**.

## Included
Workout logging (runs, strength, cross-training, other, rest), editing/deleting, calendar, weekly mileage goal, progress summaries, personal records, CSV import/export, local storage and installable PWA shell.

## Private cloud sync
1. Create a free project at https://supabase.com/.
2. Open SQL Editor and run the contents of `supabase/schema.sql`.
3. In Project Settings → API, copy the Project URL and anon/public key.
4. In app Settings → Cloud sync, enter both values and connect.
5. Enter your email and use the sign-in link. Repeat on other devices with the same email/project.
Never put a service-role key in the website or repository. The SQL enables row-level security so each signed-in user can access only their own workout rows. Local browser storage works without Supabase but does not sync by itself. This first version merges new workout rows; advanced conflict handling and syncing settings/PRs are not yet implemented. Export CSV backups periodically.

## Apple Watch
A website cannot directly access HealthKit or automatically pair with Apple Watch. CSV import is supported. Automatic Watch syncing requires a native iOS companion app with HealthKit entitlement and user permission. Full Apple Health XML export parsing is not included yet.

## Notes
The GitHub repository contains public app code, not private workout data. Training targets are editable starting points, not medical clearance or a fixed coaching plan.