# 2026-09-20, Setup, inventory and studio scaffolding

Covers everything done on the LivingBrush site on September 20, 2026, across
four working sessions: getting the repo onto Scott's Mac, repairing the live
site, taking an inventory for the Project Manager, and installing the studio's
working scaffolding.

---

## What was wrong, and what fixed it

The site had been published in September by dragging files onto GitHub's upload
page. That upload carried the seven pages but not ten smaller files: the
favicon set, the social share image, the web app manifest, robots.txt and
sitemap.xml. It also carried an older version of all seven pages.

Nothing errored. The site simply had no favicon, no picture when a link was
shared, and no link to Madelyn's site, and there was no way to notice from
looking at it.

Fixed by syncing the current files from Scott's working folder and pushing
them. Verified afterwards by asking the live site for each file and checking
what came back: all ten now return a real file of the right type and size, and
all seven pages carry the favicon links, the share tags and the Madelyn link.

## Tidying that followed

Nine copies of the site existed on the Desktop. Two were byte-for-byte
identical to the repo, so they were moved to the Trash after checking that
every file in them, including one that only existed in an older commit, could
be recovered from the repo's history. The rest are earlier iterations and were
left alone.

The design specs, page copy decks and the original page templates had been
living only on the Desktop, with no version history and no backup. They are now
in the repo under `docs/`, and kept off the live site.

## The inventory, and three corrections to it

The Project Manager asked for a plain inventory. It was produced, and then
three of its claims turned out to be wrong. All three came from the same
mistake, and it is worth recording because the next person will hit it too.

**This site does not reference images the ordinary way.** There is no
`<img src>` for most of them. A filename sits in a `data-file` attribute, or is
built in JavaScript, and a small script turns it into a real request when the
page loads. A search for `src=` finds almost nothing and reports a false clean
bill of health.

The three corrections:

1. A fourteenth event image was reported missing. It is not. The fourteenth
   entry names its own file instead, and the numbered pattern is only a
   fallback when an entry does not.
2. A thirteenth event image was then reported as unused. It is not. The
   homepage has its own separate list of thirteen events and asks for all of
   them. This also explained a stray request that could not be accounted for
   earlier.
3. The interior pages were reported as having no way to make contact. They all
   have a Contact button in the menu. That claim came from searching only for
   email addresses.

What is genuinely true: five images are referenced and do not exist, one on a
public page, and ten images exist that nothing asks for. Nothing was deleted.

## The scaffolding, installed today

- An orientation file and a master plan with four phases, each ending at a gate
  where Scott signs off from screenshots and the live site.
- A public reports notebook, which is this repository.
- A checker, `scripts/verify.sh`, with five mechanical checks: no em dashes, no
  email address written into a page, every image a page asks for actually
  exists, the sitemap lists exactly the six public pages, and every public page
  opens in a real browser at desktop and phone size with nothing in the error
  console. It saves screenshots for Scott to judge by eye. It has no opinion
  about how anything looks.
- A session-end guard that will not let a session finish unless the repo is
  clean and pushed, the handoff file was updated, and a report like this one is
  filed, listed in the index, and pushed.

The checker was proved capable of failing before it was trusted: an em dash was
put into a page on purpose, the checker reported exactly that one problem, and
the page was returned to its original state, confirmed by comparing its
fingerprint before and after.

## Where it stands tonight

The checker does not pass yet, and that is the correct result. It reports the
five missing images described above. Removing those dead slots is the next
session's job, and the checker should pass cleanly afterwards.

## Two things Scott should decide

1. The site has no contact address in its text on purpose: the forms assemble
   it in JavaScript so that address harvesters cannot read it. The side effect
   is that a visitor with JavaScript turned off has no way to make contact.
   That should be a deliberate choice rather than a side effect.
2. The original artwork, including the layered files the site images were cut
   from, exists in one folder on one Mac and is in no repository or backup.
   Every future re-crop depends on that folder surviving.
