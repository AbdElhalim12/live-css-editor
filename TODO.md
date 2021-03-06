#### New Features
* Add Emmet (Reference: https://mikethedj4.github.io/kodeWeave/editor/#b9a99b76536392cb5ec5004bc37b8fcc)
* Add Autoprefixer (References: https://github.com/postcss/autoprefixer https://autoprefixer.github.io/)
* Add support for editing and saving the CSS/Less files (back-end would need to support saving those files)
* Add a "copy-to-clipboard" button

#### Improvements
* If there are many small iframes in a page, we may not want to load Magic CSS in all of them (this might be added as a global setting)
* Currently, for the next load, we don't remember if the user had activated line numbers and CSS lint previously. The reasoning behind this is that we try to maximize the code viewability and those might be more of hindrance than use. But that reasoning may not be correct for all users, so we might make change to remember those settings.
* "Reload CSS resources" feature should try to detect and reload @import instructions through <style> and <link> tags
* CodeMirror autocomplete suggestions should have fixed position OR they should not let scroll event pass through to parent-elements/body OR both
* Review if it is possible to fix https://github.com/webextensions/live-css-editor/issues/2 (Changes aren't applied after reload until extension is opened) while keeping security concerns in mind

#### Environments
* Make "editor" a standalone project, so that it can be added to an HTML page as well
* Make "Magic CSS" a standalone project, so that it can be added to an HTML page as well

#### Global settings
* Customize indentation (allow using tab/n-spaces)

#### Compilation and Build
* Add webpack based compilation (currently, it is split into too many files, which increases load time)

#### Refactoring
* Refactor code
* Update all 3rd party libraries to their latest versions
* Move some functionalities into their own projects, for example, generate selectors, get existing selectors, point-and-click etc
* Use Shadow DOM for Magic CSS UI (and remove some code which would not be required after that)

#### Language Support
* Add translations/internationalization

#### Releases
* Add/update the link once it becomes available on store for Opera
