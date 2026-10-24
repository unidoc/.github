# UniDoc

PDF and Office libraries for Go, and open-source tools for Go supply-chain security and ISO 27001. UniDoc ehf. is an Icelandic company and has built these libraries since 2016.

## Document libraries

| Library | What it does | Licence |
|---|---|---|
| [**UniPDF**](https://github.com/unidoc/unipdf) | Create, edit, merge and split PDFs, fill forms, extract text and images, encrypt, redact, and sign with PAdES digital signatures. | Commercial, free trial key |
| [**UniOffice**](https://github.com/unidoc/unioffice) | Read, write and edit Word (.docx), Excel (.xlsx) and PowerPoint (.pptx) files. | Commercial, free trial key |
| [**UniHTML**](https://github.com/unidoc/unihtml) | Turn HTML into PDF. A UniPDF plugin that talks to the UniHTML rendering server, which runs in Docker. | Commercial, needs a UniPDF licence that includes UniHTML |

```sh
go get github.com/unidoc/unipdf/v5
go get github.com/unidoc/unioffice/v2
```

UniPDF and UniOffice are pure Go with no cgo: no native libraries, no JVM and no sidecar. Every dependency is an ordinary Go module, listed in `go.mod`, so you can check them with `go mod graph` and `govulncheck`. With an offline licence key they make no network calls.

pkg.go.dev does not show documentation for commercially licensed modules, so the API reference is at [apidocs.unidoc.io](https://apidocs.unidoc.io) and guides are at [docs.unidoc.io](https://docs.unidoc.io). The examples repositories have runnable code for most tasks: [UniPDF](https://github.com/unidoc/unipdf-examples), [UniOffice](https://github.com/unidoc/unioffice-examples), [UniHTML](https://github.com/unidoc/unihtml-examples). Get a trial key at [cloud.unidoc.io](https://cloud.unidoc.io).

## UniSupply: supply-chain checks for Go

[UniSupply](https://github.com/unidoc/unisupply) (Apache-2.0) checks a Go module's dependencies for known vulnerabilities and upkeep, and grades the risk from A to F with the reason and the fix. Run it on your own module or in CI.

```sh
go install github.com/unidoc/unisupply/cmd/unisupply@latest
```

## ISMS: your security management system in git

[ISMS](https://github.com/unidoc/isms) (Apache-2.0) runs an information security management system for ISO 27001 and similar standards. Policies and records live as documents in git, and the whole system ships as one binary. More at [isms.sh](https://isms.sh).

## Smaller tools

[PDF Debugger](https://github.com/unidoc/pdfdebug) (Apache-2.0) shows what is inside a PDF file. [UniChart](https://github.com/unidoc/unichart) (MIT) draws charts in Go. [UniType](https://github.com/unidoc/unitype) reads TrueType fonts in Go. [UniPDF CLI](https://github.com/unidoc/unipdf-cli) runs common UniPDF operations from the command line.

## Security

Report a vulnerability with **Report a vulnerability** in the repository's Security tab, or email security@unidoc.io. Our [security policy](https://github.com/unidoc/.github/blob/master/SECURITY.md) says what happens next, and [security.unidoc.io](https://security.unidoc.io) describes how we work.

Questions about licences or support: [unidoc.io/contact](https://unidoc.io/contact/).
