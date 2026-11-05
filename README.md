<div align="center">

<img src=".github/assets/logo.svg" width="96" alt="Nodaris logo">

# Nodaris

**A clean, modern game server panel for Linux.**
Install it with one command, manage everything from your browser.

[![Latest release](https://img.shields.io/github/v/release/HeX0TiiiKzz/nodaris-releases?style=for-the-badge&label=release&color=7c3aed)](https://github.com/HeX0TiiiKzz/nodaris-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/HeX0TiiiKzz/nodaris-releases/total?style=for-the-badge&color=0369a1)](https://github.com/HeX0TiiiKzz/nodaris-releases/releases)
[![Status](https://img.shields.io/badge/status-early%20preview-f59e0b?style=for-the-badge)](#-project-status)

![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04%20%7C%2024.04%20%7C%2026.04-E95420?style=flat-square&logo=ubuntu&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-12%20%7C%2013-A81D33?style=flat-square&logo=debian&logoColor=white)
![Languages](https://img.shields.io/badge/languages-EN%20%7C%20FR%20%7C%20DE%20%7C%20RU-047857?style=flat-square)
![Themes](https://img.shields.io/badge/themes-light%20%26%20dark-be123c?style=flat-square)

**[🚀 Install](#-install)** &nbsp;·&nbsp;
**[🖥️ Add a node](#%EF%B8%8F-add-a-node)** &nbsp;·&nbsp;
**[✨ Features](#-features)** &nbsp;·&nbsp;
**[📸 Screenshots](#-screenshots)** &nbsp;·&nbsp;
**[🔄 Update](#-update)** &nbsp;·&nbsp;
**[🧰 Commands](#-commands)** &nbsp;·&nbsp;
**[🚧 Status](#-project-status)** &nbsp;·&nbsp;
**[📦 Releases](https://github.com/HeX0TiiiKzz/nodaris-releases/releases)**

</div>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/home-dark.png">
    <img src=".github/assets/home-light.png" alt="The Nodaris client area" width="100%">
  </picture>
</p>

> [!WARNING]
> **Nodaris is an early preview.** It runs on a real VPS, but UFW, Let's Encrypt and HTTPS are not validated yet. [See what works today](#-project-status), and use a machine you can wipe.

## 🚀 Install

On a fresh server, as root or with sudo:

```bash
curl -fsSL https://github.com/HeX0TiiiKzz/nodaris-releases/releases/latest/download/install.sh | sudo bash
```

The installer asks a few questions, then sets up the panel, its database, nginx and HTTPS. Suggested values are already in their field, ready to be edited, **‹ Previous** goes back one question, and any answer can be changed on the review screen.

Once the panel runs, a setup guide takes over in the console: location, node, ports, a final check of the panel and the node, then how to create your first server. Select the step you are on: a step is only ticked when the panel really shows it done. Open it again at any time with `sudo nodaris setup`.

| | Requirements |
|---|---|
| 🐧 **System** | Ubuntu 22.04, 24.04 or 26.04, or Debian 12 or 13, with systemd |
| 💻 **Hardware** | x86_64 or arm64 |
| 🌐 **Network** | Ports 80 and 443 free |
| 🔒 **HTTPS** | A domain pointing to the server, otherwise the panel runs over HTTP on the IP |

## 🖥️ Add a node

A node is the machine that runs your game servers. It can be the same machine as the panel. The setup guide walks you through this, with `sudo nodaris setup`:

1. In the panel, create a node in **Admin → Nodes**.
2. Open its **Configuration** tab and copy the **Node token**.
3. In the guide, select **Configure the node**. Choose **This server** to install it here, or **Another server** to get the command to run on that machine.
4. Paste the token when the installer asks for it.

The installer sets up Docker and the Nodaris daemon. Your servers then start, stop and show their live console in the client area.

## ✨ Features

<table>
<tr>
<td width="50%" valign="top">

### 🎮 For your clients
- Start, stop and restart, with a live console
- Files, backups and SFTP
- Real databases, with import and export
- Activity page: who restarted, who edited what
- Quick downloads: plugins, mods, addons, texture packs, maps
- Two-factor authentication with recovery codes

</td>
<td width="50%" valign="top">

### 🛠️ For administrators
- Locations, nodes, allocations, servers, nests, eggs and mounts
- Node daemon in Go, with an installer of its own
- Roles with full, fine-grained permissions
- Community egg catalogue, installed in one click
- Activity log: who created, edited or deleted what
- Discord webhooks with a fully editable embed

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🎨 Make it yours
- Light and dark mode, following your system
- Built-in themes, or create your own
- Your name and logo, on the client and admin sides
- English, French, German and Russian

</td>
<td width="50%" valign="top">

### ⚙️ Easy to run
- One-command installer with a clear console
- A setup guide and a final check, from a fresh panel to your first server
- One-click updates from the admin panel
- Automatic rollback if an update fails
- Built-in help centre for administrators

</td>
</tr>
</table>

## 📸 Screenshots

<table>
<tr>
<td width="50%"><img src=".github/assets/console-dark.png" alt="Live console"><p align="center"><b>Live console</b></p></td>
<td width="50%"><img src=".github/assets/server-activity-light.png" alt="Server activity"><p align="center"><b>Who did what on a server</b></p></td>
</tr>
<tr>
<td width="50%"><img src=".github/assets/admin-overview-dark.png" alt="Admin overview"><p align="center"><b>Admin overview</b></p></td>
<td width="50%"><img src=".github/assets/admin-activity-dark.png" alt="Activity log"><p align="center"><b>Activity log</b></p></td>
</tr>
<tr>
<td width="50%"><img src=".github/assets/admin-themes-light.png" alt="Themes"><p align="center"><b>Themes, with light and dark previews</b></p></td>
<td width="50%"><img src=".github/assets/admin-webhook-dark.png" alt="Discord webhook editor"><p align="center"><b>Discord embed editor</b></p></td>
</tr>
</table>

## 🔄 Update

Open **Admin → Overview** and press **Update**: the panel checks for a new version, shows a progress bar, and asks you to refresh when it is done. If a step fails, it puts everything back as it was.

A node on the same machine is updated with the panel. A node on another machine is updated there:

```bash
curl -fsSL https://github.com/HeX0TiiiKzz/nodaris-releases/releases/latest/download/install-node.sh | sudo bash -s -- --update
```

> [!NOTE]
> Coming from 0.5 or older? Run `nodaris update` once on the server. This installs the one-click updater, and you will not need SSH for updates after that.

## 🧰 Commands

| Command | What it does |
|---|---|
| `nodaris setup` | Opens the setup guide: location, node, final check, first server |
| `nodaris status` | Shows what is running |
| `nodaris logs` | Follows the panel logs |
| `nodaris update` | Installs the latest version, on the panel and on a node of the same machine |
| `nodaris repair` | Fixes the panel and keeps your data |
| `nodaris user:reset-password` | Resets a forgotten password |
| `nodaris user:disable-2fa` | Unlocks an account that lost its two-factor device |
| `nodaris uninstall` | Removes the panel |

## 🚧 Project status

| Part | State |
|---|---|
| Panel installer: packages, MariaDB, nginx, systemd | ✅ Validated with the published command, on a machine without a panel |
| Setup guide and final check | ✅ Validated from a fresh panel to a running server |
| Panel, node and a Minecraft server on a real VPS | ✅ Validated |
| Node installer: Docker and the daemon | ✅ Validated, panel and node on the same machine |
| Node daemon: power, console, files, backups, SFTP | ✅ Validated with a real Paper server in Docker |
| Accounts, roles, 2FA, activity log, webhooks, themes | ✅ Validated |
| Databases, import and export | ✅ Validated on MariaDB 10.11 |
| Updates: `nodaris update`, one-click updates, rollback | ✅ Validated on a real systemd |
| Removing the panel | ✅ Validated |
| Removing a node | 🟡 Not tried yet |
| A node on a second machine | 🟡 Not tried yet |
| A real player joining with the game | 🟡 Not tried yet: the server answers the Minecraft status protocol |
| Schedules, collaborators, player list | 🟡 Still simulated, and they say so |
| Quick downloads | 🟡 Listed and logged, no file reaches a machine yet |
| UFW, Let's Encrypt and HTTPS on a VPS | 🔴 Not validated yet |
| Debian, Ubuntu 22.04 and 26.04, ARM | 🔴 Not validated yet |

✅ means it really ran: on Ubuntu 24.04 under WSL2 over HTTP, and on a real VPS where that line says so. Everything else is listed as it stands.

<div align="center">

**[⬆ Back to top](#nodaris)** &nbsp;·&nbsp; **[📦 All releases](https://github.com/HeX0TiiiKzz/nodaris-releases/releases)** &nbsp;·&nbsp; **[🐛 Report a problem](https://github.com/HeX0TiiiKzz/nodaris-releases/issues/new)**

<sub>This repository only hosts the release files.</sub>

</div>
