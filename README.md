# ODTS

> [!IMPORTANT]
> **Documentation status:** `ODTS-Home` is the human-readable documentation for ODTS 1.9.5. The authoritative source is always [`ODTS-Specification`](https://github.com/Nijida-Studio/ODTS-Specification). This documentation may temporarily differ from the current reference implementation while an update is being synchronized.

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

Organization-level issue types and subtype fields are shared infrastructure. Repository-specific ODTS configuration and versioned issue metadata remain within each repository and are not replaced by a Project.
