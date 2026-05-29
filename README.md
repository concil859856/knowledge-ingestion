# knowledge-ingestion

CPU-only retrieval-augmented-generation (RAG) service for voice-agent
platforms. Ingest PDFs, URLs, sitemaps, and plain text per-agent;
serve sub-100 ms vector queries at runtime.

* Embedding model: BGE-small-en-v1.5 via [fastembed](https://github.com/qdrant/fastembed)
  (ONNX, no torch dependency)
* Vector store: [LanceDB](https://lancedb.com/) (embedded, columnar)
* HTTP API: FastAPI on port 8118

The container image is built and published to
`docker.io/vocence/knowledge-ingestion` on every push to `main` (tagged
`latest` and the short commit SHA) by the GitHub Actions workflow under
`.github/workflows/build.yml`.

The full developer docs live on the `ops` branch — they merge into
`main` with the first feature PR.
