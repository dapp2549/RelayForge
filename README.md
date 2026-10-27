# RelayForge

RelayForge is a Windows desktop app that gives connected AI clients access to project tools through the Model Context Protocol (MCP). You choose the workspaces they can use and review their work in the app.

Use RelayForge to manage Tasks, inspect file changes, run commands, and connect Local or Remote MCP servers. The interface supports English and Thai.

## Release status

RelayForge is in development. Download the latest Windows x64 installer and read its release notes on the [Releases page](https://github.com/dapp2549/RelayForge/releases).

This repository contains installers and user documentation. The application source is maintained separately in a private repository. Download installers from the official Releases page.

## What you can do

- Register project folders as workspaces and set their access permissions.
- Keep Task plans and activity, review diffs, and check command results in one place.
- Give an AI client file, search, Git, and process tools through MCP.
- Connect other MCP servers and control which workspaces and tools they can access.
- Answer Agent questions from the Task page, with choices or your own text.

## Working with a project

In RelayForge Desktop, choose **Register Project** and select a folder. Review its workspace permissions before connecting an AI client. Confirm that the client has selected the intended workspace before asking it to change files or run commands.

The Task page shows the plan, file changes, activity, and checks. When an Agent needs an answer, a question indicator appears beside the workspace. Open the Task to respond. Skipping a question leaves it pending.

Start with **Normal Access**. It applies confirmation prompts to actions covered by the normal policy. **Full Access** allows otherwise permitted shell commands and actions without those prompts, using your Windows account's file and network permissions, including outside the workspace. Blocked commands and tool rules still apply.

## Documentation

- [Connect MCP servers](docs/mcp-connections.md)
- [Data and privacy](docs/data-and-privacy.md)
- [Install and verify a release](docs/release-verification.md)
- [Get help or report a bug](SUPPORT.md)
- [Report a security issue](SECURITY.md)

## Contact

Use [GitHub Issues](https://github.com/dapp2549/RelayForge/issues) for bugs, feature requests, and questions. For private reports, email [dappnutchanon@gmail.com](mailto:dappnutchanon@gmail.com).
