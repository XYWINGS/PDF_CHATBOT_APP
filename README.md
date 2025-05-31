# RAG-Powered PDF Q&A Web Application

## Overview

This project is a Next.js web application that allows users to upload PDF documents and ask questions about their content using a Retrieval-Augmented Generation (RAG) model. The frontend is hosted on Netlify, while the RAG model API is deployed separately.

## Features

- PDF file upload and processing
- Interactive Q&A interface
- Responsive design
- Connection to custom RAG model API

## Prerequisites

- Node.js (v18 or later)
- npm or yarn
- Access to a RAG model API (or local instance) Ex: https://github.com/XYWINGS/PDF_Chatbot.git

## Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/XYWINGS/PDF_CHATBOT_APP.git
   cd rag-webapp
   ```

2. Install dependencies:

   ```bash
   npm install
   # or
   yarn install
   ```

3. Run the development server:

   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Deployment

### Frontend (Netlify)

1. Push your code to a GitHub repository
2. Sign in to Netlify and select "New site from Git"
3. Choose your repository and configure the build settings:
   - Build command: `npm run build`
   - Publish directory: `out` (for static export) or `.next` (for server-side)
4. Add your environment variables in the Netlify dashboard

### RAG API

This app works with a simple api design.

```Upload PDFs: curl -X POST RAG_MODAL_URL/upload -F "pdfs=@yourfile.pdf"```

```Ask a question: curl -X POST RAG_MODAL_URL/ask -H "Content-Type: application/json" -d '{"question": "What is a rag modal? "} ```
