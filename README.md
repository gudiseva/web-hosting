# Prep Hub

A small static website that collects interview-preparation and education-research pages into one place, with a landing page (`index.html`) linking to everything.

Designed to be hosted on **[tiiny.host](https://tiiny.host)** (or any static host / GitHub Pages). `index.html` at the repository root is the entry point.

## Structure

The deployable site lives in **`dist/`** (the build/output folder some hosts require). `README.md` and `.gitignore` stay at the repo root.

```
.
├── README.md
├── .gitignore
└── dist/                            # <-- deploy this folder; index.html is here
    ├── index.html                   # Landing page — links to every page below
    ├── interview-prep/              # Career & interview material
    │   ├── Java21-Spring-Tudor-Sagarsoft-Prep.html
    │   ├── Interview-Cheat-Sheet.html
    │   ├── MassMutual_EA_Interview_Prep.html
    │   └── massmutual_full_prep_table.html
    └── education/
        ├── bba/                     # BBA & college options
        │   ├── bba_college_comparison.html
        │   ├── bba_course_comparison.html
        │   ├── bba_deep_comparison_4courses.html
        │   └── bba_distance_pu_vs_ignou.html
        ├── course-comparisons/      # Engineering / applied-science courses
        │   ├── course_comparison.html
        │   ├── four_course_comparison.html
        │   └── three_course_comparison_v2.html
        ├── universities/            # Campus comparisons
        │   └── ou_vs_jntuh_comparison.html
        └── career-paths/            # Specialised career routes
            ├── culinary_arts_usa_careers.html
            └── bvsc_pvnrtvu_guide.html
```

## Hosting on tiiny.host from GitHub

1. Push this repository to GitHub (see below).
2. In tiiny.host, choose **Import from GitHub**, select this repository, and set the
   **publish / build directory to `dist`** so the contents of `dist/` are served at the site root.
3. tiiny.host then serves `dist/index.html` as the home page; every other page is reachable
   from the cards and by direct URL, e.g. `web-hosting.tiiny.site/education/bba/bba_college_comparison.html`.

## Notes

- All pages are fully self-contained (inline CSS, no external build step or dependencies).
- File and folder names are case-sensitive on the host — keep them exactly as committed.
