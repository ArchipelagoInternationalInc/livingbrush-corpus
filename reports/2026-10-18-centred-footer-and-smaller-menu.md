# 2026-10-18, A centred footer, Home in the menu, and a smaller menu

All seven pages. Live, commits `6d8b3d9` and `d0290c6`.

---

## The footer is centred

Everything in it now sits on the centre line of the page: the name mark, the
four columns as a group, the links inside each column, and the copyright.
Measured on the finished pages, all three land exactly on the centre, 960 at
1920 wide and 195 at 390.

The name mark had to move to its own line above the columns. Left in the same
row it was a flex item like any other, so centring the row put the mark at the
left of the group and pushed the four columns off centre, to 1039 where the
page centre is 960. On its own line, the mark centres and the columns centre.

At phone width the four columns still stack, now centred rather than left
aligned, which is what was asked for and replaces the earlier instruction.

## Home joins the menu

A Home link now sits before Work in the top menu on all seven pages, going to
the home page. One consequence worth knowing: on a phone the menu shows only
the first two links, so where it used to read Work and Record it now reads Home
and Work.

## The three buttons came in again

The gap between them went from 19.2 to **12.8 pixels**, which is 40 per cent of
the 2 rem the menu row uses, down from the 60 per cent set the day before.

A note on what was asked: the request was for the "top 3 left buttons". The top
menu has exactly three buttons and they sit on the right, so these are the ones
that were tightened, on the reading that "a bit more" continues the tightening
done the day before. If the left-hand links were meant instead, that is a one
line change.

## The whole menu is smaller

The menu was asked to be made smaller so it fits. Worth recording that it was
not actually overflowing: measured from 1920 down to 900 pixels wide there was
between 744 and 346 pixels of clear space between the logo and the menu, and
nothing overlapped at any width. So this was a judgement about how it looked,
not a fault, and it was made smaller as asked.

Links and buttons went from 11.5 pixels to **9.9**, the logo from 16 to 14.4,
the space between links and around the menu row from 2 rem to 1.5 rem, and the
button padding in a step. The menu block on the home page went from 951 pixels
wide to 794.

One thing changed from a plain shrink: the interior pages used smaller menu
type than the home page, and scaling everything by the same proportion would
have taken them to 9 pixels, which is too small to read comfortably. All seven
pages are now set to the same 9.9 pixels. That is smaller than before on every
page, and it removes an inconsistency between the home page and the rest.

## Checked

The checker passes all six checks. The contrast check, which reads the real
pixels rather than the stylesheet, now makes 394 measurements across the menus
and footers of all seven pages at both sizes, and none is below the mark.
Confirmed in a browser on the live site: the menu reads Home, Work, Record,
Events, Ideas, About at 9.9 pixels with 12.8 pixel gaps between the buttons and
no overflow, and the footer is four centred columns.
