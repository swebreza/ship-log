# Ship log

One self-contained page. No build step, no dependencies, no framework. `index.html` is the whole site.

## Deploy

Fastest route, from this folder:

```bash
npx vercel --prod
```

Accept the defaults. Vercel detects a static site and serves `index.html` at the root.

If you would rather keep it under your existing portfolio at `suweb-mu.vercel.app`, copy `index.html` into that project as `public/ship-log.html` (or `app/ship-log/page.tsx` if you want it as a route) and it becomes `suweb-mu.vercel.app/ship-log`.

Either way, put the final URL into every `{ship log link}` placeholder in `../OUTREACH.md` before sending anything.

## What to keep updated

The numbers are the whole point of the page, so they need to stay true.

Regenerate the commit count any time you want to refresh it:

```bash
cd "C:/Users/Suweb Reza/onefolder/Desktop/emireq" && for d in */; do [ -d "$d/.git" ] || continue; n=$(git -C "$d" log --author="swebreza" --oneline | wc -l); echo "$n  $d"; done | sort -rn
```

Then update the four numbers in the stat band and the per-product `.metrics` blocks.

## Deliberate choices worth knowing

**No live product URLs.** I checked the repos and the only public URLs are placeholders (`emireq-main-xxx.run.app`). Rather than link things I could not verify, the page proves itself with counted numbers, the stack, the hard problem in each product, and a command anyone can run to check the commit totals. If any of these are publicly reachable, add the link under the product name.

**No screenshots.** There are DataZonn and auth-gateway PNGs in the emireq folder, but shots for two products out of six reads as uneven rather than as evidence. If you want images, add one per product or none.

**Takafulik shows no commit count.** Its repo has 7 commits because the work landed in large batches, and a "7" next to "462" would undersell it. That row leads on portals and deployment shape instead. Nothing is misstated; a weak number is simply not the thing being claimed.

**Dates say Mar to Aug 2026, and that is deliberate.** Your first commit in this workspace is 2026-03-18, so the window is 6 months, not 12. Earlier drafts of your resume said 12 months; that was wrong and has been corrected everywhere. The 6-month version is the stronger claim anyway: 1,350 commits and six verticals in six months is a velocity number, and it lines up exactly with your Emireq start date so it survives scrutiny.

**17 repositories, not 18.** The workspace has 18 git repos but Attlas-Wire has zero commits by you, so it is not counted.
