# Xverb — releases

Built copies of [Xverb](https://github.com/xsm909/xverb), a dual-pane
file manager in the Total Commander tradition, written in Flutter and extended
with Python plugins.

**This repository holds no source of its own.** It is where the built archives
live, so that a clone of the application's own repository stays small: a build
is twenty megabytes and git keeps every one of them for ever.

## Installing

One line, and nothing to unpack:

```sh
curl -fsSL https://raw.githubusercontent.com/xsm909/xverb-release/main/install.sh | sh
```

```powershell
irm https://raw.githubusercontent.com/xsm909/xverb-release/main/install.ps1 | iex
```

Either one takes the newest release below, checks it against the checksum
beside it, and installs it without asking for administrator rights — into
`/Applications`, `%LOCALAPPDATA%\Programs` or `~/.local/lib`. Settings and
installed plugins are left alone, both when installing over an older copy and
when uninstalling.

## What is in `release/`

Per release, one archive per platform, each with the SHA-256 beside it:

```
xverb-1.1.0.477-macos-arm64.tar.gz     + .sha256
xverb-1.1.0.477-linux-x64.tar.gz       + .sha256
xverb-1.1.0.477-windows-x64.zip        + .sha256
xverb-1.1.0.477-source.tar.gz          + .sha256
xverb-1.1.0.477-notes.md
```

Each release also has a page under
[Releases](https://github.com/xsm909/xverb-release/releases), with its notes and
the same files. The installers read this folder, not those pages, so the
folder is the one that is always complete.

**Versions are `A.B.C.D`,** and each part promises something different:

| | moves when |
|---|---|
| **A** | the contract between the application and its plugins breaks. A plugin written for `apiVersion: 1` runs on every `1.x`, and on no other major |
| **B** | something is in the program that was not there before |
| **C** | a release is worth talking about — a name to say, not a gate |
| **D** | every build |

**Any build published here is an update**, whichever part of it moved: a copy
that is already installed offers it. The newest release is simply the largest
version here, compared number by number — that is all an installer has to know.
There is no index to keep in step and nothing to parse.

Releases are named after places, with a photograph of the place on the About
card; the builds of 1.1.0 are **Iceland**.

## The source beside the binaries

`…-source.tar.gz` is the source the binaries next to it were built from, and it
belongs here because the GNU General Public License says it must: whoever is
offered the object code from a place must be offered the corresponding source
from the same place. Every build here is reproducible from the archive beside
it.

**It is here from 1.1.0.461 on**, beside every release that follows. It is the
public tree, not the development repository: the files the application is built
from, assembled by `tool/publish.dart` out of the same commit as the binaries
beside it, and no history. For the two releases published before it, 1.0.0.445
and 1.0.0.448, ask and it will be sent.

## Licence

Xverb is free software under the **GNU General Public License, version 3
or later** — the same licence as the source, because a build is the source in
another shape. See [LICENSE](LICENSE), or
<https://www.gnu.org/licenses/gpl-3.0.html>.
