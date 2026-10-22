# Connect MCP servers

RelayForge can connect an AI client to MCP servers you configure in Desktop. You choose which workspaces can use each server and whether individual tools require confirmation.

## Add a connection

1. Open **Settings > Runtime > MCP Connections** and choose **Add MCP server**.
2. Choose **Local process** or **Remote server**, then enter the server's connection details.
3. Select the workspaces allowed to use it and save the connection.
4. Open its details, select an allowed workspace, and choose **Connect**.
5. Open **Tools & permissions > Discover tools** and review the available tools. Choose **Ask**, **Allow**, or **Deny** for each tool you intend to use.

Saving a connection does not start the server or contact it. New tools default to Ask. Deny still applies when the workspace uses Full Access.

## Local processes

Supply the executable and its arguments in separate fields. Arguments do not use shell expansion. Add any required protected environment values through the connection settings.

A Local server runs with your Windows account's permissions and is not sandboxed. Check the executable, arguments, and package source before connecting it. Requirements such as Node.js or Docker depend on the server you select.

## Remote servers

Remote connections support Streamable HTTP with anonymous access, bearer tokens, or public-client OAuth, depending on the server. Enter credentials in Desktop's protected fields.

If OAuth sign-in is needed, review the authorization destination and choose **Approve and sign in** to open the browser. Choose **Connect** again after sign-in completes.

Loopback HTTP and private-network HTTPS connections require explicit approval. Legacy SSE transport is not supported.

## Failures and retries

When a call shows **Outcome unknown**, the request may have reached the server before the connection failed. Check the external service before starting the operation again, especially if it changes data. Reconnecting does not automatically replay the call.

To report a connection problem, include the connection type, server name, app build, and error code. Remove credentials and private arguments from the report. See [Support](../SUPPORT.md) for contact details.
