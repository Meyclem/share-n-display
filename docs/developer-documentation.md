# Developer Documentation

## Disclaimer

This project is still under heavy development. The documentation is not up to date and the project is not ready for production (AT ALL 😄).

Module | Status
--- | ---
Dashboard | 🫥
Upload | 🫥
Display | 🫥
Cleaner | 🫥
Obsidian Share Plugin | 🫥

## Architecture

The project uses [Npm Workspaces](https://docs.npmjs.com/cli/v7/using-npm/workspaces) and is made of several parts:
- An Obsidian plugin that allows to share a note from an Obsidian vault. It is designed through the [Obsidian plugin documentation](https://docs.obsidian.md/Plugins/Getting+started/Build+a+plugin).
- A collection of Cloudflare Workers that handle the different parts of the project. Each worker is a separate application that can be deployed independently. They are designed through the [Cloudflare Workers documentation](https://developers.cloudflare.com/workers/).
  Each worker has its own README file with more detailed information:
    - [Dashboard](/workers/dashboard/README.md): the application responsible for managing the server configuration and users settings.
    - [Upload](/workers/upload/README.md): the worker responsible for uploading files to the server.
    - [Display](/workers/display/README.md): the application that requests and serves the shared note.
    - [Cleaner](/workers/cleaner/README.md): the worker responsible for cleaning up the server. It will delete files after a certain amount of time.

## Setup

You can install the dependencies for the project by running the following command from the project root directory:

```bash
npm install
```
