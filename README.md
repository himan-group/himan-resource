# himan-resource Himan Source

Himan source repository for reusable agent resources.

## Resources

<!-- himan:resources:start -->
### Rules

- No rule resources yet.

### Commands

- No command resources yet.

### Skills

- No skill resources yet.
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
