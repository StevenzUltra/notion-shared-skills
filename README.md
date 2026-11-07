# Notion Shared Skills

A portable skill for agents to find and read complete workflows from your own Notion skills library before asking questions already answered there.

## Install

1. Download this repository or its ZIP.
2. Put `SKILL.md`, `SETUP.md`, and `LICENSE` together in a `notion-shared-skills` folder in your agent's supported custom-skills directory. If your client supports importing skill folders, import that folder instead.
3. Connect your own Notion account using your agent's supported Notion connector and grant access to your skills library.
4. Follow [SETUP.md](SETUP.md) to configure the private library location and optional agent instruction.

The package provides instructions, not a Notion connector, executable plugin, or automatic migration script. Tool names and supported installation paths vary by agent. Keep private library URLs, account selectors, and credentials in your own configuration.

## What it does

- Finds relevant canonical skills and reads their supporting files.
- Handles pagination and packaged attachments when the client supports them.
- Keeps shared team workflows separate from system-provided skills and personal memories.
- Supports faithful maintenance and verified migration when requested.

See [SKILL.md](SKILL.md) for the complete workflow. Runtime behavior depends on the agent and connector; no cross-client runtime compatibility claim is made.

## License

Copyright (c) 2026 Steven Z. Released under the [MIT License](LICENSE). You may use, copy, modify, distribute, sublicense, and sell copies under its terms. Retain the copyright and permission notice. MIT does not transfer copyright ownership.

Only this package's instructions and documentation are included. Private libraries, third-party skills, attachments, and Notion trademarks or services are not licensed by this repository. This is an independent project, not an official Notion product.
