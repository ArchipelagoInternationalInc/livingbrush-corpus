# 2026-10-18, The wordmark face across the menu and the footer

All seven pages. Live, commit `3eafff2`.

---

## What changed

The menu and the footer are now set in **Barlow Condensed**, the face the
LivingBrush wordmark uses on the home page. That covers the name mark, the menu
links, the three buttons, the phone number, and in the footer the wordmark, all
the links and the copyright line.

Before this they were in three different faces depending on the page: the home
page used Montserrat for its menu, and the six interior pages used Geist Mono
for theirs and Fraunces for the wordmark. The site's furniture now reads as one
voice whatever a page's body type is. It is held in a single named value, so
changing it later is one line per page rather than ten.

**The six interior pages were not loading Barlow Condensed at all.** They asked
for Fraunces, Inter Tight and Geist Mono only, so simply naming the face would
have fallen back to Arial Narrow on six of the seven pages. They now request
it, at the weights actually used.

## The footer wordmark

It was on its own line above the columns, which made it read as a heading over
them. It now sits at the left of the same row as the columns, as one element
beside them. On a phone, where the columns stack and there is no left side to
sit on, it centres with everything else.

The footer type came down a step so the wordmark does not dominate: the
wordmark from 16.8 to **12.8 pixels**, the links from 12.8 to **10.56**, and
the copyright from 11 to **10**. The wordmark is now close enough to the link
size to read as part of the same group.

## The contrast check had to be rebuilt

The check reads the real pixels rather than the stylesheet. With the menu type
now smaller and in a condensed face it started reporting failures, so the first
job was to find out whether they were real.

They were not. Measured directly: on a menu button at 9.92 pixels the true ink
covers **0.23 per cent** of the button. The letters are thin and antialiasing
smears their colour across dozens of near shades, so no single exact value was
common enough to clear the check's threshold, and it was reading the background
as though it were the text.

The method was wrong rather than the threshold. It now takes the pixels
furthest from the background in brightness, the top one per cent of the box,
and averages them. That is the core of the letters at any type size, and
averaging a band rather than trusting one value keeps a stray pixel from
standing in for the text. It reads slightly low, because the average includes
some antialiased edge, which is the safe direction: it under-reports contrast
rather than over-reporting it.

Because the method changed, the check was proved again: a pale grey name mark
planted on the white page was caught at 1.66 to 1 against a mark of 4.5, on
both screen sizes and both scroll positions, and it exited with the code that
blocks. Restored, it went clean.

## Checked

All six checks pass. 394 contrast measurements across the menus and footers of
all seven pages, at both sizes, none below the mark. Confirmed on the live site
across four pages: every piece of menu and footer text is Barlow Condensed, and
the wordmark sits to the left of the columns on the same row.

## One number worth watching

The Madelyn button on the white pages now measures 4.76 to 1 against a mark of
4.5. The true figure for that gold on white is 5.37; the reading is lower
because the averaging includes antialiased edge. There is room, but not much.
If the menu type is made smaller again, that button is the one that will fail
first, and the answer then is a darker gold rather than a looser check.
