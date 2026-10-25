# 12 — Export and Import

Status: ready-for-agent
Blocked by: 02
Spec: `../spec.md`

## What to build

In Settings:
- **Export** downloads the Stored Data as a dated JSON file.
- **Import** reads a chosen file, then has the core validate `schemaVersion` and the data's shape. A valid file replaces the Stored Data after a confirmation. An invalid file shows an error and changes nothing.

## Acceptance criteria

- [ ] Core tests: export → import round-trips to identical query results
- [ ] Core tests: malformed JSON, a wrong `schemaVersion` and missing fields are each rejected, with the existing data untouched
- [ ] On the iPhone, Export saves to Files and Import restores from that file
