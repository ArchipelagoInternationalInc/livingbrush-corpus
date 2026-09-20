# 2026-09-20, Homepage copy, and making the phone read properly

Third session of the day. Two approved copy changes on the home page, then a
sweep of how every public page reads on a phone.

---

## The copy, in Scott's words

The Our Unique Standing paragraph now opens "achieved a Guinness World Record"
rather than "hold a", and ends at "This is the living archive of that work."
The bold on Guinness World Record and TEDx talk is unchanged.

The block above it gained a sixth statement, about the bodypainting events
co-founded within the Arnold Schwarzenegger Sports Festivals and the Olympia in
Spain, South Africa and the US. The whole block is now set in the same gold as
the phone number in the menu.

## What was wrong on the phone, and why

Every headline on this site is built one line at a time. Each hand-chosen line
sits in its own box so it can be slid up into place when you scroll to it. That
is what produces the reveal effect on a wide screen.

On a phone those boxes do not go away. The hand-chosen break stays, and the
screen adds its own wrapping on top of it. So a headline written as three lines
became six, with single words stranded on rows of their own.

Measured before the fix, at a 390 pixel wide screen:

| Page | Lines that broke a second time |
|---|---|
| Home | 8, counting the hero, the gold block and the record heading |
| Work | 3 |
| Record | 2 |
| Ideas | 2 |
| About | 2 |
| Events | none |

Read on the phone, the home page hero said: "The only bodypainting / artists /
in history to win all five / world / championship titles". The About page said
"We have spent our / lives inside / the oldest art form on / earth." The
descenders on "championship" were also being clipped, because the box each line
sits in is sized for one line and hides anything taller.

## The fix

Below 861 pixels the lines flow together as ordinary paragraph text, the slide
is switched off, and the script skips the reveal at that width so nothing is
left depending on a movement that is no longer going to happen. Headlines and
the home page's centred blocks centre. Body paragraphs on the interior pages
stay left, because long text is easier to read that way.

Nothing about the wide-screen layout changed. Checked afterwards at 1920 by
1080: the lines are still separate boxes, still left aligned, still animate.

## Antarctica, which needed a different answer

The brief asked for the text to sit on the sky above the horizon, and said that
if the photograph was too short on a phone, to put the text on black beneath it
instead.

It is too short. At phone width the photograph is about 175 pixels tall and the
text is five lines. Before the fix it ran straight across the horizon and the
figure, and its final line was cut off at the bottom edge of the image. There
is no position on that photograph where five lines fit above the horizon. So
the text moved to black directly beneath it. The photograph is now fully
visible for the first time on a phone.

## One thing I expected to find and did not

The events collage looked in the screenshots as though images were being cut
off at both edges of the screen. Measured, they are not: the whole collage sits
between 8 and 385 pixels on a 390 pixel screen. What looks like clipping is the
photographs overlapping each other, which is how that piece is designed. No
page scrolls sideways. The gallery arrows also sit inside the screen.

## Checked afterwards

The checker passes on all five of its checks. The live phone view was then
opened in a real browser: the hero flows as one centred paragraph with no
forced breaks, the six-line block is present and gold, no errors in the
console, and the page does not scroll sideways.

## For Scott to decide

On the interior pages the small label above each headline, the one reading
things like "06 / About. The Artists", stays left while the headline itself
centres. The brief said to centre the page headlines only, so that is what was
done. It may look unbalanced. Centring the label as well is a one line change
if that reads better.
