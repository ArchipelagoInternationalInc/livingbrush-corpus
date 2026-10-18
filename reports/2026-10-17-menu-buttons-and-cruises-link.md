# 2026-10-17, Three buttons in the menu, and a Cruises link

All seven pages. Live.

---

## What is there now

To the right of the phone number, three buttons in order: Madelyn, Cruises,
Contact. Madelyn and Cruises are outlined in gold on a see-through background;
Contact is filled with the same gold and set in near-black, so it is the
loudest of the three. All three are the same shape, because they share the
measurements of the Contact button that was already on each page.

Madelyn goes to the fine-art site and replaces the plain text link that used to
sit in the menu. Cruises goes to the new cruise and resort site. Both open in a
new tab. Contact still reaches the form on the home page and is still last.

The footer of every page gained a plain Cruises link beside the ones already
there, in the footer's own style, opening in a new tab. No other footer text
changed.

## The problem that shaped the solution

The menu is drawn with a blend that inverts it against whatever is behind it.
That is what lets one piece of white type stay readable over a black page, over
a white page, and over photographs as they scroll past underneath.

Anything inside a blended element is blended along with it. Gold inverted
against white is not a paler gold, it is blue. So gold buttons could not simply
be added to the menu: on the one white page they would have come out blue.

The first attempt moved the blend off the menu and onto only the pieces that
need to flip. That failed, and the failure is worth recording. The menu is
pinned to the top of the screen and stacked above the page, and that by itself
makes it a sealed group for blending purposes. A piece inside it has nothing
left to blend against, so the name and the links turned white on white and
vanished on the white page. Caught by looking at the picture, not by any
measurement, since every number still read as correct.

What was checked next was whether the blend is doing real work or is decoration
that could be dropped. It is doing real work: the menu passes over photographs
on three of the pages and over a pale panel near the foot of the home page, and
only one of the seven pages is white. Six are dark. So the blend stayed.

The buttons were moved out of the menu instead, into their own strip pinned to
the same row. The menu keeps blending exactly as before; the buttons keep their
real colours on every page and over every photograph.

## On a phone

Three buttons will not fit beside the menu at phone width. They drop to their
own line under the logo, centred, as a group, keeping the same three shapes.
Measured at 390 wide on all seven pages: one row, equal gaps between the three,
nothing running off the side, and the page exactly as wide as the screen.

## Checked

All seven pages carry identical button markup and the same footer link. The
checker passes all five checks. No em dashes.

Clicked on the live site, from the home page and from an interior page, at both
sizes, sixteen tests in all: Madelyn opens the fine-art site in a new tab,
Cruises opens the cruise site in a new tab, Contact reaches the form and brings
it into view, and the footer Cruises link opens in a new tab. All passed.

Commit `d505d43`.

## One thing fixed in passing

One page was missing the rule that shrinks the Contact button on a phone, so
its button was larger there than on the other six. Since all three buttons now
share that rule, it was added to that page as well and the seven now match.
