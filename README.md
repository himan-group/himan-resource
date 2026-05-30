# himan-resource Himan Source

Himan source repository for reusable agent resources.

## Use With Himan
<!-- himan:guide:start -->
Use these resources with [@hi-man/himan](https://www.npmjs.com/package/@hi-man/himan). Install it with `npm install -g @hi-man/himan` or run it with `npx @hi-man/himan --help`.

### 1. Bind source and set agent

```bash
himan source add team https://github.com/himan-group/himan-resource.git          # add the source to your local config
himan source use team                       # switch the current default source
himan agent use codex                       # set the current project's default agent
```

You can also bootstrap a new project in one step with `himan init <git_repo> --agent codex`.

### 2. View available resources

```bash
himan list             # list all active resources in the current source
himan list skill       # list only skill resources
himan list --installed # list resources installed in the current project
```

### 3. Install and uninstall resources

```bash
himan install skill <name>              # install one resource into the current project
himan install skill <name> -r           # install a skill with one dependency layer
himan install skill <name> -r --depth 2 # install a skill with deeper dependencies
himan install skill <name> -g           # install into user-level agent directories
himan uninstall skill <name>            # remove a project install and update himan.lock
himan uninstall skill <name> -g         # remove a user-level global install
himan install                           # restore everything from the current himan.lock
```

### 4. Develop, publish, and archive resources

Create new skills with your coding agent and the `himan-skill-metadata` skill, then use Himan to validate, publish, and manage them:

```bash
himan dev skill <name>                                                   # edit an installed resource in place
himan publish skill <name> --patch                                       # publish a new patch version
himan publish skill <name> -g                                            # publish and install globally
himan resource archive skill <name> --reason "Replaced by another resource" # archive a source resource
himan resource restore skill <name>                                      # restore an archived resource
```

- Resource versions are tracked by Git tags such as `rule/code-review@1.0.0`.
- Source maintainers can refresh this README and `CHANGELOG.md` with `himan source init-docs --repair-history`.
<!-- himan:guide:end -->

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
      <td width="288"><code>common-dev-pattern</code></td>
      <td width="112"><code>0.0.1</code></td>
      <td width="160"><code>9/10</code><br><small>常用，约束Coding Agent不要乱改</small></td>
      <td>Follow existing repository patterns for code changes and validate them before the final response. Use for nontrivial edits across pages, components, services, tests, build config, generated files, APIs, migrations, or integration code.</td>
    </tr>
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
      <td width="288"><code>himan-skill-metadata</code></td>
      <td width="112"><code>0.0.2</code></td>
      <td width="160"><code>9/10</code><br><small>创建/修改Skill时，自动补充himan规定的meta信息</small></td>
      <td>Create or update Himan skill metadata. Use when Codex creates, edits, migrates, or audits a skill folder with SKILL.md and should also generate or refresh a matching himan.yaml file containing category and static analysis metadata such as content token estimates, hashes, dependencies, scripts, MCP tools, and generation details.</td>
    </tr>
    <tr>
      <td width="288"><code>himan-resource-manage</code></td>
      <td width="112"><code>0.0.1</code></td>
      <td width="160">-</td>
      <td>Create, edit, validate, and publish Himan rule, command, or skill resources from project agent folders. Use when Codex needs to manage Himan resources with `himan create`, `himan dev`, project/global install target decisions, `himan publish`, lock-file verification, and a required Himan CLI version gate.</td>
    </tr>
  </tbody>
</table>

### Configs

No config resources yet.
<!-- himan:resources:end -->
