

# Literate configuration for Emacs and Gentoo Linux

This repository contains the (almost) complete system configuration,
as literate config. I even use it when I install the system on new
machines, semi-automatically, thanks to Org babel and Org tangle :)

I am a researcher and Org mode maintainer, and the config reflects my
workflows:

-   Custom agenda views with `org-ql`, email/RSS integration
-   Modal editing
-   Gentoo with LUKS encryption, Secure Boot, and BTRFS subvolumes
-   A working example of managing an entire OS from Org mode


# Repository layout

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">File</th>
<th scope="col" class="org-left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="org-left"><code>config.org</code></td>
<td class="org-left">Main Emacs configuration (tangles to <code>~/.emacs.d/</code>).</td>
</tr>

<tr>
<td class="org-left"><code>system-config.org</code></td>
<td class="org-left">Gentoo system configuration and installation guide</td>
</tr>

<tr>
<td class="org-left"><code>config_archive_*.org</code></td>
<td class="org-left">Archived entries from <code>config.org</code>, organized by year</td>
</tr>

<tr>
<td class="org-left"><code>system-config_archive_*.org</code></td>
<td class="org-left">Archived entries from <code>system-config.org</code></td>
</tr>

<tr>
<td class="org-left"><code>LICENSE</code></td>
<td class="org-left">GNU General Public License version 3</td>
</tr>
</tbody>
</table>


# Emacs

-   Multi-layer custom agenda via `org-ql`
-   Project management
-   `helm-org-ql` search across Org files, emails (Notmuch), and buffer history
-   Elisp development setup to work with mailing lists and high message inflow

-   `notmuch` with automatic tagging and multi-account support
-   `elfeed` for RSS, combined with `urlwatch` for web-page diff monitoring

-   Modal editing via `boon` and navigation with `avy`
-   Startup optimizations and garbage-collection tuning
-   All configuration is literate – tangled to `init.el` and `early-init.el`


# Gentoo

-   Full-disk encryption with LUKS2 on LVM and BTRFS subvolumes.
-   YubiKey integration for LUKS decryption (optional password fallback).
-   Secure Boot enabled via `shim` with custom keys.

-   The Org file tangles to `/etc/portage/make.conf`, `/etc/fstab`,
    kernel config, and Portage’s world file.
-   Automated update scripts and cleanup routines

-   Awesome WM as the primary window manager, with Picom for compositing
-   Qutebrowser as the default browser, configured with custom keybindings
-   System-wide theming (GTK/Qt, fonts, icons), all derived from the Emacs theme

-   `rclone` and `restic` for encrypted remote backups.


# License

GNU General Public License v3 (see `LICENSE`).

