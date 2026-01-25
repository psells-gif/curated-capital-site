# Curated Capital Operating System

An internet-native operating system for running Curated Capital—everything coded, version-controlled, and interconnected.

## Structure

```
curated-capital-os/
├── index.html              # Dashboard/command center
├── strategy/               # Roadmap, brand, competitive analysis
├── operations/             # Policies, procedures, checklists
├── finance/                # Financial model, projections
├── product/                # Specs, designs, research
├── marketing/              # Copy, assets, campaigns
├── tasks/                  # Active, backlog, parking lot
├── team/                   # Directory, meetings, handoffs
├── legal/                  # Entity docs, licenses, contracts
└── assets/                 # Documents, templates, archive
```

## Deployment

This is deployed as a subdomain via Vercel:

**URL:** ops.curatedcapital.com

### Setup Steps

1. Push this folder to GitHub (or add to existing repo)
2. In Vercel dashboard, create new project or add to existing
3. Set root directory to `curated-capital-os`
4. Add domain: `ops.curatedcapital.com`
5. Configure DNS (A record or CNAME to Vercel)

## Design Principles

1. **Everything is a web page** — HTML/CSS/JS, viewable in browser
2. **Everything links** — Policies reference procedures, tasks link to specs
3. **Single source of truth** — One place for each thing
4. **Version controlled** — Git for history
5. **Mobile accessible** — Responsive design throughout
6. **Searchable** — Global search across all content
7. **Printable** — Clean print styles when needed

## Entity Information

- **Legal Entity:** Project Indigo LLC (EIN: 41-3646660)
- **DBA:** Curated Capital
- **Corporate Domain:** IndigoOps.com
- **Customer Domain:** CuratedCapital.com

---

*Your collection is capital.*
