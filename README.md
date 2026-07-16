# ODTS

> [!IMPORTANT]
> **Documentation status:** `ODTS-Home` is the human-readable documentation and currently describes a pre-1.0 development state. The authoritative source is always [`ODTS-Specification`](https://github.com/Nijida-Studio/ODTS-Specification). Its `main` branch is currently the unreleased ODTS 1.0 release candidate. Until a versioned release is published, this documentation may differ from the current specification and may contain errors or older artifacts.

ODTS is a narrow reference framework for agile project management. It helps developers plan work as issues and establish code structure, documentation, and tests before completing the implementation.

ODTS is primarily intended for software development, but the Epic → Item → Task planning model can also be used for other projects.

## Start here

- Read the [ODTS Specification](SPECIFICATION.md).
- Follow the [installation guide](INSTALLATION.md) to configure an organization and create a project from the two ODTS templates.
- Use the [contribution workflow](CONTRIBUTING.md) when implementing work with ODTS.
- Use the [Project template checklist](PROJECT_TEMPLATE_CHECKLIST.md) when maintaining the reference Project.

`ODTS-Specification` is the authoritative source for ODTS behavior. `ODTS-Home` provides human-readable explanations and additional documentation and may temporarily differ from the current specification.

## The two templates

ODTS uses two separate GitHub templates:

1. The **ODTS-Specification repository template** provides the reusable GitHub configuration without an ODTS README or other documentation that must be deleted from the new repository.
2. The **ODTS-Specification Project template** creates the planning views and workflows.

Organization-level issue types and issue fields are shared infrastructure. They are configured once for the organization and are not replaced by either template.
