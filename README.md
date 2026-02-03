# pdfinjector
pdfinjector



## 1. Go Module Configuration

```go
// go.mod
module pdfinjector

go 1.21

require github.com/unidoc/unipdf/v3 v3.54.0

require (
	github.com/davecgh/go-spew v1.1.1 // indirect
	github.com/konsorten/go-windows-terminal-sequences v1.0.2 // indirect
	github.com/pmezard/go-difflib v1.0.0 // indirect
	github.com/sirupsen/logrus v1.5.0 // indirect
	github.com/stretchr/testify v1.8.0 // indirect
	github.com/unidoc/pkcs7 v0.2.0 // indirect
	github.com/unidoc/timestamp v0.0.0-20200412005513-91597fd3793a // indirect
	github.com/unidoc/unitype v0.2.1 // indirect
	golang.org/x/crypto v0.0.0-20220722155217-630584e8d5aa // indirect
	golang.org/x/image v0.0.0-20211028202545-6944b10bf410 // indirect
	golang.org/x/sys v0.0.0-20211216021012-1d35b9e2eb4e // indirect
	golang.org/x/text v0.3.7 // indirect
	golang.org/x/xerrors v0.0.0-20200804184101-5ec99f83aff1 // indirect
	gopkg.in/yaml.v3 v3.0.1 // indirect
)
```

## 2. Installation and Usage

### Install Dependencies:
```bash
go mod init pdfinjector
go mod tidy
```

### Build the Program:
```bash
go build -o pdfinjector
```

### Usage Examples:

1. **Basic usage (with default metadata):**
```bash
./pdfinjector /path/to/pdf/folder
```

2. **Custom metadata:**
```bash
./pdfinjector /path/to/pdf/folder \
  --title "My Document" \
  --author "John Doe" \
  --subject "Technical Report" \
  --keywords "report,technical,2024" \
  --creator "Go PDF Processor" \
  --producer "Custom Producer"
```

3. **Partial metadata update:**
```bash
./pdfinjector /path/to/pdf/folder --author "New Author" --title "New Title"
```



## Key Features:

1. **Batch Processing**: Processes all PDFs in a folder recursively
2. **Flexible Metadata**: Update title, author, subject, keywords, creator, producer
3. **Command-line Interface**: Easy to use with command-line arguments
4. **Safe Operations**: Uses temporary files to avoid data loss
5. **Error Handling**: Continues processing even if some files fail
6. **Cross-platform**: Works on Windows, macOS, and Linux

## Notes:

- The program uses the UniDoc library which is robust for PDF manipulation
- Make sure you have Go installed (version 1.16 or later recommended)
- For production use, consider adding more error handling and logging
- Test on sample PDFs before processing important documents
- Some PDFs with DRM or advanced encryption may not be editable

