# ICBM access list

This repository contains the device IDs authorized to use the ICBM mod.

## Manage access

Edit `whitelist.txt` on the `main` branch and commit your changes:

- Add a device ID on a new line to grant access.
- Remove its line to revoke access on the next game launch.
- Use one 64-character hexadecimal ID per line. Uppercase and lowercase are accepted.
- Do not add names, comments, commas, or other text to the file.

The mod checks this list when it starts. Updates do not require a new DLL while the file URL remains the same. Changes may take time to reach clients because of caching. Sessions already running are not rechecked.

If the list cannot be downloaded, contains invalid entries, or does not include the current device ID, the remote-enabled mod closes the game.

## Device IDs

Use the separate ID tool to obtain your ICBM device ID. It is a SHA-256 value derived from the Windows installation identifier. Reinstalling Windows may change it; cloned installations may share the same value.

## Repository contents

Keep this repository limited to the access list and documentation. Do not upload private administration tools, DLLs, backups, credentials, or signing keys.

The list is public. This version uses HTTPS and a URL embedded in the mod; the list is not digitally signed. Modifying the DLL can bypass client-side checks. Older DLLs with embedded local lists are not controlled by this repository.
