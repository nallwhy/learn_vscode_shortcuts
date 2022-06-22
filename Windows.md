# Learn VSCode Shortcuts (Mac)

https://code.visualstudio.com/docs/getstarted/keybindings

> Visual Studio Code lets you perform most tasks directly from the keyboard.

Table of Contents

- [Learn VSCode Shortcuts (Mac)](#learn-vscode-shortcuts-mac)
  - [Symbols](#symbols)
  - [Navigation](#navigation)
    - [Practice](#practice)
  - [Display](#display)
  - [Editor/Window](#editorwindow)
    - [Split/Focus Editor](#splitfocus-editor)
    - [Move Editor](#move-editor)
    - [Close Editor](#close-editor)
    - [Practice](#practice-1)
  - [Editing](#editing)
    - [Insert/Move Line](#insertmove-line)
      - [Practice](#practice-2)
    - [Select](#select)
      - [Practice](#practice-3)
    - [Insert Cursor](#insert-cursor)
      - [Practice](#practice-4)
  - [Add Custom Shortcuts](#add-custom-shortcuts)

## Symbols

- `ctrl`: Control
- `⇧`: Shift
- `alt`: Alt

## Navigation

- `ctrl P`: Quick Open
- `ctrl ⇧ P`: Show All Commands (`>`)
- `ctrl T`: Show All Symbols (`#`)
- `ctrl ⇧ O`: Go to Symbol (`@`)
  - Type `:` to group symbols.
- `ctrl G`: Go to Line (`:`)
- `alt ←`: Go Back
- `alt →`: Go Forward

**Note:** `Show All Symbols` command can be less usable if your project imports many dependencies. (https://github.com/microsoft/vscode/issues/46718)

### Practice

1. Show all commands.
2. Type 'Open Recent' and run `File: Open Recent...` command.
3. Open any projects.
4. Run `Quick Open` command and type `#` to show all symbols.
5. Go to any function with name (like `deleteUser`).
6. Run `Go to Symbol` command and type `:` to group symbols.
7. Go to any function.
8. Go back.
9. Go forward.
10. Go to line 1.

## Display

- `ctrl B`: Toggle Sidebar
- `ctrl ⇧ P`: Toggle Integrated Terminal
- `` ctrl ` ``: Focus/Toggle Integrated Terminal
- `ctrl ⇧ E`: Show Explorer
- `ctrl ⇧ F`: Show Search
- `ctrl K Z`: Toggle Zen Mode

## Editor/Window

### Split/Focus Editor

- `ctrl \`: Split
- `ctrl 1`: Focus into first editor group
- `ctrl 2`: Focus into second editor group

### Move Editor

- `ctrl alt →`: Into Next Group
- `ctrl alt ←`: Into Previous Group

### Close Editor

- `ctrl W`: This
- `ctrl K W`: Group
- `ctrl ⇧ T`: Reopen

### Practice

1. Split this editor twice.
2. Focus into second editor group.
3. Open `code.js`.
4. Move code.js to third editor group.
5. Close third editor group.
6. Close all editor groups.

## Editing

### Insert/Move Line

- `ctrl ⇧ Enter`: Insert Line Above
- `ctrl Enter`: Insert Line Below
- `alt ↓`: Move Line Down
- `alt ↑`: Move Line Up

#### Practice

1. Insert a line (cursor here) below and type `3. Done.`.
2. Move this line up.

### Select

- `ctrl D`: Add Selection To Next Find Match
- `ctrl ⇧ L`: Select all occurrences of current selection
- `ctrl →`: Move Cursor to next word part
- `ctrl ←`: Move Cursor previous word part
- `ctrl ⇧ →`: Select to next word part
- `ctrl ⇧ ←`: Select to previous word part
- `ctrl U`: Undo last cursor operation

#### Practice

1. Select next 😃.
2. Select all 😃 and delete them.
3. 😃R😃e😃m😃o😃v😃e `Not` from `shortcutsWillNotMakeYourMoreProductive`.

### Insert Cursor

- `ctrl alt ↓`: Insert Cursor Below
- `ctrl alt ↑`: Insert Cursor Above
- `alt + click`: Insert Cursor

#### Practice

1. Change first character of the below lines to upper case.
2. remove emojis in the line below with inserting cursor with click.
3. go😂od j🧘🏻‍♂️o🌍b!

## Add Custom Shortcuts

1. Open `Keyboard Shortcuts` with `ctrl shift p`.
2. Click `Open Keyboard Shortcuts (JSON)` on the right top corner.
3. Copy & paste the code below in the JSON array.
4. Use `ctrl alt ↓` to go to 5 lines below.

```
{
  "key": "ctrl+alt+up",
  "command": "cursorMove",
  "args": {
    "to": "up",
    "by": "line",
    "value": 5
  },
  "when": "editorTextFocus"
},
{
  "key": "ctrl+alt+down",
  "command": "cursorMove",
  "args": {
    "to": "down",
    "by": "line",
    "value": 5
  },
  "when": "editorTextFocus"
}
```
