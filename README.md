![FreshThread — Start Fresh Without Starting Over.](assets/freshthread-banner.png)

# FreshThread BETA version

**FreshThread is a Windows companion for Codex that shows task activity and helps
you continue in a fresh task with your working context.**

Its panel shows available context usage, completed turns, compactions and handoff
readiness. A handoff summarizes your goal, constraints, completed work and next
steps. You review and approve it before moving to a new task.

[![FreshThread in action — looping demonstration.](assets/freshthread-demo.gif)](assets/freshthread-demo.mp4)

## Reading the panel

| Label | Meaning |
| --- | --- |
| **MiB** | Physical size of the session data accumulated on disk, up to FreshThread's latest reading. Separate from the model's context usage. |
| **Session pressure** | The session's overall pressure status, shown as BASELINE, RISING, ELEVATED or LOOPING. It gives a session-level status rather than a live usage percentage. |
| **Last compaction** | The latest compaction's before → after percentages. The **right-hand value** is the starting context load after compaction: **88.5% → 17.1%** means the session resumed with 17.1% already occupied. |
| **Compactions** | Total recorded context compressions in this session. Each condenses earlier context to free space; the count does not tell you how much space was freed. |
| **Completed turns** | Total response cycles recorded as completed in this session. One cycle can include several tool calls. |
| **Interrupted** | Total response cycles recorded as interrupted in this session, for example when a response is stopped. |
| **Token use** | Accumulated recorded token usage over completed and interrupted turns. This total can grow across many context windows. |
| **Handoff** | Readiness to continue in a new task with the prepared working context. A ready handoff starts only when you choose it. |
| **Context load** | How much of the current context window is occupied at the latest measurement. It changes as work continues and drops when compaction frees space. |

The right-hand value in **Last compaction** shows how much context was still
occupied when work resumed. A higher starting value leaves less room for new
work. **Context load** shows the latest occupancy as the session continues.

## Beta status

**The public beta is being prepared. No installer has been published yet.**
This repository will host downloads, release notes and bug reports. The source
code remains private.

The planned trial lasts **14 days from first use**, with a FreshThread account
and online verification. Each device gets one trial, shared across accounts.
Reinstalling, switching accounts or moving an existing account to another device
will not restart it. After expiry, FreshThread features will stop, while user
data and access to updates remain available.

Trial enforcement is still being implemented and tested. There is no invitation
limit or announced release date.

## Getting started

Once the beta is released:

1. Download the Windows x64 installer from this repository's Releases.
2. Install it in the Windows account where you use Codex.
3. Review and enable FreshThread's hooks in Codex.
4. Open the FreshThread panel to view task activity or start a handoff.

The initial installer will lack a Windows publisher signature (Authenticode),
so Windows may show an unknown-publisher warning. Do not disable Windows
protection. Automatic updates require separate signature verification; a
download hash alone does not prove who published a file.

## What to test

- Startup and hook setup.
- Tasks opened from Projects and Recents, task switching and empty tasks.
- Panel placement and proportions across resolutions, Windows scaling and pets.
- Measurements after a completed turn, and handoffs using a disposable task
  without private content.
- Whether updates preserve settings and hooks. Avoid deliberately interrupting
  installation on your everyday computer.

Check release notes for known limitations. Report unexpected behavior even if
you find a workaround.

## Report a problem

Search existing issues, then use **Issues → New issue → Bug report**. Include:

- FreshThread build, Codex version, Windows version and display scaling.
- Steps to reproduce the problem.
- What you expected and what happened.

Issues are public. Remove private information from screenshots and optional
diagnostics. Never upload conversations, databases, credentials, account
identifiers or raw diagnostic folders.

Report security vulnerabilities through
[private reporting](https://github.com/GG95-lab/FreshThread-BETA-version/security/advisories/new),
not public issues.

## Your data

FreshThread stores its context checkpoints locally and encrypts them on Windows.
Handoffs run through Codex; model-based preparation may use Codex's model provider.
The planned sign-in and trial service will verify your account and device, without
receiving your conversations or project files.

## Updates

A separate beta update channel is planned and must pass testing before launch.
Stable installations will not receive beta builds automatically.
