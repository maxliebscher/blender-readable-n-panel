# Source and release provenance

## License

Blender and this modified build are free software under the GNU General Public License, version 2 or later (`GPL-2.0-or-later`). The repository's complete patch is provided under the same license.

The binary archive retains Blender's standard `license` directory, including notices for bundled dependencies. No proprietary Blender build or closed-source add-on is included by this project.

## Exact source base

- Upstream repository: `https://projects.blender.org/blender/blender`
- Upstream base commit: `4d6a448ec8e203a080b276c34ae73fb91078d088`
- Minimal readable-label reference commit: `6a37f824a4c8af813d987ebd1afaf1f4275df8f1`
- Experimental development branch: `experimental/full-feature-portable`
- Complete patch: `patches/blender-sidebar-organizer-v0.2-full.patch`

The patch is intentionally generated only from the 12 Blender source files involved in the readable-label and organizer implementation. Replaced local Git-LFS working files, build outputs, test profiles, and captured media are excluded from the source patch.

## Reconstructing the source tree

```bash
git clone https://projects.blender.org/blender/blender.git
cd blender
git checkout 4d6a448ec8e203a080b276c34ae73fb91078d088
git apply /path/to/blender-sidebar-organizer-v0.2-full.patch
```

Use Blender's official build documentation for your platform. The provided Windows archive is only one reproducible convenience build from that patched source.

## Relationship to upstream work

The upstream pull request proposes only optional readable labels. Grouping, sorting, aliases, favorites, hiding, color tags, sizing controls, and live search remain experimental and should not be represented as accepted Blender functionality.

The experimental organizer remains separate from the focused upstream pull request and must not be represented as accepted Blender functionality.
