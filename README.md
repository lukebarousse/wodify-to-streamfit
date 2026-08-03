# Wodify → StreamFit Migration Helper

A single-page tool that converts the performance-history export Wodify support sends you
(`UserIdXXXX_PerformanceResults_*.xlsx`) into the two CSV files StreamFit's Wodify importer
actually accepts.

**Use it here: https://lukebarousse.github.io/wodify-to-streamfit/**

Everything runs in your browser — your workout data is never uploaded anywhere.

## Why this exists

StreamFit has a built-in Wodify importer, but three things bite every member who uses it raw:

1. **Dates**: the importer only parses US-style dates (`M/D/YYYY`). ISO dates — including the
   format in StreamFit's own template — silently fall back to the *upload* date, re-stamping
   your entire history to today.
2. **Generic "Metcon" rows** collide with a benchmark section named "METCON", which discards
   each workout's description. This tool gives daily WODs unique names so they import as
   individual workouts with their descriptions intact.
3. **Movement names** must exactly match StreamFit's catalog. The tool detects mismatches
   (complexes, "Snatch" vs "Squat Snatch", EMOMs) and lets you fix them with one click before
   anything is uploaded.

It also folds your comments into workout descriptions (the importer drops the comment column),
filters blank/zero-weight junk rows, and lists rep-based gymnastics PRs the importer can't
handle so you can add them manually.

## Not affiliated

Community tool; not affiliated with Wodify or StreamFit. Movement/benchmark catalog snapshot:
August 2026.
