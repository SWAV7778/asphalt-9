---
name: asphalt-asset-workflow
description: Inspect Asphalt and related Gameloft game model, texture, and archive files; select compatible extraction or conversion tools and handle Blender editing, rendering, and validated resource replacement. Use for game asset workflows, not gameplay automation or vehicle statistics.
---

# Asphalt asset workflow

## Establish the actual input
Inspect supplied files before asking for information already present. Record game title, exact build, platform, input paths, and requested output: inspection, extraction, conversion, rendering, or replacement. Ask only for missing facts that affect compatibility; continue independent research while waiting.

Treat extensions as hints. Inspect file signatures and version fields, and distinguish archives from models and textures. Never simulate conversion by renaming a suffix. Preserve source bytes and associated texture/material files.

## Match tools to evidence
Read [tool-candidates.md](references/tool-candidates.md) when selecting Gameloft-specific tools. Verify current upstream documentation, license, supported format version, platform, and actual read/write capabilities before adopting a candidate. Pin the tested source revision and retain required license notices when incorporating code.

Keep research candidates, installed tools, and tools tested against the user's sample distinct. Never infer Asphalt compatibility from the Gameloft name or a matching extension. A viewer or extractor is not an exporter or repacker.

If no compatible parser is established, report the header/version evidence and the missing capability. Do not invent proprietary field layouts or claim that a conversion succeeded.

## Process a sample before a batch
Work in a separate output directory. Start with one representative asset and capture tool revision, command, exit status, and output paths. Check output contents, not only successful exit codes. Expand to a batch only after meaningful sample validation.

For Blender work, inspect available capabilities and the current scene first. Use a separate scene or file for imports so existing work is preserved. Validate mesh counts, material assignments, UV layers, normals, hierarchy, skeleton, animation, units, and coordinate axes as applicable. Flag missing textures rather than silently replacing them. Preserve source materials unless changes were requested.

For generic format conversion, select the target based on required features. Reimport the result and compare important structures; report feature loss. For rendering, retain an editable scene when requested, inspect a preview, and then produce the requested outputs.

## Replace only with a verified write path
Before replacement, establish a compatible exporter/repacker and any required path, naming, metadata, compression, and index constraints. Record hashes and back up each target before changing it. Confirm resolved target paths remain within the intended game/resource directory.

Use one reversible replacement first. On a format mismatch or failed validation, stop batch replacement, preserve diagnostics, and restore changed targets from the backup if safe within the authorized scope. Do not overwrite a target that changed after the backup without investigating it.

If a write path is unavailable, finish the achievable extraction/rendering work and clearly identify replacement as unsupported. Do not treat exported FBX/GLB files as game-ready resources.

## Report the result
Reply in the user's language, briefly stating what was inspected or changed, where outputs are, validation performed, and remaining limitations. Distinguish documented support from support actually tested. Do not claim a skill grants new file-format support or installs an external application.
