# Experimental v0.2 QA report

## Isolation

- Developed only in the separate `exp-full` tree on `experimental/full-feature-portable`.
- The Blender upstream pull-request worktree was not modified by the experimental organizer.
- Production Blender 5.1 was not patched, launched, or configured during this work.
- The release profile resolves to `portable/config` inside the extracted package.

## Automated checks

- Native Blender 5.3 Alpha Release build and link completed.
- All 18 organizer RNA properties were present and writable.
- A second Blender process reproduced every stored smoke-test value after restart.
- Conservative release defaults were restored after the persistence test.
- The installed runtime contained zero Git-LFS pointer placeholders.
- The temporary visual-QA startup hook was removed before packaging.
- The final source diff passed `git diff --check` apart from expected local line-ending warnings.

## Release artifact verification

- The final ZIP was extracted into a new short-path verification directory and tested from that extracted copy.
- The extracted portable contained 6,002 files, zero Git-LFS pointer placeholders, and zero internal organizer QA/startup-hook fragments.
- All 18 organizer defaults passed again from the extracted executable; Blender resolved its configuration to the package's own `portable/config` directory.
- ZIP SHA-256: `44EEAE572EC513DC07DFEAF95766F726DB451B016166216BCFA74D52EBC190E0`.
- Full source patch SHA-256: `1B07D25285F49E190789D34434640F5C325BBA414B5625272F822310319B5D07`.

## Publication media verification

- The animated GitHub preview is 800 × 450, approximately 2.1 MB, and uses five short descriptive overlays.
- Contact-sheet and full-size frame inspection confirmed that controls, grouped labels, and the filtered state remain legible.

## Real GUI user journey

Tested through real mouse and keyboard input with a long synthetic category list:

- readable labels remain vertically stacked;
- Favorites, Blender, Look Development, Modeling, and Output headings have consistent spacing;
- the category list scrolls to lower entries and back;
- live search filters during typing without requiring Enter;
- the search clear button restores the list;
- a non-matching active category remains visible;
- the search field can be disabled and re-enabled in Preferences;
- right-click access opens category and global settings;
- organizer settings remain readable in the Preferences window.

## Limits of this QA

This is targeted feature testing, not Blender's full platform, file-format, add-on, render, or regression test suite. It does not establish production readiness and cannot exclude crashes, incompatibilities, or data loss.
