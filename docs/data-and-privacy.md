# Data and privacy

## Data on your computer

RelayForge keeps workspace registrations, Task history, file-change records, command output, and Agent question answers in its local application data. Indexes and change records can contain project content. Treat the application data as sensitive when backing it up or sharing access to your computer.

Tunnel and external MCP credentials use operating system protection. If the protection backend is unavailable, credential operations fail rather than falling back to plaintext storage.

## Connected clients and services

An AI client receives the results of the tools it calls. Depending on the tool and permissions, these results can include file content, command output, images, and project metadata. Review the AI provider's data-handling terms before connecting private projects.

Calls to an external MCP server send the requested arguments to that server and return its results through RelayForge. The server's operator controls what happens to the data it receives. A Local server runs on your computer with your operating system permissions; a Remote server receives requests over its configured connection.

## Diagnostics and reports

Native crash dumps stay on the computer. Automatic crash-dump upload is disabled. Dumps can contain process memory, so avoid attaching them to a public issue.

The Support report in Settings lets you preview and copy a limited diagnostic summary. Opening or copying it does not upload it. The summary contains build and runtime-health information plus recent error metadata. It excludes workspace paths, project files, command arguments, environment variables, and raw dumps.

If you post a report on GitHub or send it by email, the information is shared through that service. Check screenshots and attachments as well as the report text before sending them.

## Questions about your data

Email [dappnutchanon@gmail.com](mailto:dappnutchanon@gmail.com) for private questions about data handling. Use [GitHub Issues](https://github.com/dappnutchanon/RelayForge/issues) for questions that can be discussed publicly.
