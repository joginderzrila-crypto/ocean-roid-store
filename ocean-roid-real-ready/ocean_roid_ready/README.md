# Ocean Roid — Real Store + Admin

This is a production-oriented full-stack starter for Ocean Roid. It uses Express + PostgreSQL, real admin authentication, product management, orders, customers and reports.

## Deploy on Render
1. Create a new GitHub repository and upload the contents of this folder.
2. On Render, choose **New > Blueprint** and connect the GitHub repository. Render will read `render.yaml` and create the web service + PostgreSQL database. The included Blueprint uses a paid small Postgres plan because Render's Free Postgres expires after 30 days and is not suitable for a real store.
3. In the Render service environment variables, set:
   - `ADMIN_EMAIL` = your private admin email
   - `ADMIN_PASSWORD` = a strong private password
   - `WHATSAPP_NUMBER` = your WhatsApp number with country code, digits only (example: 9198xxxxxxxx)
   - `INSTAGRAM_URL` = your Instagram profile URL
4. Deploy. Open `https://YOUR-RENDER-URL/` for the store and `https://YOUR-RENDER-URL/admin` for the admin panel.
5. Login with the admin email/password you set in Render.

## Important
- Do NOT upload `.env` or passwords to GitHub.
- Change the admin password before going live.
- Customer photo files are intentionally handled through WhatsApp in this version; this avoids storing customer photos in the database. A later Cloudinary/S3 upload module can be added.
- Shipping and payment are recorded in the admin panel, but automatic Razorpay/Shiprocket settlement/tracking is not enabled yet.
- The current catalogue is seeded from Ocean Roid's supplied product list.

## Local run
Requires Node 18+ and PostgreSQL. Set `DATABASE_URL`, `JWT_SECRET`, `ADMIN_EMAIL`, `ADMIN_PASSWORD` and optionally `WHATSAPP_NUMBER` before `npm start`.
