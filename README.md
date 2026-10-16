# ConversionSystem™ — Vercel Preview Project

This is a deployable static HTML project assembled from the 15-section GHL backup. It is a separate preview copy. Keep `ConversionSystem_GHL_Code_Backup_15_Sections.zip` as the untouched archival backup.

## Pages
- `/` — landing page assembled from the 13 landing sections
- `/checkout-page` — checkout UI and original checkout source code
- `/thank-you` — thank-you page

## Deploy with GitHub + Vercel
1. Extract this ZIP on your computer.
2. Create a **new** GitHub repository such as `ConversionSystem-Vercel-Preview` (Private recommended).
3. Upload the **contents of this extracted folder** to the repository root. Do not upload this ZIP as the only file. The repository root must contain `index.html`, `vercel.json`, and the `checkout-page/` and `thank-you/` folders.
4. In Vercel, choose **Add New → Project**, import this new GitHub repository, and deploy it.
5. Framework Preset: **Other**. For a static HTML site, leave the Build Command empty / skip the build; serve files from the project root (`.`). No dependencies are needed.
6. After deployment, test these routes: `/`, `/checkout-page`, and `/thank-you`.

## Important checkout note
- The checkout HTML/JavaScript, form IDs, payment endpoint URLs, dynamic Razorpay key/order handling, and payment verification code were copied from the original checkout snippet without modifying its contents.
- The main landing-page copy changes existing checkout CTA links to the preview site's `/checkout-page/` route. Those link changes exist only in this deployable preview copy; the archival section backup remains unchanged.
- Requests from a Vercel preview URL may be rejected by the existing backend's origin/CORS allowlist. Do **not** change payment keys or backend endpoints just to get the visual preview working. Until the final site origin is explicitly allowed by the backend, test page layout and navigation only, not real payments. Before switching a custom domain, make sure the backend allows that exact final origin while retaining any existing allowed production origin.
- Never add Razorpay secret keys, passwords, or private tokens to this repository.

## Source integrity
The archival ZIP is the source of truth for the individual uploaded snippets. This preview project wraps the snippets in complete HTML documents so Vercel can serve them as routes.
