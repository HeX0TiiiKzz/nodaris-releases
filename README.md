# Nodaris

Game server panel for Linux. This repository only hosts the release files.

## Install

On a fresh server, as root or with sudo:

```bash
curl -fsSL https://github.com/HeX0TiiiKzz/nodaris-releases/releases/latest/download/install.sh | sudo bash
```

The installer asks a few questions, then sets up the panel, its database, nginx and HTTPS.
You sign in with the administrator account you create during the installation.

## Requirements

- Ubuntu 22.04, 24.04 or 26.04, or Debian 12 or 13
- x86_64 or arm64, with systemd
- Ports 80 and 443 free
- A domain name pointing to the server for HTTPS, otherwise the panel runs over HTTP on the IP

## Status

Early preview. Accounts and sign-in are real, but game servers are simulated: there is no node
daemon yet, so the panel does not run real game servers. The installer has not been validated
on a production server yet, so use a machine you can wipe.

## After the installation

```bash
nodaris status
nodaris logs
nodaris user:reset-password
nodaris update
```
