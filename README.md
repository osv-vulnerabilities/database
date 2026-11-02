# OSV Vulnerability Database Mirror

A daily mirror of [OSV](https://osv.dev/) vulnerability data sourced from the
[`gs://osv-vulnerabilities`](https://storage.googleapis.com/osv-vulnerabilities)
Google Cloud Storage bucket.

## Purpose

Engineers working in environments where access to Google Cloud Storage (GCS) is
restricted can use this repository to download pre-packaged vulnerability
datasets via standard GitHub Release assets — no GCS access required.

## Available datasets

| Ecosystem | Source URL |
|-----------|-----------|
| Maven | `https://storage.googleapis.com/osv-vulnerabilities/Maven/all.zip` |
| npm | `https://storage.googleapis.com/osv-vulnerabilities/npm/all.zip` |
| Wolfi | `https://storage.googleapis.com/osv-vulnerabilities/Wolfi/all.zip` |

## Downloading the latest artifacts

Go to the [**Releases**](../../releases/latest) page and download the asset(s)
you need:

- `maven-all.zip` — all Maven advisories
- `npm-all.zip` — all npm advisories
- `wolfi-all.zip` — all Wolfi advisories

Direct link to the latest release:
```
https://github.com/osv-vulnerabilities/database/releases/latest
```

## Release cadence

The workflow runs automatically every day at **04:00 UTC** and can also be
triggered manually via `workflow_dispatch`.  
Only a **single release** is kept at any time; each run replaces the previous
one. Release tags follow the pattern `1.0.0-YYYYMMDD` (e.g. `1.0.0-20260625`).

## License

See [LICENSE](LICENSE).
