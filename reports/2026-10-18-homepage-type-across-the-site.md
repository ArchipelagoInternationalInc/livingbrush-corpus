# 2026-10-18, The home page's type across the whole site

All seven pages. Live, commit `def1288`.

---

## What changed

Every page now uses the same three faces the home page uses:

- **Barlow Condensed** for headlines
- **Montserrat** for labels
- **Inter Tight** for body text

The six interior pages were using Fraunces for headlines and Geist Mono for
labels. Body text was already Inter Tight everywhere, so that did not move.
Each page now asks the type service for exactly those three faces and nothing
else, where before the interior pages were loading two faces the site no longer
uses.

This is the typography half of Phase 1a in the plan, which asked for exactly
this set.

## The part that needed judgement

Swapping the face alone made the interior headlines read as weaker. Barlow
Condensed is a condensed face: at the same point size it sets narrower and
lighter than the serif it replaced. Set side by side at the old size, the
About headline shrank from about 1,150 pixels wide to about 990, and it read
as a smaller page rather than a different one.

So the display sizes came up by about a sixth across those pages, and the tight
negative letter spacing the serif used was opened up, because a condensed face
does not want it. The About headline now sets at 78 pixels instead of 67 and
takes back the width it had. The result reads as the same page in the home
page's voice, rather than as the same page shrunk.

The first attempt at this was uneven: the display rules are written slightly
differently on each page, so matching their exact text only caught three of the
six. That was backed out and done again by finding every rule that uses the
display face and scaling its sizes, which caught all of them: between three and
six rules per page.

## Checked

All six checks pass, including the contrast check that reads the real pixels:
394 measurements across the menus and footers of all seven pages at both sizes,
none below the mark, and no errors in the browser console on any page.

Confirmed on the live site, all seven pages: headline face, label face and body
face all match the home page.

## Worth knowing

The preview branch `phase-1a-about` did this for the About page only, through a
shared stylesheet. The type part of that work has now happened on the live site
for all seven pages instead. What that branch still holds, and the live site
does not, is the shared stylesheet itself: on the live site each page still
carries its own copy of the styles. Pulling those together is still worth
doing, and is still the thing that makes the next change happen once rather
than seven times.
