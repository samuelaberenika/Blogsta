# Blogsta 🎙️

A single-repo podcast setup - store your episodes, artwork and metadata in one place and automatically generate a valid RSS feed with every push.

Blogsta keeps everything simple: you write your podcast data in a `feed.yaml` file, and a Python script (`feed.py`) generates `podcast.xml` from it. No CMS, no XML editing, just YAML and Git.

---

## How it works

1. Add your audio files to `audio/` and artwork to `images/`
2. Update `feed.yaml` with your episode details
3. Push to `main` - the GitHub Actions workflow runs `feed.py` and outputs a fresh `podcast.xml`
4. Host via GitHub Pages and point any podcast app at your feed URL

---

## Repo structure

```
Blogsta/
├── .github/workflows/   # GitHub Actions workflow
├── audio/               # Episode audio files
├── images/              # Episode and podcast artwork
├── feed.yaml            # Podcast metadata (edit this)
├── feed.py              # Python script that generates the RSS feed
├── podcast.xml          # Generated RSS feed (don't edit manually)
└── README.md
```

---

## Want to use this in your own repo?

Check out **[Blogsta-Cloner](https://github.com/samuelaberenika/Blogsta-Cloner)** - a reusable GitHub Action built from Blogsta's feed generation logic. Drop it into any repo and get the same YAML-to-RSS pipeline without setting anything up from scratch.

---

## Built with

- Python
- GitHub Actions
- YAML (because XML got old fast)

---

## License

MIT
