# Pustaka Terbuka — IPG (Pusat Sumber Institut Pendidikan Guru Malaysia (KPM))

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Pusat Sumber Institut Pendidikan Guru Malaysia (KPM) (IPG) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Pusat Sumber Institut Pendidikan Guru Malaysia (KPM)** (`IPG`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `ipg` |
| **Agency Code** | `IPG` |
| **Official Name** | Pusat Sumber Institut Pendidikan Guru Malaysia (KPM) |
| **Institution Type** | `university` |
| **State / Territory** | Kuala Lumpur |
| **Target End Bib** | 250,000 |
| **OPAC Base URL** | [https://ipgm.moe.edu.my/library](https://ipgm.moe.edu.my/library) |
| **Subject Focus** | Pedagogy, instructional design, early childhood education, and teacher training |

---

## Directory Structure

```text
ipg/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/ipg/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/ipg/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-ipg.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/ipg/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Pusat Sumber Institut Pendidikan Guru Malaysia (KPM) (IPG)** & **Pustaka Terbuka**.
