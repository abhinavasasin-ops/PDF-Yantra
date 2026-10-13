PDF Chat
Ask questions about your PDFs and get answers with clickable page citations. A single HTML file: no backend, no build step, no install.
How it works:
Ingest: PDF.js extracts text per page in the browser.
Chunk: each page is split into overlapping ~180-word chunks tagged with file name and page.
Retrieve: BM25 keyword ranking (plain JavaScript) returns the top 6 chunks from the selected documents.
Generate: Google Gemini answers using only those excerpts
Verify: clicking a citation renders that page in the side reader.
Features
Multi-document chat with per-document selection
Page-level citations that open the source page
Grounded answers with explicit "not found" behavior
Dark mode, responsive layout, drag-and-drop upload
Run
Open index.html in a browser, paste a free Gemini API key (https://aistudio.google.com/apikey), and upload a PDF. The key is stored only in your browser's localStorage.
Privacy
PDFs are parsed locally. Only the retrieved passages are sent to the Gemini API.

Limitations
Scanned PDFs need OCR first
Keyword (BM25) retrieval can miss paraphrased questions; embeddings would improve recall
Tables and charts are extracted as plain text
Stack

Vanilla JavaScript · PDF.js · BM25 · Gemini API
