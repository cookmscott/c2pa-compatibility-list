# C2PA Compatibility List
**The public reference for C2PA Content Credentials support across devices, apps, and platforms.**

If you're trying to answer *"does this camera / app / platform support C2PA?"* this is the list. We track real-world support status and short implementation notes across the ecosystem, and update it weekly.

## What's included

We track C2PA Content Credentials support across six categories:

- **Cameras** - hardware support and camera model coverage
- **Smartphones** - phones, mobile rollouts, and related hardware enablers
- **Editing tools** - tools used to create or edit media with C2PA support
- **AI generation tools** - tools that generate media and attach C2PA credentials
- **Publishing platforms** - anywhere you can post, save, store, or share media with C2PA credentials
- **Verification tools** - tools that read, inspect, verify, or display Content Credentials

```json
{
  "cameras": {},
  "smartphones": {},
  "editing_tools": {},
  "ai_generation_tools: {},
  "publishing_platforms: {},
  "verification_tools: {}
}
```

Each entry is intentionally simple and answers the basics:

- what it is
- whether support is live, announced, beta, suspended, or not supported
- what someone should know before relying on it

The JSON source of truth is here:

- [data/c2pa-compatibility-list.json](/Users/scottcook/Documents/side-projects/c2pa-compatibility-list/data/c2pa-compatibility-list.json)

Example:

```json
{
  "cameras": {
    "Leica": [
      {
        "name": "M11-P",
        "status": "Live",
        "notes": "The world's first camera with built-in Content Credentials."
      }
    ]
  },
  "publishing_platforms": {
    "ProofInBio": [
      {
        "name": "ProofInBio",
        "status": "Live",
        "notes": "Cloud Photo Service and Gallery for C2PA images."
      }
    ]
  }
}
```

## Status vocabulary

Every entry uses one of these statuses:

- `Live`
- `Announced`
- `Beta`
- `Suspended`
- `Not Supported`

When support changes or is limited, entries stay conservative and include notes explaining why.

## How it's maintained

The list is updated weekly using a broad scan of primary sources, including:

- manufacturer product pages and press releases
- firmware and software release notes
- official C2PA ecosystem announcements
- developer documentation and SDKs
- platform help centers and support articles
- standards body references and certification lists

This repo is meant to be lightweight, useful, and as up-to-date as possible. It focuses on practical product support rather than broader ecosystem participation.

The category names are intentionally simple. In particular, `publishing_platforms` is broader than just social posting. It includes anywhere people can post, save, store, or share C2PA-enabled media.

## Data files

The compatibility data is available in two formats:

| File | Best for |
|---|---|
| `data/c2pa-compatibility-list.json` | Apps, scripts, and programmatic use |
| `data/c2pa-compatibility-list.csv` | Spreadsheets and quick review |

JSON is the canonical source. CSV is a convenience export for browsing and analysis.

## Contributing

Spotted something missing or out of date? Contributions are welcome. Open an issue or submit a pull request, and please link to a primary source wherever possible.

## Goal

To be the most useful, trustworthy, and complete public reference for one simple question:

