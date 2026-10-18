# 2026-10-17, Menu contrast: measured from the pixels, then fixed

All seven pages. Live, commit `c5cd3cb`.

---

## Why the stylesheet could not answer this

The menu was drawn with a blend that inverts it against whatever is behind it.
The colour written in the file was therefore never the colour on the screen.
So the menu was photographed and the actual pixels were read: for every piece
of menu text, the commonest colour inside its box is the background and the
colour furthest from that in brightness is the ink. Then the contrast between
the two was worked out. Two screen sizes, two scroll positions, every page.

Two measuring faults had to be fixed before the numbers could be trusted. The
first counted a button's word as absent because the letters cover only about
one per cent of the button; the second read the page showing just outside a
button's edge as though it were the button's ink. Both were found by checking a
result that looked wrong against the same button on another page.

## What the before measurement found

206 measurements, **25 below the pass mark**, in three groups.

**The two outline buttons on every white page.** Gold #E2B04A on white measures
**1.99 to 1** against a mark of 4.5. This affected About, Events and Record at
both screen sizes, top of page and scrolled.

**Menu links where the menu passed over a photograph.** On Events, four links
measured between 1.00 and 1.05 to 1: the blend had turned the text almost
exactly the colour of the picture behind it. On About one link measured 4.07.

**An outline button over a photograph.** The outline buttons are see-through,
so on Work at phone width the picture behind showed through the Cruises button
and its word measured 1.45 to 1.

## A correction to what was recorded before

An earlier report of mine said only the About page is white. That was wrong,
and it was wrong because it was generalised from four pages rather than all
seven. **Three pages are white: About, Events and Record.** The gold buttons
were therefore failing on three pages, not one.

## What changed

**The blend is gone.** It could not hold a pass mark over photographs and it
turns gold blue on a white page. Readability beats the blend.

**A scrim replaces it.** The menu now carries a soft bar in the page's own
colour, fading out downward, so menu text always sits on a known background
even while a photograph scrolls underneath. On the black home page the bar is
black and invisible, so the poster is unchanged.

**On the three white pages:** the name mark and the links are set in #1C1B19 at
full strength, measuring 17.21 to 1. The two outline buttons use a darker gold,
**#8A6410**, which measures **5.37 to 1** on white. A slightly lighter #9A6F0E
would have measured 4.51 and scraped the mark, so the darker value was taken.
The filled Contact button keeps the bright #E2B04A, because there the gold is
the background and its near-black word measures 9.48 to 1.

**On the four dark pages:** white type, which measures between 7.76 and 21 to 1.

**A fault the fix exposed.** With the blend gone, the buttons no longer needed
to sit outside the menu, and the moment the scrim made that outside strip
opaque it was covering the end of the phone number on the home page. The
overlap had been there all along and was invisible while the strip had no
background. The buttons went back inside the menu row, which removed both the
overlap and the hand-set gap that had been reserved for them.

## After

**380 measurements, none below the mark** (the check now covers the footer too).

## Proving the check can fail

The new check is wired into the checker as its sixth test. To prove it works,
the name mark on the white About page was set to a pale grey on purpose. The
check reported four failures, naming the page, the screen size, the scroll
position and the item, and measuring 1.66 to 1 against a mark of 4.5. It exited
with the code that blocks a commit. The colour was put back and it returned to
clean.
