# duchamp LineageOS OTA feed

Public OTA feed for the POCO X6 Pro 5G / Redmi K70E (`duchamp`) LineageOS
23.2 builds.

## Files

* `lineage-23.2.json` — legacy Updater feed (`{"response": [...]}`), used by
  builds from before 2026-05-29, including the last public 2026-04-29 build.
* `v2/duchamp.json` — current Updater feed (`api/v2`), used by current
  lineage-23.2 builds.

The OTA zip itself is attached to a GitHub release, not committed here.

## Releases

Releases are numbered `1.0`, `2.0`, … in the order the previous maintainer used;
this repository continues the series with `9.0`.  One release carries one build:

```
Release 9.0
└── lineage-23.2-YYYYMMDD-UNOFFICIAL-duchamp.zip
    https://github.com/filco/duchamp-linageos/releases/download/9.0/<zip-name>
```

The tag is created when the release is published and must not move once a feed
entry points at it.  A release asset is limited to **2 GiB** by GitHub; bigger
zips have to be hosted elsewhere and linked from the release description.

The feeds are committed only after the asset URL answers HTTP 200: the Updater
does not tolerate a feed entry whose package is missing.

## Regenerate

```sh
/home/mio/rom/work/build/publish.sh \
  /home/mio/rom/dist/lineage-23.2-YYYYMMDD-UNOFFICIAL-duchamp.zip \
  https://github.com/filco/duchamp-linageos/releases/download/<tag>/<zip-name>
git add .
git commit -m "OTA: lineage-23.2-YYYYMMDD"
git push origin main
```

## Updater URL

```
https://raw.githubusercontent.com/filco/duchamp-linageos/main/v2/duchamp.json
```

Legacy feed for the 2026-04-29 build:

```
https://raw.githubusercontent.com/filco/duchamp-linageos/main/lineage-23.2.json
```
