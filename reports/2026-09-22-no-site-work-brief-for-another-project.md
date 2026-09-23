# 2026-09-22, No site work: the brief belonged to another project

Short record. **Nothing on the LivingBrush site was changed today.**

---

## What happened

A brief arrived asking for database work: verifying a hosted practice database,
loading a schema into it, retiring a local throwaway database, proving a
destructive-delete guard still refuses to run against the live database, and
running four measuring scripts.

None of that belongs to this project. It is CheckThenFix work, and it was
pasted into a session opened on the LivingBrush website repository.

## How that was established, rather than assumed

This repository was checked for every item the brief named. It holds none of
them: no database folder, no migrations, no test harness file, and none of the
four scripts. It contains no TypeScript files at all. The CheckThenFix
repository is not cloned anywhere on this Mac.

The step that would have done real damage was the last one, which asked for the
project's orientation file to be rewritten to describe a database. Applied
here, that would have overwritten the LivingBrush orientation file with another
project's notes, and the next session would have read it and believed it.

## Noted for whoever picks the real work up

That session needs the CheckThenFix repository cloned first. On this Mac the
secrets tool is installed, but the database command-line tool is not, and
neither is anything that can run TypeScript files, so the four measuring
scripts could not run here even with the right repository present.

Its report belongs in the CheckThenFix notebook, not this one.

## State of the site

Untouched and healthy. The repository is clean and level with its remote. The
statement block work filed on 2026-09-20 is live and unchanged.
