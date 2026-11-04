# tani2shell

Black-box pentest labs, one exploit story per repo — every lab is **home-grown, battle-tested by an autonomous AI pentest agent, and shipped with a full write-up** (challenge brief → solution walk-through → difficulty calibration, in English / 日本語 / 中文).

## The *2Shell series

| Lab | Exploit story | Difficulty (calibrated) | Solved by AI agent |
|---|---|---|---|
| [node2shell-lab](https://github.com/tani2shell/node2shell-lab) | Node.js `zlib` brotli crash chain (CVE-2026-111497), crash-gated double flag | 3.5/5 | full chain, factory-measured |
| [php2shell-lab](https://github.com/tani2shell/php2shell-lab) | PHP2Shell-era heap-disclosure chain (CVE-2026-109618/109619) + SUID symlink privesc | 4/5 nominal · 3.5/5 live-fire | both flags, ~15 min best run |

## What makes a tani2shell lab different

- **CHALLENGE.md** — true black-box brief, zero spoiler.
- **SOLUTION.md** — complete kill chain with every command, offsets, and the actual flag values (a write-up without the flag is a write-up without the ending).
- **DIFFICULTY.md** — nominal rating vs. live-fire calibration, with the reasoning behind it.
- **RESET.sh** — one command back to factory state.
- Every lab was attacked by an AI pentest agent before it was published; if the agent couldn't break it (or broke it in a way we didn't design), we fixed the lab, not the story.

## The rules

1. Only labs built from scratch get published — no repackaged upstream CTF images.
2. Every lab must be broken end-to-end by an autonomous agent before it ships.
3. Fix the lab before you blame the player.

*New labs land here as soon as they survive first contact — watch this space.*
