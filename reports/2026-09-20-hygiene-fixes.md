# 2026-09-20, Hygiene fixes, and the checker goes green

Second session of the day. Small, approved fixes to clear the faults the
inventory found. No design work, and no new words anywhere except "Contact" on
a button.

---

## What changed

**The About page** had an empty slot waiting for a photograph that was never
delivered. Every visit asked the site for it and got nothing back, which the
browser recorded as an error. The slot is gone.

**The Practice page** had four empty slots for broadcast replays, same problem.
They are gone, and the page is now marked so search engines do not index it.
It stays out of the sitemap on purpose; that was never an oversight.

**All six interior pages** gained a Contact link in the footer, beside the
phone number, pointing at the contact form on the home page. There was already
a Contact button in the menu at the top of each page; this adds one at the
bottom, where someone who has read to the end will look for it.

**The home page** was downloading a typeface it no longer used anywhere. An
italic line under the headline was removed in September, and that line was the
only thing set in it. The typeface, the variable that pointed at it, and the
style rule that used it are all gone. The home page's appearance is unchanged.

## One thing that needed care

Removing the second photograph from the About page nearly broke the first one.
The two sat in a layout that gives the left photograph a wide landscape shape
and the right one a narrow upright shape. With only one photograph left, it was
being given the narrow upright treatment meant for the one that had been
removed, so the surviving photograph rendered squeezed into the right-hand
column with an empty gap beside it.

This was caught by looking at the page rather than by trusting that the
checker's green tick meant it looked right. The layout now recognises when only
one photograph is present and gives it its proper landscape shape at full
width. Measured afterwards at both screen sizes: the photograph renders at its
intended 3:2 proportion.

Worth stating plainly, because it is the general lesson: the checker confirms
that nothing is broken mechanically. It has no idea whether a page looks right.
Only a person looking at it knows that.

## The checker

It now passes, with all five checks clean and no errors in the browser on any
of the twelve page and screen-size combinations tested. Before this session it
failed on five missing images, which was the correct result.

## Confirmed on the live site, not just locally

The About page now loads with nothing in the error console. The new Contact
link was clicked in a real browser: it lands on the home page and scrolls the
contact form into view. The Practice page carries its no-index instruction. The
home page no longer requests the unused typeface.

## Waiting on Scott

**One sentence on the About page no longer matches what is above it.** The
caption reads: "Married on the main stage of the World Bodypainting Festival,
beside an early festival painting." The second half described the photograph
that has been removed. It was left exactly as written, because changing a
public sentence without Scott's words is not the Builder's call. Three ways
forward: supply the missing photograph, shorten the caption, or leave it.

**Nothing has been deleted from the image library.** Ten images exist that no
page asks for, about 2.5 MB. Clearing them is Phase 3, and the list should be
rechecked at the time rather than trusted from today.
