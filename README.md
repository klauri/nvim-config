# Custom NeoVim Config

## Plugins used
    - telescope
    - treesitter
    - packer
    - rose-pine (color scheme)

Plugin configs are in `after\plugins`
Installation files are in `lua\kirkl`

## LSP Server Install

### Go
To install golangci-lint server, run the following: 
```
    go install github.com/nametake/golangci-lint-langserver@latest
    go install github.com/golangci/golangci-lint/cmd/golangci-lint@latest
```

