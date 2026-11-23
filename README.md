# duchamp LineageOS OTA feed

Public OTA feed for the POCO X6 Pro 5G / Redmi K70E (`duchamp`) LineageOS
23.2 builds.

## Files

* `lineage-23.2.json` — legacy Updater feed (`{"response": [...]}`), used by
  builds from before 2026-05-29, including the last public 2026-04-29 build.
* `v2/duchamp.json` — current Updater feed (`api/v2`), used by current
  lineage-23.2 builds.

The OTA zip itself is attached to a GitHub release, not committed here.

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
