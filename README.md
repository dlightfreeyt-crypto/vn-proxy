# PROXY SERVER Simple Website

Includes a single-page request form with UID, Gmail/mobile, plan selection (Free 24-hour trial or Paid access ₹2,000), optional message, and Submit. `admin.html` is a separate secure admin dashboard.

## Setup
1. Create a Supabase project.
2. Run `supabase/schema.sql` in SQL Editor.
3. Add Supabase Project URL and public publishable/anon key to `config.js`. Never add a service-role/secret key.
4. Create an admin user under Authentication → Users; copy UUID and run `insert into public.admin_users(user_id) values('YOUR-ADMIN-UUID');` in SQL Editor.
5. Upload all files to GitHub (keep `index.html` at root).
6. Import the GitHub repo at Netlify and deploy with publish directory `.` and blank build command.
7. Main form is the site URL; admin panel is `/admin.html`.

The form collects only UID, contact details, selected plan and optional note. It does not collect passwords/OTPs or process payments. The trial/price are displayed as options; automatic expiration/payment activation is not implemented.
