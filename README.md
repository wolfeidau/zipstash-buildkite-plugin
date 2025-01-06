# ZipStash Buildkite Plugin

Uses zipstash to cache dependencies.

# Example Configuration

```
steps:
  - plugins:
    - wolfeidau/zipstash#v0.1.0:
        id: go
        key: "{{ runner.os }}-{{ id }}-{{ checksum 'go.mod' }}"
        paths:
          - ~/.cache/go-build
          - ~/go/pkg/mod
```

## License

This application is released under Apache 2.0 license and is copyright [Mark Wolfe](https://www.wolfe.id.au).
