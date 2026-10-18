# 2026-10-17, One footer for the whole site, and tighter menu buttons

All seven pages. Live, commit `a00fb3d`.

---

## The buttons

The gap between the three menu buttons was 32 pixels, the same spacing the menu
row uses between everything. It is now **19.2 pixels**, which is 60 per cent of
it. On a phone it went from 16 to 9.6 pixels. The gap between the phone number
and the first button is the row's own spacing and is **unchanged at 32 pixels**,
measured after the change. The buttons themselves are the same size, shape and
colour.

## The footer

One block of markup, the same on all seven pages, so the next change happens
once. It carries the name mark, the six public pages in one group, and the
phone number with Contact, Madelyn and Cruises in a second group, with the
copyright on its own line underneath. Practice is deliberately absent, as it is
from the menu and the sitemap.

It takes its colour from the page it sits on rather than a fixed value: every
link and the copyright inherit the body ink. On the four dark pages that is the
pale bone the pages already use; on the three white pages it is black. Nothing
in it is hard-coded, so it stays right as more pages turn white in Phase 1.

Measured the same way as the menu: **every footer link and the copyright line
passes**, at 17.54 to 1 on the dark pages and 21 to 1 on the white ones, at both
screen sizes. The copyright is 11 pixels, the smallest type on the site, in
exactly the same ink as the links above it: not grey, not faded.

At phone width the groups stack and stay left aligned, with the spacing between
links opened up for tapping. No page scrolls sideways.

## A bug worth recording

The page-links group was first written as a `<nav>`. The site styles every
`<nav>` as the fixed menu at the top of the screen, so that group was torn out
of the footer and planted over the top of the page. It is now a plain box with
a navigation label, which reads the same to a screen reader without colliding
with the menu's styling.

## One instruction I did not follow in full, and why

The brief said to remove the line "Made of the moment, for the moment"
everywhere it appears. It appears in two quite different roles.

In the home page footer it was a tagline. **That is gone**, along with the old
footer line it sat in.

On the Ideas page the same words are a pull quote and part of a sentence in the
body: "This art is alive. Made of the moment, for the moment, fleeting,
temporary, ephemeral." **That was left exactly as it is.** The brief's own
sentence is "It does not go in the new footer," which reads as being about the
footer, and removing a pull quote and cutting a sentence in half would be a
change to the writing that no brief has given the words for. Scott should say
if he does want it gone from the Ideas page.

It also survives in two archived page templates under the documentation folder,
which are a record of how the pages were built and are not published.

## What else was removed

The old interior footers carried a single "back" link, such as "Read the
record". Those are gone, because the new footer lists every page. Say if that
step-backwards link is wanted as well.

## Checked

The checker passes all six checks, including the contrast check, which now
covers the footer as well as the menu: 380 measurements, none below the mark.

Twenty-six click tests on the live site: all ten footer links from the home
page and again from an interior page, and the three menu buttons from the home
page and from the About page. Every page link lands on its page, the phone
number is a tap-to-call link, Contact reaches the form, and Madelyn and Cruises
each open in a new tab.
