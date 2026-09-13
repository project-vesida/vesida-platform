# vesida-platform

Part of [Project Vesida](https://github.com/project-vesida). AGPL-3.0. **Roadmap only: no code yet.**

The open catalog. Stations upload angles-only observations as CCSDS Tracking Data Messages; the
platform stores them, serves them, and publishes them under CC BY 4.0.

## What it will do

- **Ingest**: authenticated TDM upload per station, validated against the I-02 contract in
  [opta-pipeline/docs/interfaces.md](https://github.com/project-vesida/opta-pipeline/blob/main/docs/interfaces.md).
- **Catalog**: time-indexed store of tracklets with station, object association, and quality flags.
- **Public API**: query tracklets by time, sky region, object, or station. Read access is anonymous.
- **Dashboard**: stations on a map, nightly counts, sky coverage, per-station health.
- **Open data**: bulk export of the catalog under CC BY 4.0, with attribution to Project Vesida and to the station operator who observed.

Lean by design: one service, one database, a hosting budget of a few hundred francs a year.

## The line between open and commercial

Everything in this repository is open, AGPL-3.0. Downstream products that need observations from
many stations at once, such as multi-station orbit refinement, manoeuvre detection, and conjunction
alerts, are built and sold by the Vesida company. They consume this platform through the same public
API and the same open data as everyone else, and they contain none of this platform's code. The open
layer never depends on the commercial one.

## Roadmap

1. Define the ingestion and public-query contracts.
2. Implement authenticated TDM ingestion and the tracklet store.
3. Publish the API, dashboard, and bulk open-data export.
4. Support independently operated arrays and multi-site products.

## Get involved

Open an issue on this repository. The API design and the dashboard are the first two things a
contributor without a camera can start on.
