# Security reporting

Email suspected vulnerabilities to [dappnutchanon@gmail.com](mailto:dappnutchanon@gmail.com). Keep exploit details and private data out of public GitHub issues while the report is being reviewed.

Include the affected version or build, steps to reproduce, and the impact you observed. A small example using disposable files or test credentials is preferable to a copy of a real project. Remove live tokens, passwords, personal information, and unrelated file contents.

For general bugs and feature requests, use [GitHub Issues](https://github.com/dapp2549/RelayForge/issues).

## Access boundaries

RelayForge can read files, change project content, and start processes through its tools. Review workspace access and tool permissions before connecting an AI client.

Full Access uses your Windows account's file and network permissions and can reach outside the workspace. A Local MCP server also runs with your operating system permissions and is not sandboxed. Configure only executables and servers you trust.

Tool descriptions and results from an external MCP server are supplied by that server. Review permissions before allowing calls, especially calls that can change files, accounts, or external services.

## Release status

There is no public installer release yet. Current development builds are not an established public support baseline. Public release notes will identify the builds distributed through this repository.
