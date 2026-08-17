# Safety and disclaimer

This repository and its downloadable portable build are an **experimental demonstration**, not a production release of Blender.

## Before running it

- Do not open, edit, save, convert, render, or overwrite important files with this build.
- Work only on disposable files or verified copies.
- Keep current backups made with software you trust.
- Keep your normal Blender installation and profile separate.
- Do not configure Windows file associations to point at this build.
- Do not deploy the build in a studio, classroom, render farm, or automated pipeline without independent review and testing.

## Risk

The build is based on Blender 5.3 Alpha and contains native C++ changes. Bugs, crashes, hangs, add-on incompatibilities, preference corruption, incorrect saves, and data loss are possible. Testing reduces risk but cannot prove the absence of defects.

The software and accompanying material are provided in good faith, to the best of the author's current knowledge, as a demonstration of possible user-interface behavior. No guarantee is made that it is correct, complete, secure, compatible, fit for a particular purpose, or continuously maintained.

The GNU GPL's warranty disclaimer applies. To the extent permitted by applicable law, use is at your own risk.

## Isolation

The supplied Windows archive is configured as a portable build. Its Blender preferences are stored under `portable/config` inside the extracted directory. This reduces contact with an installed Blender profile, but it is not a security sandbox and does not isolate files that the user explicitly opens.

Extract the archive to a short local path such as `C:\BlenderSidebarTest`. Deeply nested paths can exceed legacy Windows path limits and prevent Blender resources or Python modules from loading correctly.

Deleting the extracted directory removes the portable program and its local preferences. It does not undo changes already saved to user files.
