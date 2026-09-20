# 2026-09-20, Phase 1a, the About page on a preview branch

Part C of the overnight run. **Nothing here is live.** It sits on a branch
called `phase-1a-about` and was never merged.

---

## The preview address, and who can open it

`https://livingbrush-3jznfj744-archipelago-international-inc-s-projects.vercel.app`

**A stranger cannot open it.** Asked for without any login, it redirects to the
Vercel sign-in page. The project has deployment protection turned on, which is
the sensible default and was not changed. Scott can see it while signed in to
Vercel. If it needs to go to someone outside the team, Vercel can issue a
sharing link for a protected deployment, or protection can be turned off for
previews. That is an account setting and a decision for Scott, so it was left
alone.

## What the About page needed, and what it did not

The plan describes Phase 1a as converting the interior pages to dark type on
white. **The About page was already dark type on white**, black on pure white.
So that part was already done, and the real work was the type, the grey, and
pulling the styles out into a shared file.

## What changed

- A new shared stylesheet, `assets/interior.css`. Only the About page links it.
  The other five interior pages still carry their own styles and were not
  touched.
- The About page dropped its own block of styles entirely and links the shared
  one instead. The page file went from about 14,700 characters to about 8,100.
- The typefaces now match the home page: Barlow Condensed for headlines,
  Montserrat for labels, Inter Tight for body, requested from Google in exactly
  the way the home page requests them. The old Fraunces and Geist Mono are gone.
- Grey text is gone. Labels and quiet paragraphs were #5A564E. Measured, that
  was 7.3 to 1 against white, so it was never hard to read, but it read as grey
  and the house rule forbids it. Those are now near-black, #1C1B19, which
  measures 17.2 to 1. The smallest label sizes went up a step at the same time,
  from about 10.9 pixels to about 12.5.

Every piece of text on the finished page was measured: nothing sits below 17 to
1 against its background.

## The gold, and why it is not used here

The home page accent #E2B04A sits on black at 10.5 to 1, which is strong. On
white it measures **1.99 to 1**, far below the 4.5 that readable text needs. It
is defined in the shared stylesheet so the value lives in one place, but it is
deliberately not used for text on this white page. Making it work on white
would need a darker companion tone, and inventing a colour was outside this
brief.

## Unchanged, deliberately

No words were altered. The caption under the wedding photograph reads exactly as
it did. The Contact link in the footer and the Madelyn link in the menu both
still work. No image was touched; the page's one photograph is well under the
size limit.

## Checked by looking, not only by measuring

Full-page pictures of the live page and the new one, at both sizes, are saved
beside the work as before and after pairs, plus close views of the phone
headline and footer. Looked at directly: the headline sets well in the
condensed face, the rooms and the pull quote hold their shape, the biography box
is intact, and the footer is unchanged in structure. On a phone the headline
still flows as one centred paragraph, the page is exactly as wide as the screen,
and nothing overlaps or is cut off. The checker passes all five checks on the
branch.

## One thing to settle before this goes live

The deployment configuration tells browsers to keep anything under `assets/` for
a year and never check again. That is right for the animation libraries, which
never change. It is wrong for a stylesheet that is going to change five more
times during Phase 1: a returning visitor would keep the old one. Before this
branch is merged, either exclude the stylesheet from that rule or give its name
a version. Not fixed here because it is a change to the live site's
configuration and this part was not allowed to touch anything live.
