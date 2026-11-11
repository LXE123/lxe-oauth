# LXE Agent OAuth metadata

This repository publishes LXE Agent's public OAuth Client ID Metadata Document (CIMD) through GitHub Pages.

- Document and client ID: https://lxe123.github.io/lxe-oauth/client.json
- Application: https://github.com/LXE123/LXE_AGENT

The document describes a native public client using the authorization code flow with PKCE. The callback is `http://127.0.0.1:<port>/callback`; the document omits the port because native loopback redirects allow a port chosen at runtime (RFC 8252, section 7.3).

GitHub Pages serves the root of `main`. `.nojekyll` keeps the JSON file unchanged. Keep the document URL stable and keep its `client_id` identical to that URL.

This repository contains public metadata only. Publishing it does not enable CIMD in an LXE build; the client must implement CIMD and the authorization server must advertise support.
