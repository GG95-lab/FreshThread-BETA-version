# FreshThread BETA version

This repository distributes FreshThread installers and collects feedback. The
application source is maintained separately. No public beta installer has been
published yet.

The planned public beta lasts **10 days from its announced launch**. Exact start
and end dates will appear with the first beta release. This is a feedback period,
not an automatic application expiry. There is no invitation or tester-count limit.

## Before installing

- Use the Windows x64 installer attached to a release in this repository.
- The initial beta has no Windows Authenticode signature. Windows may display
  an unknown-publisher warning. Do not disable Windows protection globally.
- Update signatures and Windows publisher signatures are different. Automatic
  updates must be verified by FreshThread's embedded updater public key. A hash
  posted next to a download alone does not prove publisher authenticity.
- Back up your work and any existing FreshThread data privately before testing.
  Do not move FreshThread databases between Windows users.

## What to test

1. Install in the Windows account where you use Codex. Check startup and the
   initial hook setup; approve FreshThread hooks in Codex yourself.
2. Open tasks from Projects and Recents, switch tasks, and open an empty task.
3. Check panel placement with your normal Windows scaling, resolution and pet.
4. Complete a turn, review the available measurements, then try an approved
   handoff using a disposable task without private content.
5. When a new beta is released, check that updating preserves settings and hooks.
   Do not deliberately interrupt installation on your daily working environment.

Report unexpected behavior even if you found a workaround. Missing measurements
are not zero measurements. The release notes list known limitations.

## Report a problem

Open this repository's **Issues → New issue → Bug report**. Include the exact
FreshThread version/build, Codex version, Windows version/scaling, reproduction
steps, expected behavior and actual behavior. Search for existing reports first.

Issues are public. Never attach conversations, databases, credentials, account
identifiers or raw diagnostic folders. Review and redact screenshots before
posting. Diagnostics are optional and must be inspected before sharing.

For a suspected security vulnerability, use
[private reporting](https://github.com/GG95-lab/FreshThread-BETA-version/security/advisories/new).
Do not publish exploit details or secrets in a normal issue.

## Updates and the end of the beta

Beta updates will use a beta-only feed. Stable users must not receive beta builds
implicitly. Feed provisioning and signed-update acceptance are launch gates;
this document does not claim that the service is already running.

At the end of day 10, we will summarize confirmed problems and decide whether to
release a stable version or extend the beta. Open issues will remain visible.
There is no promised stable-release date and no automatic deletion of user data.

Windows uninstall removes FreshThread's owned integration and local application
data. Keep any needed private backup before uninstalling. Database schema changes
mean that installing an older executable alone is not a supported rollback.
