## 1. API & Backend

- [ ] Add PDF upload endpoint.
- [ ] Add document ID management for uploaded files.
- [ ] Add endpoint for asking questions about a specific document.
- [ ] Add health check endpoint.
- [ ] Add request/response validation with Pydantic schemas.
- [ ] Add proper error handling for invalid PDFs, empty questions, and missing documents.

## 2. PDF Processing

- [ ] Improve PDF text extraction.
- [ ] Handle pages with empty or non-extractable text.
- [ ] Store page numbers for extracted text.
- [ ] Add support for multiple uploaded PDFs.
- [ ] Add metadata for each document, including filename, upload time, and page count.

## 3. Chunking

- [ ] Improve chunking strategy based on paragraphs or sentences.
- [ ] Add configurable chunk size and overlap.
- [ ] Preserve page number and source file for each chunk.
- [ ] Avoid splitting important context in the middle of sentences.

## 4. Embedding & Retrieval

- [ ] Normalize embeddings before indexing.
- [ ] Use cosine similarity or FAISS `IndexFlatIP`.
- [ ] Add configurable `top_k` retrieval.
- [ ] Add support for multilingual embedding models.
- [ ] Return retrieval score with each result.
- [ ] Store and load FAISS index from disk.

## 5. LLM Answer Generation

- [ ] Add LLM integration for generating final answers.
- [ ] Build a prompt template using retrieved context.
- [ ] Add source-aware answers with page references.
- [ ] Prevent answering when context is insufficient.
- [ ] Add optional conversation history support.

## 6. Response Format

- [ ] Return final answer separately from retrieved chunks.
- [ ] Include source filename, page number, chunk text, and score.
- [ ] Add consistent JSON response format.
- [ ] Add clear error responses.

## 7. Configuration

- [ ] Add `.env` support.
- [ ] Move model name, chunk size, overlap, and `top_k` to config.
- [ ] Add environment-based settings for local and Docker execution.
- [ ] Add default values for all required settings.

## 8. Docker & Deployment

- [ ] Improve Dockerfile.
- [ ] Add `.dockerignore`.
- [ ] Add Docker Compose setup.
- [ ] Make data and index folders persistent using volumes.
- [ ] Add startup command documentation.

## 9. Repository Cleanup

- [ ] Add `.gitignore`.
- [ ] Remove unnecessary cache files.
- [ ] Organize project folders.
- [ ] Move sample files to a dedicated sample data directory.
- [ ] Keep production data out of the repository.

## 10. Testing

- [ ] Add unit tests for PDF extraction.
- [ ] Add unit tests for chunking.
- [ ] Add unit tests for embedding and retrieval.
- [ ] Add API tests for upload and ask endpoints.
- [ ] Add tests for invalid inputs and edge cases.

## 11. Logging & Monitoring

- [ ] Add structured logging.
- [ ] Log uploaded documents.
- [ ] Log retrieval results for debugging.
- [ ] Log errors with useful messages.
- [ ] Add basic request timing logs.

## 12. Documentation

- [ ] Improve README.
- [ ] Add installation guide.
- [ ] Add Docker usage guide.
- [ ] Add API examples with `curl`.
- [ ] Add sample request and response.
- [ ] Add project architecture overview.
- [ ] Add explanation of the RAG pipeline.

## Priority Roadmap

### Phase 1 — Core Improvements

- [ ] Add PDF upload endpoint.
- [ ] Add document-based question answering.
- [ ] Store page numbers and metadata.
- [ ] Improve response format with sources.

### Phase 2 — Better RAG

- [ ] Improve chunking.
- [ ] Improve embedding model.
- [ ] Normalize embeddings.
- [ ] Add LLM-generated answers.

### Phase 3 — Production Readiness

- [ ] Add config management.
- [ ] Add Docker Compose.
- [ ] Add tests.
- [ ] Improve logging.
- [ ] Complete documentation.
