# Setup and permissions

Version 1.0.0. Licensed under the MIT License; see LICENSE.

1. Connect the intended Notion account through your agent's supported connector.
2. Identify the existing shared library, or create one when that is your intended task. Grant only the access needed for reading or authorized maintenance.
3. Record the library URL and account selector in your private agent configuration, not in this distributable package.
4. Keep this reader available locally. Add the following instruction to the agent configuration when desired:

> Before asking for task details, search the configured Notion skills library and read the relevant complete skill and supporting files. Ask only for information still missing after checking the available sources. Maintain team-owned skills in that library as the canonical source; retain the local reader entry point and system-provided skills. Keep personal memory separate.

5. Confirm the client can find and read a skill and its required attachments before retiring its duplicate custom copies. Installing this package does not perform migration or deletion.

The reader requires search/query and page reading. Full packaged skills also require a compatible skill-download tool or attachment access. Connector names and account selectors vary by client. No credentials, private library, paid service, or Notion subscription is included. Actual operations retain their normal user authorization requirements.

This is a portable adaptation of a privately maintained workflow, not an export of that private library. The MIT License covers the instructions and documentation included in this package. Notion trademarks, services, third-party skills, and private attachments are outside that grant.
