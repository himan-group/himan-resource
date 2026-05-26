# himan-resource Himan Source

Himan source repository for reusable agent resources.

## Resources
<!-- himan:resources:start -->
### Rules

No rule resources yet.

### Commands

No command resources yet.

### Skills

#### Common

<table class="himan-resource-table" style="table-layout: fixed; width: 100%;" width="100%">
  <thead>
    <tr>
      <th width="288">Resource</th>
      <th width="112">Version</th>
      <th width="160">Score</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td width="288"><code>common-readme-writer</code></td>
      <td width="112"><code>0.0.1</code></td>
      <td width="160">-</td>
      <td>Create, evaluate, or rewrite concise README.md files for npm CLI and GitHub projects. Use when Codex needs to improve project positioning, highlight differentiators, simplify onboarding, split long reference content into docs, or apply README best practices to command-line tools, developer tools, plugins, SDKs, and similar open source packages.</td>
    </tr>
  </tbody>
</table>

#### Himan

<table class="himan-resource-table" style="table-layout: fixed; width: 100%;" width="100%">
  <thead>
    <tr>
      <th width="288">Resource</th>
      <th width="112">Version</th>
      <th width="160">Score</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td width="288"><code>himan-resource-manage</code></td>
      <td width="112"><code>0.0.1</code></td>
      <td width="160">-</td>
      <td>Create, edit, validate, and publish Himan rule, command, or skill resources from project agent folders. Use when Codex needs to manage Himan resources with `himan create`, `himan dev`, project/global install target decisions, `himan publish`, lock-file verification, and a required Himan CLI version gate.</td>
    </tr>
    <tr>
      <td width="288"><code>himan-skill-metadata</code></td>
      <td width="112"><code>0.0.1</code></td>
      <td width="160">-</td>
      <td>Create or update Himan skill metadata. Use when Codex creates, edits, migrates, or audits a skill folder with SKILL.md and should also generate or refresh a matching himan.yaml file containing static analysis metadata such as content token estimates, hashes, dependencies, scripts, MCP tools, and generation details.</td>
    </tr>
  </tbody>
</table>

### Skills

No config resources yet.
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
