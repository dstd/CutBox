<p align="center">
  <img src="CutBox/CutBox/GraphicAssets/cutbox-icon.png">
</p>

<p align="center">
  <a href="https://github.com/ocodo/CutBox/releases/download/1.4.0/CutBox.dmg"> <img src="https://img.shields.io/github/release/ocodo/CutBox.svg" alt="CutBox"/> </a> &nbsp;
  <img src="https://img.shields.io/github/commits-since/ocodo/CutBox/latest.svg" alt="Github commits (since latest release)"/> &nbsp;
  <a href="https://github.com/ocodo/CutBox/releases/download/1.4.0/CutBox.dmg"> <img src="https://img.shields.io/github/downloads/ocodo/CutBox/latest/CutBox.dmg.svg" alt="Latest release"/> </a>
&nbsp;
  <a href="https://gitter.im/CutBox/Lobby" title="Chat about CutBox"/><img src="https://badges.gitter.im/cutbox/CutBox.png"/></a>
  &nbsp;
  <a href="https://www.codacy.com/app/jasonm23/CutBox?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=cutbox/CutBox&amp;utm_campaign=Badge_Grade"> <img src="https://api.codacy.com/project/badge/Grade/1e2514342ff44f24ab5e2eb8c79f4f2b"/> </a>
</p>

<div align="center">
  <h1>CutBox</h1>
  <p>it'll make your pasteboard awesome!</p>
</div>

## About CutBox

CutBox keeps your pasteboard cut/copy history and lets you paste
anything back to your current app by searching for items.

Inspired by [JumpCut](https://github.com/snark/jumpcut) & [Flycut](https://github.com/TermiT/Flycut)

![](CutBox/CutBox/GraphicAssets/cutbox-search-bar.png)

What does it do? Let's you search from your pasteboard history....

![](CutBox/CutBox/GraphicAssets/cutbox-search-fuzzy.png)

What else...

- Make items favorite
- Select and paste multiple items as one

Anything else?

- You can send your pasted text through [Javascript functions](https://github.com/cutbox/CutBox/wiki/Javascript-support)

# Download / install...

You can find the latest release here: https://github.com/ocodo/CutBox/releases/latest

After downloading, open **CutBox.dmg** and drag **CutBox.app** to **/Applications**

To run, open **/Applications** (Cmd + A in Finder) and double click **CutBox**

**Please note:** Macos will give a security warning, that it was built
by an unidentified developer.  [I'm that developer!](https://github.com/jasonm23)

CutBox is Free OpenSource software. It isn't available via Apple's AppStore.

## Using CutBox

Any text you copy on MacOS is saved to CutBox's history.

![](CutBox/CutBox/GraphicAssets/cutbox-menu.png)

CutBox Search is activated using a global hotkey:

<kbd>**Cmd**</kbd> + <kbd>**Shift**</kbd> + <kbd>**V**</kbd>

(This can be customized in preferences.)

### Searching and pasting

![](CutBox/CutBox/GraphicAssets/cutbox-search-fuzzy.png)

When you activate CutBox you can search for anything copied, just type
what you're searching for or navigate with the arrow keys (or
mouse/trackpad).

Press <kbd>**Enter**</kbd> and the selected item will paste into your
current app.

You can exit without pasting, just press <kbd>**Esc**</kbd>.

If fuzzy matching isn't specific enough for you, regexp matching is
also available.

![](CutBox/CutBox/GraphicAssets/cutbox-search-mode.gif)

Press <kbd>Cmd</kbd> + <kbd>s</kbd> to toggle through search modes,
fuzzy match, regexp/i or regexp.

# Would you like to know more?

I'm moving more help and information to the project wiki, [read more...](https://github.com/cutbox/CutBox/wiki)

# Bugs...

If you find a bug I'd love to hear about it, [click here to tell me
what happened.](https://github.com/cutbox/CutBox/issues/new?template=ISSUE_TEMPLATE.md)

# Would you like CutBox to do something?

If you have an [idea for a new feature please let me know
here](https://github.com/cutbox/CutBox/issues/new?template=feature.md)

# Developers

If you'd like to contribute to CutBox development, please follow the guidelines below.

- Pull requests should be covered by tests (Quick/Nimble or XCUITest)
- Code must pass the quality checks as used by Codacy

### Development setup / tooling

Various tools are needed to build and release

- XCode 10.1
- Cocopods 1.6.1
- Carthage 0.32.0

Release tooling (for maintainer reference)

- `hub` - Github's git cli wrapper `brew install hub`
- `semver` - Semantic version manager `npm install -g semver`
- `gsort` - GNU sort `brew install coreutils`
- `cmark` - Markdown to HTML `brew install cmark`
- `sign_update` - Sparkle Update manager DSA signer for AppCast. (TODO: Upgrade signing)
- `mustache` - Template system (`gem install mustache`, or equivalent npm package)

Also, assuming assumptions are not great,  you're building on MacOS compatible with XCode 10.1 which has the following installed:

- `git` 2.20.1
- `osascript`
- `unexpand`
- `PListBuddy` (You should be able to find it at `/usr/libexec/PlistBuddy`)

### Clone and setup dependencies

CutBox depends on Cocoapods to manage most dependencies, however it also depends on KeyHolder and Magnet (from Clipy)

To properly clone, use the `--recurse-submodules` option. i.e.

    git clone --recurse-submodules git@github.com:CutBox/CutBox

- Install Cocoapods: `pod install`
  - (run from `./CutBox/Cutbox`)
- Bootstrap Carthage: `carthage bootstrap`
  - (run from `CutBox/CutBox/DependencySubmodules/KeyHolder`)
  - This will build the Magnet & KeyHolder frameworks.
- XCode 10.1 should then be able to build / run / test

To keep things simple try `bin/setup`

It'll run these steps for you (Note it's very basic!)

There's a Gitter channel if you have problems getting up and running (https://gitter.im/CutBox)

# Licence

> CutBox is free software: you can redistribute it and/or modify
> it under the terms of the GNU General Public License as published by
> the Free Software Foundation, either version 3 of the License, or
> (at your option) any later version.
>
> CutBox is distributed in the hope that it will be useful,
> but WITHOUT ANY WARRANTY; without even the implied warranty of
> MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
> GNU General Public License for more details.
>
> You should have received a copy of the GNU General Public License
> along with this program.  If not, see <http://www.gnu.org/licenses/>.
