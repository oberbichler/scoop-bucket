# scoop-bucket

[Scoop](https://scoop.sh) bucket for [@oberbichler](https://github.com/oberbichler)'s tools on Windows.

## Usage

```powershell
scoop bucket add oberbichler https://github.com/oberbichler/scoop-bucket
scoop install oberbichler/<app>
```

## Apps

| App | Description |
| --- | --- |
| [`pdfnotator`](https://github.com/oberbichler/pdfnotator) | PDF viewer for pair-designing Typst documents with AI agents |

`pdfnotator` compiles Typst documents with the `typst` command: `scoop install main/typst`.

## How it is updated

Manifests live in `bucket/` as `<app>.json`. Each tool's release workflow
updates its manifest (version, URL, hash) with a `HOMEBREW_TAP_TOKEN` secret
that has write access to this repository. CI installs every manifest on
Windows to check it.

The apps are not code-signed. Scoop unpacks them without running an
installer, so there is no installer prompt, but Windows SmartScreen may warn
at the first start.

## License

ISC — see [LICENSE](LICENSE).
