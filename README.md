# Learn VSCode Shortcuts (Mac)

https://code.visualstudio.com/docs/getstarted/keybindings

> Visual Studio Code lets you perform most tasks directly from the keyboard.

Table of Contents

- [Symbols](#symbols)
- [Navigation](#navigation)
- [Display](#display)
- [Editor/Window](#editorwindow)
  - [Split/Focus Editor](#splitfocus-editor)
  - [Move Editor](#move-editor)
  - [Close Editor](#close-editor)
- [Editing](#editing)
  - [Insert/Move Line](#insertmove-line)
  - [Select](#select)
  - [Insert Cursor](#insert-cursor)
- [Add Custom Shortcuts](#add-custom-shortcuts)

## Symbols

- `⌃`: Control
- `⇧`: Shift
- `⌥`: Option
- `⌘`: Comamnd

## Navigation

- `⌘P`: Quick Open
- `⇧⌘P`: Show All Commands (`>`)
- `⌘T`: Show All Symbols (`#`)
- `⇧⌘O`: Go to Symbol (`@`)
  - Type `:` to group symbols.
- `⌃G`: Go to Line (`:`)
- `⌃-`: Go Back
- `⌃⇧-`: Go Forward

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

- `⌘B`: Toggle Sidebar
- `⌘J`: Toggle Integrated Terminal
- `` ⌃` ``: Focus/Toggle Integrated Terminal
- `⇧⌘E`: Show Explorer
- `⇧⌘F`: Show Search
- `⌘K Z`: Toggle Zen Mode

## Editor/Window

### Split/Focus Editor

- `⌥⌘→`: Focus into next editor
- `⌥⌘←`: Focus into next editor
- `⌘\`: Split
- `⌘1`: Focus into first editor group
- `⌘2`: Focus into second editor group

### Move Editor

- `⌃⌘→`: Into Next Group
- `⌃⌘←`: Into Previous Group

### Close Editor

- `⌘W`: This
- `⌘K W`: Group
- `⌘K ⌘W`: All
- `⇧⌘T`: Reopen

### Practice

1. Split this editor twice.
2. Focus into second editor group.
3. Open `code.js`.
4. Move code.js to third editor group.
5. Close third editor group.
6. Close all editor groups.

## Editing

### Insert/Move Line

- `⌘Enter`: Insert Line Above
- `⇧⌘Enter`: Insert Line Below
- `⌥↓`: Move Line Down
- `⌥↑`: Move Line Up

#### Practice

1. Insert a line (cursor here) below and type `3. Done.`.
2. Move this line up.

### Select

- `⌘F + ⌘G`: Select Next
- `⌘D`: Add Selection To Next Find Match
- `⇧⌘L`: Select all occurrences of current selection
- `⌃⌥→`: Move Cursor to next word part
- `⌃⌥←`: Move Cursor previous word part
- `⌃⇧⌥→`: Select to next word part
- `⌃⇧⌥←`: Select to previous word part
- `⌘U`: Undo last cursor operation

#### Practice

1. Select next 😃.
2. Select all 😃 and delete them.
3. 😃R😃e😃m😃o😃v😃e `Not` from `shortcutsWillNotMakeYourMoreProductive`.

### Insert Cursor

- `⌥⌘↓`: Insert Cursor Below
- `⌥⌘↑`: Insert Cursor Above
- `⌥ + click`: Insert Cursor

#### Practice

1. Change first character of the below lines to upper case.
2. remove emojis in the line below with inserting cursor with click.
3. go😂od j🧘🏻‍♂️o🌍b!

## Add Custom Shortcuts

1. Open `Keyboard Shortcurs` with `⌘K ⌘S`.
2. Click `Open Keyboard Shortcuts (JSON)` on the right top corner.
3. Copy & paste the code below in the JSON array.
4. Use `⌃⌥↓` to go to 5 lines below.

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
