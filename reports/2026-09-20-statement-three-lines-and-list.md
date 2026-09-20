# 2026-09-20, Three statements, and a quieter list beneath them

Home page only. Live.

---

## What is on the page now

Three statement lines, unchanged in size and gold:

1. Five distinct disciplines. Five separate levels of mastery.
2. We won a sweep of first-place victories in each and every category in only four years.
3. Top honors at competitions and events all over the globe.

Then a bulleted list, smaller, in the same gold:

- We co-founded the largest bodypainting competition event in the Western Hemisphere.
- We co-founded bodypainting events within the Arnold Schwarzenegger Sports Festivals and the Olympia in Spain, South Africa, and the US.
- We founded the first international bodypainting film festival.
- We created the first event to combine opera with bodypaint, and the first combining bodypainting with fire performance.

The forced break after "competition event" is gone. Every item wraps wherever
the width happens to put it.

## The numbers, measured on the finished page

At 1920 wide the three lines are 28.8 pixels and the list is 20.16 pixels,
which is exactly seven tenths. The list is 900 pixels wide and its left edge
sits at the same place as the text above it. The gap above the list is 1.8
times the list's own line height, and the gap between items is half of it, both
set in units tied to the list's type size so they hold at any width.

The bullet sits outside the text, so where an item runs to a second line that
line starts under the first word rather than under the bullet. The marker is a
round dot, not a dash. The colour is #E2B04A throughout, the same as the lines
above. No grey.

## On a phone

The three lines stay centred, as they were. The list keeps its text left so the
bullets line up under one another, and the block itself sits in the same column
as everything else. Measured at 390 wide: the list is 313 pixels, the same as
the text above it and aligned with it, items run to one or two lines, every
bullet sits on the same left edge, and the page is exactly as wide as the
screen.

## One change from the starting values

The brief suggested capping the list narrower than the lines above so it reads
as a separate block, which is right on a wide screen and is what was done: 900
pixels against the 974 of the lines above.

On a phone that idea does not transfer. A first attempt carried a narrow cap
down to the small screen and squeezed the list into a 169 pixel column, where
every item broke into three or four short lines and read like a column of
fragments. The cap is now lifted below 861 pixels and the list uses the same
column as the rest of the text. Caught by looking at the screenshot rather than
by any check, which is the point of looking.

## Checked

The checker passes all five. No em dashes anywhere. Commit `df00efd`, pushed
and confirmed live at both sizes: seven tenths the size, 900 pixels wide on
desktop, aligned with the text above, gold, and no errors in the console.
