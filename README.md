## Seqera Studio Xpra

This repository contains the definition of Seqera Studio Xpra. The `main` branch contains the
latest supported version of Xpra with connect-client. To use an older version of any component,
check the existing tags using the pattern: `xpra/<version>/connect/<version>`.

## Components

- **[Xpra](https://xpra.org/) v6.2.0-r2-1** — persistent remote display server and client
- **Python 3.12** — system Python
- **Micromamba** — conda-based environment manager
- **Terminator** — default terminal emulator
- **connect-client** — Seqera connect client for studio integration

## Repository Structure

`.seqera/` contains:

- `studio-config.yaml` — references the pre-built image; studios using this branch will not require a build step
- `Dockerfile` — shows how the image was built; fork this repository and modify it to create a custom image
- `entry.sh` — startup script that launches the Xpra server
- `seqera-wallpaper.png` — desktop background wallpaper
- `welcome_ASCII.txt` — welcome banner displayed in terminal sessions

## Customization

To create a customized version:

1. Fork this repository
2. Modify the `Dockerfile` and/or `env.yaml` to add your tools or dependencies
3. Build and push your custom image
4. Update `studio-config.yaml` to reference your custom image

## Pre-built Image

The pre-built image is available at:

```
public.cr.seqera.io/platform/data-studio-xpra:6.2.0-r2-1-0.12.0
```
