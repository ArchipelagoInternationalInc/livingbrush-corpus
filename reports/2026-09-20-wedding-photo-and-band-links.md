# 2026-09-20, The right wedding photograph, and band links that land

Fifth session of the day, from Builder Task 05.

---

## 1. The wedding band entry, as it now reads in the file

```
{file:'band-wedding.jpg', ar:'1280/720', g:['#8a5d7a','#2a6f7a'], eyebrow:'World Bodypainting Festival',
 title:'Married on the main stage of the World Bodypainting Festival.',
 copy:'', link:'about.html'},
```

The photograph is the 2015 World Bodypainting Festival wedding picture, copied
in at its original size: 1280 by 720, 231 KB. Under the size limit, so it went
in untouched, neither enlarged nor recompressed. The contain fitting is gone,
so it now fills its frame like the other wide band photographs. The eyebrow,
title, empty copy and colours are unchanged.

The old picture stays in the images folder and the About page still uses it.
The About page was not edited.

## 2. The anchors: I was wrong last session, and here is the correction

**Last session's report said the band links pointed at anchors that do not
exist. That was wrong, and the handoff has been corrected.**

The anchors were always there. The event entries are not written into the page
as fixed text; the script builds them when the page opens, and one line of it
sets each entry's name from the data: `sec.id = ev.a`. The data already carried
the names laa, tedx, guinness and skull. Searching the page file for those
names found nothing because they only come into existence when the page runs.
The lesson for next time: on this site, check the page in a browser before
concluding something is missing from it.

**So no ids were added, because none were missing.**

**There was a real fault underneath, though, and it was worse than a missing
name: the links only worked about four times in five.** Because the entries are
built by the script, the browser tries to jump to the anchor before the entries
exist. Tested cold five times, one run stopped near the top of the page instead
of at the section asked for. It was not specific to one link; any of them could
miss.

The fix is to ask for the jump again once the entries are in the page, and once
more after the pictures have settled the layout. Retested thirty-two times
across the four links and two screen sizes: every one landed, with the heading
clear of the fixed menu.

**No entry for the World Bodypainting Festival exists to link to.** There are
five entries for individual festival years, 2010 through 2014, and the wedding
was 2015. None of them is the wedding, and nothing on that page is. Rather than
point at a year that is not the right one, the wedding band still links to the
About page, which does carry the wedding photograph and its caption. Worth
adding a 2015 entry to the events page if Scott wants that link to go there.

## 3. Click test

Every band's Read more was clicked from the home page, at 1920 and at 390.

| Band | Goes to | Result |
|---|---|---|
| The events we founded | events, Living Art America | lands, heading clear of the menu |
| The TEDx talk | events, TEDx | lands, heading clear |
| The Guinness World Record | events, Guinness | lands, heading clear |
| World Bodypainting Festival | About page | arrives, no anchor by design |
| In Voluptas Mors | events, the skull | lands, heading clear |

Repeated afterwards against the live site: all eight anchor tests land clear.

## 4. Checks

The checker passes all five. Commit `ecedc6e`, pushed. Confirmed live: the new
photograph serves at the right size and type, the old one is still in place for
the About page, and the anchor fix is serving.
