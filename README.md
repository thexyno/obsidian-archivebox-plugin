# Obsidian ArchiveBox Plugin
fork that works with the new REST API

This plugin searches Obsidian posts for Internet links and archives them to a self-hosted [ArchiveBox](https://archivebox.io) instance. If you're linking to external things in a second brain, you don't want them to disappear.

Tested against Obsidian 1.8.9.

## Assumptions and Limitations

-   You are running [ArchiveBox](https://archivebox.io) **v0.8.4-rc1** or later (required for the **ALPHA** REST API).
-   A API Token has been created for ArchiveBox / Obsidian and this is used to submit.
-   You may or may not use HTTP Basic auth in front of `/public`
-   You want to archive fully-qualified URIs (e.g. `https://google.com/`, not `google.com` or `./some/path`).

## Usage

Install the ArchiveBox plugin and load it, then configure the information in the settings panel.

### Settings

-   **ArchiveBox URI** - Set this to the URL where your ArchiveBox instance is accessible, e.g. `https://archivebox.example.com/`.
-   **ArchiveBox API Token** - The API Token for an account that has submission privileges.
-   **Ignore RFC1918 Addresses** - Ignore links that contain private addresses. By default, no URI pointing at an RFC1918 address will be saved.
-   **Ignored Domains** - Ignore links that exist in a comma-separated domain blocklist. (e.g. `google.com,duckduckgo.com`).
-   **Use Basic Auth** - Use [HTTP Basic Authentication](https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication) for a username/password ahead of ArchiveBox. Sometimes used when one wants to keep `/public` private.
-   **Basic Auth Username** - The HTTP basic auth username.
-   **Basic Auth Password** - The HTTP basic auth password.
-   **Auto-Submit** - Watch for file modification and auto-submit to ArchiveBox in real time. This can be relatively chatty so it is off by default.
-   **Minimum Batch Submission Time** - Wait at least this many seconds before sending another auto-submission.
-   **Cache URIs** - If this is selected, the plugin will not resubmit URIs it has seen before to ArchiveBox. ArchiveBox deduplicates on its own, but this cuts down on needless request bandwidth.
-   **Debug Mode** - Adds verbose logging to the Obsidian developer console. Turn on if a contributor has asked, or if you want to file an issue.


## License

[GNU GPL-3.0](./LICENSE).

Personal software is for people, not corpo profit.
