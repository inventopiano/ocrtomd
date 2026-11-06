# OCR to Markdown

A native **macOS** app that turns **PDFs and images into Markdown**, entirely on your Mac.

Built for people who feed documents to language models: Markdown is what agents read best, and a clean Markdown file is worth more than a scanned PDF. No uploads, no accounts, no subscriptions.

Each version is available on the Releases page (direct download) and on the Mac App Store.

<!-- Immagine di copertina: aggiungi il file e decommenta la riga
![OCR to Markdown](docs/header.png)
-->

## Why

Scanned documents and PDFs are where useful context gets stuck. OCR to Markdown pulls the text out and writes Markdown — headings, lists and tables included when the model recognises them — so it can go straight into a RAG pipeline, a second brain, a personal or company wiki.

Everything happens locally: the OCR models run on your Mac, documents never leave it, and the app keeps working offline once the model is downloaded.

## Features

### Compatibility

macOS 14 or later. Universal: Apple silicon and Intel.

### Input and output

- Drag PDFs or images into the window, or pick them from the Finder.
- One file or a whole batch: the queue shows progress per file and lets you cancel a single job or the entire batch.
- Markdown is saved automatically to the folder you choose, with a numbered suffix if the name already exists.

### OCR models

Pick the model that fits the page:

- **GLM-OCR** — general text and tables, fast.
- **PaddleOCR-VL 1.6** — difficult scans, multi-column layouts, 100+ languages.
- **MinerU2.5-Pro** — complex layouts and tables in a single pass.
- **DeepSeek-OCR** — challenging pages and blank-page detection.

Models are downloaded once from Hugging Face and stay on disk.

### Interface

- 24 languages, including right-to-left Arabic.
- Dark, compact window designed to stay out of the way.
- Native SwiftUI app, sandboxed, no telemetry.

### Free, with a tip jar

The app is free and has no ads. If it saves you time you can leave a contribution from the tip jar in Settings: it opens the App Store purchase sheet, or RevenueCat's web checkout in the direct-download build. Tips are voluntary and unlock nothing.

### Updates

- Mac App Store builds update through the App Store.
- Direct-download builds update themselves via **Sparkle**, signed and notarized.

## Built with

Swift and SwiftUI, [RevenueCat](https://www.revenuecat.com) for the tip jar, [Sparkle](https://sparkle-project.org) for updates, and [llama.cpp](https://github.com/ggml-org/llama.cpp) (via `llama.swift`) to run the OCR models locally.

## Developed with

Built with [OpenCode](https://opencode.ai) and a small set of local OCR models, iterating on real documents — receipts, contracts, scanned notes and academic papers.
