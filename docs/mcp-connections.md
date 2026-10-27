# Connect MCP servers

These steps apply to RelayForge 0.2.0 and newer. Open **Settings > Runtime > MCP Connections** to manage the services your agents can use.

## Add a connection

1. Choose **Add MCP server**, then select Context7, GitHub, Playwright, Chrome DevTools or MarkItDown. Choose **Custom MCP** for another server.
2. Review the connection details. Enter any required token in the protected field. Local presets show their package, publisher and install location.
3. Select the workspaces that may use the MCP and choose **Ask before use** or **Allow this MCP**.
4. Choose **Add & connect** or **Install & connect**. RelayForge prepares the reviewed Local dependencies, connects and loads the tools automatically.

Access applies to the MCP as a whole. New valid tools inherit that policy. Open **Tools > Tool exceptions** when an individual tool needs a different rule. Existing tool overrides are retained, and old connections without an MCP policy continue to Ask. Server Block, tool Deny and project protection rules still apply in Full Access.

Custom setup accepts one server URL, a quoted command or a single-server MCP JSON configuration. Use **Advanced configuration** for separate executable arguments, protected environment fields or additional connection options. Custom servers may require runtimes or services that you install yourself.

## Local processes

Reviewed presets prepare their required runtimes and packages in a managed folder. Browser presets also install isolated browsers. Use a dedicated folder if you choose a different location. Local MCPs run with your Windows account's permissions and are not sandboxed. Review the publisher and package before installing.

Setup continues when you leave Settings. **Cancel setup** keeps the saved connection, and **Retry setup** reuses the selected location. After an app interruption, choose Retry. Account sign-in and provider approvals still require your action.

## Remote servers

Remote connections support Streamable HTTP with anonymous access, bearer tokens or public-client OAuth. Enter credentials in Desktop's protected fields; saved values cannot be displayed.

For OAuth, review the authorization destinations and choose **Approve and sign in**. RelayForge continues after sign-in finishes. Loopback HTTP and private-network HTTPS require explicit approval.

Legacy SSE, Resources, Prompts, sampling and elicitation are not exposed.

## Failures and retries

Open **Connection** in the MCP details for status, sign-in and diagnostics. Tools load automatically. A catalog refresh keeps the connection open when possible; invalid or stale schemas remain unavailable for use. Independently invalid tools are marked while valid tools can remain available.

When a call shows **Outcome unknown**, it may have reached the server before the connection failed. Check the external service before starting the operation again, especially if it changes data. Reconnecting does not replay the call.

For a report, include the server name, connection type, app version and error code. **Copy diagnostics** copies metadata without saved credentials, arguments or results. See [Support](../SUPPORT.md) for contact details.
