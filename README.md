# GitVersion Usage Example

Example repo to validate our GitVersion usage

## Branching Model

Oveview;

 * current development happens on `master`
 * support / maintenance branches on `release/<major>.<minor>.x`
 * we use `feature/*` or `bugfix/*` topic branches with PR

## GitVersion Usage

How we use it:

 * release versions (e.g. "v0.1.0") are created manually via tag
 * pre-release version (e.g. "v0.2.0-sprint5") are created manually via tag, too
 * we use `gitversion -showvariable FullSemVer` to compute the full version string to be imprinted into our artifacts (e.g. "v0.2.0-sprint5+3")
