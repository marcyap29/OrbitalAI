# orbitalai.net

Parent-brand site for Orbital AI. Same build shape as sabihin.com: one
static `index.html`, one `favicon.svg`, one `vercel.json`. No build step,
no serverless function (nothing to submit here; the waitlist lives on
sabihin.com).

## Deploy

1. New GitHub repo (e.g. `marcyap29/orbitalai-website`), push these files.
2. Vercel: Add New → Project → Import that repo. No build command, no
   output directory.
3. Project → Settings → Domains → add `orbitalai.net` and `www.orbitalai.net`.
   Vercel shows you the A record and CNAME to set at your registrar.
   Remove the old Carrd DNS records first or they'll fight.
4. Once DNS propagates (minutes to a few hours), cancel Carrd.

## What `vercel.json` does

Two redirects so the parent site never hard-codes product URLs in
more than one place:

- `orbitalai.net/sabihin` → `https://sabihin.com`
- `orbitalai.net/download/mac` → `https://sabihin.com/download/mac`

The second one chains into the redirect on sabihin.com, which points at
the GitHub release asset. Change the destination there, and both sites
follow.

## Design notes

- Palette is cooler and blacker than Sabihin on purpose. Parent is the
  sky, product is the warm room inside it. Sabihin's own tokens are used
  only inside the Sabihin panel.
- Type is IBM Plex Serif (display, weight 300) and IBM Plex Sans (body).
- The hero instrument: eight rays at 45°, one tilted orbit, one brass
  body. The body is the only thing on the page that moves. Reduced-motion
  users get it parked.
- No og:image yet. Same reasoning as sabihin.com: a missing card beats a
  broken one. Add when designed.
- Correspondence is deliberately absent. Add a section when it's real.
