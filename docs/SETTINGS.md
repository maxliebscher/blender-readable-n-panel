# Settings and behavior

Open `Edit → Preferences → Interface → Editors → Sidebar Categories (Experimental)`, or right-click the category strip and choose **Sidebar Category Settings…**.

## Display

### Readable Labels

Draws category names horizontally while retaining their vertical stack. Disable it to restore Blender's original rotated labels.

### Width

- **Automatic:** measures visible labels and clamps the result between Minimum and Maximum.
- **Fixed:** uses the selected fixed width regardless of label length.

Very narrow values can truncate labels. Very wide values reduce the remaining sidebar content area.

### Row Height

Scales the height of readable category rows. Small values fit more categories; large values improve click targets but require more scrolling.

## Ordering and organization

### Sort

- **Blender Order:** keeps registration order.
- **Alphabetical:** sorts by the visible label.
- **Custom:** uses the semicolon-separated identifier order from Advanced Sidebar Category Data.

### Favorites First

Moves favorited categories ahead of non-favorites while retaining the selected secondary ordering.

### Group Headers

Displays named groups as compact headings. Click a heading to collapse or expand that group. Ungrouped categories remain usable.

### Color Tags

Shows one of eight native Blender color markers configured for a category. Color changes presentation only; the original add-on category identifier remains unchanged.

### Aliases

Changes only the displayed category name. It does not rename or re-register an add-on's panel category.

### Hidden categories

Removes selected categories from the organizer view. The active category is protected from becoming unreachable; reset remains available in Preferences.

## Search

### Show Search Field

Adds a live search field above the readable category list.

The filter matches:

- the original category identifier;
- its visible alias;
- its group name.

Results update while typing. The clear button restores the full list. The active category remains visible if it does not match, preventing an invisible active state.

## Editing one category

Right-click a category and choose **Organize Active Category…** to edit:

- Display Name;
- Group;
- Color Tag;
- Favorite;
- Hidden.

## Reset and advanced data

**Reset Sidebar Organization** clears aliases, groups, colors, favorites, hidden categories, custom order, and the filter.

**Advanced Sidebar Category Data** exposes the raw semicolon-separated data used by this prototype. It is intended for testing and bulk editing, not as the final manager interface. Invalid identifiers are ignored rather than changing add-on registration.

## Persistence scope

Settings are global to the portable user profile. They are not stored per workspace or per `.blend` file.

