# comrade-cli

`ani-cli` defected. It now pulls everything from [hdrezka.website](https://hdrezka.website) instead of anidb, which means the motherland's servers decide your quality now, and every show arrives dubbed by whichever collective of Russian voice actors got to it first.

There is no more sub vs dub. There is only *perevod* (translation), assigned by committee. You will select from the list like everyone else, and you will be grateful.

The committee's jurisdiction is not limited to anime either, movies and TV shows are also subject to nationalization. Search for whatever you want, the collective has already dubbed it.

## What changed from upstream

- Source: anidb.app ➜ hdrezka.website (nationalized)
- Audio: mostly Russian dubs, some Ukrainian, occasional original+subs if the committee approves
- `--dub`: abolished, replaced by a translator picker — there is no dub, only many dubs
- `--skip` and `-N`: seized by the state, redistributed to nobody
- Everything else: same ani-cli you already know — POSIX sh, fzf, your video player of choice

## Install

```sh
git clone "https://github.com/justchokingaround/comrade-cli.git"
sudo cp comrade-cli/comrade-cli /usr/local/bin
rm -rf comrade-cli
```

Needs `curl`, `sed`, `grep`, `fzf` (or `rofi`/`dmenu`), and `mpv`/`vlc`/whatever plays video in your republic.

## Usage

```sh
comrade-cli lain
comrade-cli -q 720p grand blue
comrade-cli -c            # continue watching, the collective remembers everything
```

Same flags as upstream ani-cli, minus the ones the state confiscated above. `comrade-cli -h` for the rest.

## Why does this exist

Because the anime had to come from somewhere, and hdrezka said "for the workers." Blame [pystardust/ani-cli](https://github.com/pystardust/ani-cli) for the good parts, blame me for whatever breaks.

Comrade select episode. Comrade watch anime. Comrade do not ask about the ads.
