# himan-resource Himan Source

Himan source repository for reusable agent resources.

## Resources
<!-- himan:resources:start -->
### Rules

- No rule resources yet.

### Commands

- No command resources yet.

### Skills

- `skill/himan-resource-manage@0.0.1`: Create, edit, validate, and publish Himan rule, command, or skill resources from project agent folders. Use when Codex needs to manage Himan resources with `himan create`, `himan dev`, project/global install target decisions, `himan publish`, lock-file verification, and a required Himan CLI version gate.
- `skill/himan-skill-metadata@0.0.1`: Create or update Himan skill metadata. Use when Codex creates, edits, migrates, or audits a skill folder with SKILL.md and should also generate or refresh a matching himan.yaml file containing static analysis metadata such as content token estimates, hashes, dependencies, scripts, MCP tools, and generation details.
<!-- himan:resources:end -->

## Usage

```bash
himan source add team https://github.com/himan-group/himan-resource.git --alias team
himan source alias default primary  # only needed when current default has no alias
himan source use team
himan list rule
himan install rule <name>
```

## Maintenance

- Add resources with `himan create <type> <name>`.
- Publish resource versions with `himan publish <type> <name>`.
- Record source-level changes in `CHANGELOG.md`.
- Resource versions are tracked by Git tags such as `rule/code-review@1.0.0`.
