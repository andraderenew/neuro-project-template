# Neuroimaging Project Template

A reusable GitHub template for small, reproducible neuroimaging and
electrophysiology projects.

The repository provides a lightweight structure for documenting data
provenance, analysis methods, software versions, quality control, results,
limitations, and citation information without committing raw research data.

## Intended use

Use **Use this template** on GitHub to create a new repository, then replace
the project-specific placeholders before considering that repository
complete.

Suitable examples include:

- structural MRI
- diffusion MRI
- task and resting-state fMRI
- PET
- EEG
- MEG
- graph/network analyses

The template is deliberately software-agnostic. Projects may use tools such
as FreeSurfer, FSL, SPM, CAT, MRtrix3, MNE-Python, EEGLAB, FieldTrip,
Brainstorm, BRAPH, MATLAB, Python, R, or other appropriate software.

## Repository structure

```text
.
├── README.md
├── DATA_SOURCES.md
├── CITATION.cff
├── LICENSE
├── docs/
│   └── index.md
├── env/
│   └── TOOL_VERSIONS.md
├── reports/
│   └── report.md
└── results/
    ├── figures/
    └── tables/
```

## New-project checklist

After creating a repository from this template:

1. Replace the README with the actual scientific question and project scope.
2. Document the dataset, subset, access conditions, and provenance in
   `DATA_SOURCES.md`.
3. Record the versions actually used in `env/TOOL_VERSIONS.md`.
4. Update `CITATION.cff` with the new repository title and URL.
5. Document preprocessing, analysis, statistics, QC, and limitations.
6. Add only lightweight reproducible outputs to `results/`.
7. Do not commit restricted, identifiable, or unnecessarily large raw data.
8. Verify all quantitative claims against generated outputs before release.
9. Run `git diff --check` and review the complete tracked file list.
10. Create a release only when the repository represents a stable,
    documented state.

## Data policy

Raw neuroimaging or electrophysiology datasets should normally remain
outside Git.

Public datasets should be referenced by their authoritative source,
accession, DOI, or URL. Restricted datasets should document the access
requirements without redistributing restricted material.

The `.gitignore` provides conservative defaults, but every project should
review it because legitimate small example files or derivatives may need to
be tracked intentionally.

## Reproducibility principles

A project created from this template should make clear:

- exactly which data were used;
- which transformations were applied;
- which software versions produced the results;
- which outputs support the reported claims;
- what was independently validated;
- what remains a limitation.

Passing a software command or validator is not, by itself, evidence that a
scientific result is correct.

## Automation

This template intentionally does **not** propagate files, releases, or
changes automatically to other repositories.

Each project is maintained and reviewed independently.

## GitHub Pages

`docs/index.md` can be used as the project landing page when GitHub Pages is
enabled for the generated repository.

## License

The template code and documentation are provided under the MIT License.

Individual datasets and third-party software retain their own licenses,
terms, and citation requirements.
