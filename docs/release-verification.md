# Install and verify RelayForge

RelayForge for Windows x64 is distributed from the [official Releases page](https://github.com/dapp2549/RelayForge/releases). Do not download an installer from an issue attachment, third-party mirror, or a source-development CI artifact.

## Install

1. Open the official Releases page and choose the latest **published stable** release, not a draft or prerelease.
2. Read the release notes, supported Windows versions, prerequisites, and known issues. Download the `RelayForge-<version>-win-x64.exe` installer.
3. Check the installer SHA-256 against the checksum published with that exact release.
4. Verify any Windows publisher signature shown in the release notes. A missing or invalid Authenticode signature must not be represented as a verified publisher signature.
5. Run the installer under your own Windows account. Review the publisher and Windows security prompts; do not disable SmartScreen or security controls based on an unofficial instruction.
6. Open RelayForge, review the Workspace access permissions, and start with **Normal Access**.

In PowerShell, calculate a SHA-256 checksum with:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\RelayForge-<version>-win-x64.exe'
```

Compare the complete 64-character hash with the release's checksum; the version and filename must match.

## Updates

RelayForge's release updater retrieves metadata from this repository's **published stable** GitHub Releases. New releases include `relayforge-update.json` and a binary Ed25519 signature file, `relayforge-update.sig`. The installed updater checks the signed manifest against a trusted public key included in the application and verifies the installer size and SHA-256 before installation. This is separate from a Windows Authenticode publisher signature.

A newer version must also pass the application's compatibility and rollback checks. A failed check is **not** a reason to disable signature, antivirus, or hash verification. Updates may be unavailable until a previously trusted release is installed as the baseline.

Do not replace the installed app manually while tasks or file operations are running. Before any upgrade, back up your application data and stop running work safely. See the release notes for supported migration and rollback instructions.

## Privacy and support

The application source is maintained in a separate private development repository. This distribution repository contains user-facing documentation and published installers only; it is **not** a mirror of the private codebase.

For support, see [SUPPORT.md](../SUPPORT.md), and for confidential vulnerability reports see [SECURITY.md](../SECURITY.md). Do not upload credentials, raw crash dumps or private project files to public issues.
