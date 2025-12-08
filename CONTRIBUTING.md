# Contributing

Thanks for considering a contribution! This guide explains how to open issues and PRs and how to validate changes.

## Workflow
- Fork this repository and create a descriptive branch: `feature/probuilder-element-alignment` or `fix/uv-refresh`.
- Keep commits small and descriptive, e.g., `PBMove: align local axis to element rotation`.
- Open a Pull Request including:
  - The problem it solves (link to issue if available)
  - The approach/summary of the solution
  - Manual validation steps (see below)

## Manual Validation
Before requesting review, validate:
- Unity 2021.3+ in a fresh project with ProBuilder installed.
- ProBuilder with Orientation: Element.
- Test `G`, `S`, `R` with Face/Edge/Vertex selections:
  - Axis lock `X/Y/Z` respects the element axis when Local.
  - UVs and Normals remain stable after applying.
  - Global continues to work as in the original.
- Test with and without snap for `G`/`S`/`R`.

## Code Guidelines
- Keep changes surgical and consistent with the existing style.
- Avoid dependencies on non-public internal ProBuilder types.
- Update documentation when behavior changes.

## Versioning & Release
- Use SemVer (`MAJOR.MINOR.PATCH`). E.g., `0.2.0` for new features and `0.2.1` for fixes.
- Create a tag when publishing a stable release; update `CHANGELOG.md` with date and items.
- For UPM, reference the tag in the URL if desired (`#v0.2.0`).

## Issues
- Prefer descriptive titles, include reproduction steps, Unity/ProBuilder versions, and screenshots/GIFs when possible.
- Use Bug/Feature templates (if available).

## Code of Conduct
- Be respectful and collaborative in discussions and reviews.

Thanks for helping improve the project!