# Student Tracker MVP

A responsive student-only academic progress tracker built with HTML, CSS and JavaScript. It includes:
- Sign up / sign in interface
- Dashboard overview
- Course progress tracking
- Assignment/task tracking
- Study session logging
- Academic goals
- Weekly study activity visualization

## Run locally
Open `index.html` in a modern browser. No build step is required.

## Demo mode
Without Supabase credentials, the app uses browser `localStorage` for a demonstration. This is not secure authentication, is limited to that browser, and must not be used for real student data.

## Enable Supabase authentication
1. Create a Supabase project.
2. In `index.html`, replace `YOUR_SUPABASE_URL` and `YOUR_SUPABASE_ANON_KEY` with the Project URL and anon/public key from Supabase Project Settings → API.
3. In Supabase Authentication settings, configure your allowed redirect URLs for your local and deployed site.
4. Enable Email provider. If email confirmation is enabled, users must confirm their email before signing in.
5. Deploy the folder to GitHub Pages.

Important: the current MVP stores courses, tasks, study sessions and goals in browser localStorage. Supabase authentication alone does not sync that data to the cloud or protect it across devices. Before production, create user-owned database tables and Row Level Security policies, then replace localStorage operations with Supabase database operations. Never put a Supabase service_role key in frontend code.
