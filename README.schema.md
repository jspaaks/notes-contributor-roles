# Preliminary `roles` schema

The file [schema.json](schema.json) describes how to update CFF's JSONSchema file for version 1.3.0. I wrote it for the [enum from sdruskat.net + recommendations](tax-sdruskatnet.md), but it would conceptually be the same for any given `enum`. Combine some online resources to try it out interactively:

1. JSONschema validator [https://www.jsonschemavalidator.net/](https://www.jsonschemavalidator.net/)
1. converting YAML to JSON here [https://onlineyamltools.com/convert-yaml-to-json](https://onlineyamltools.com/convert-yaml-to-json)
1. converting JSON to YAML https://www.json2yaml.com/

```yaml
# a contributor with one role, as array of string with one element
roles:
- conceptualization
```

```yaml
# a contributor with multiple roles, as array of string
roles:
- supervision
- artwork
- conceptualization
```

```yaml
# contributor with multiple roles, as mixed array of
# string and key-value pair, with free text added
# to explain
roles:
- supervision
- artwork: drawings
- conceptualization: description of conceptualization
    # "conceptualization" is a key in a dict of length 1
```

```yaml
# contributor with a role that doesn't fit the existing
# role names, according to the metadata author
roles:
- other: description of the other activity
```

Notes:

1. Some folks have advocated for having a free text field as CFF contributor role. This would not be useful for downstream usage, consumption by machines, and could hamper automatic validation of the contributor roles. But if we do it like I wrote in the schema file, you can have an element from an `enum`, or a `dict` key with an explanation. In YAML/CFF, this looks pretty clean.
1. The advantage of including an optional description is we can see if people need more roles / how they interpret existing role names.
