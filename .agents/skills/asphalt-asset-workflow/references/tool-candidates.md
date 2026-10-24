# Candidate tools

These are research leads, not bundled dependencies or verified Asphalt converters.
Recorded 2026-10-24; recheck upstream for a concrete task.

| Source | Evidence and use | Limits |
| --- | --- | --- |
| https://github.com/lOlbas/Game-Engines-Filetypes-Reverse-Engineering | Gameloft binary structure templates and reading scripts, including BDAE-related research. Useful for understanding a matching format version. | Work in progress. Check the actual version folder and script. License and compatibility with the user's files are unverified. |
| https://github.com/pixel3rr0r/oac-bdae-parser | C++ parser and OpenGL viewer. README targets Order and Chaos Online 4.2.5a, BDAE version 0.0.0.779. | Do not assume support for Asphalt. No verified game-resource writer in this workflow. Review provenance and licensing before copying code. |
| A9Tool historical lead | Investigate model/texture conversion for historical Asphalt 9 assets. Search upstream author material for a real implementation and exact supported versions. | Source, license, modern compatibility, and repacking support are unverified. Do not install an arbitrary executable merely because its name matches. |

No third-party source is bundled. Failure to retrieve a root LICENSE file does not establish that no license exists; check the complete repository and upstream permissions.

For every tested tool record:
- Upstream URL and pinned commit or release.
- License and required attribution, if incorporating code.
- Game build, platform, format signature and version.
- Input sample hash and invocation.
- Read, export, and write support separately.
- Observed structural validation and limitations.
