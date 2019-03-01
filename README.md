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
 * we use `gitversion -showvariable FullSemVer` to compute the full version string to be imprinted into our artifacts (e.g. "v0.2.0-sprint6+19")

Examples:

 * "v0.1.0" is the (tagged) release version v0.1.0
 * "v0.2.0-sprint5" is the (tagged) v0.2.0 pre-release for the sprint 5 demo (we are still working towards v0.2.0)
 * "v0.2.0-sprint6+19" is an ordinary (untagged) CI build, working towards the v0.2.0-sprint6 pre-release and 19 commits ahead of the previus v0.1.0 release