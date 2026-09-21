![FreshThread — Start Fresh Without Starting Over.](assets/freshthread-banner.png)

# FreshThread BETA version

**FreshThread is a Windows companion for Codex that shows task activity and helps
you continue in a fresh task with your working context.**

Its panel shows available context usage, completed turns, compactions and handoff
readiness. A handoff summarizes your goal, constraints, completed work and next
steps. You review and approve it before moving to a new task.

FreshThread does not expand the model's context limit or preserve every detail.
Measurements that Codex does not provide appear as unavailable.

[![FreshThread in action — looping demonstration.](assets/freshthread-demo.gif)](assets/freshthread-demo.mp4)

## Beta status

**The public beta is being prepared. No installer has been published yet.**
This repository will host downloads, release notes and bug reports. The source
code remains private.

The planned trial lasts **10 days from first use**, with a FreshThread account
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

Back up your work and existing FreshThread data before testing. Do not copy
FreshThread databases between Windows users.

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

## Updates and removal

A separate beta update channel is planned and must pass testing before launch.
Stable installations will not receive beta builds automatically.

Uninstalling removes FreshThread's integration and local application data, so
keep any needed backup first. Installing an older executable alone is not a
supported rollback because database formats can change.
