# Semantic Frame Identifier

A Python/NLTK-based Natural Language Processing (NLP) tool for extracting semantic frames from text related to finance, commerce, and business.

`Vishnu_Jayanti_Semantic_Frame_Identification.pdf` -> Paper explaining research process
Paper can also be found [here](https://utdallas.app.box.com/v/HS-Research-2025/file/1954312683612)

This project identifies three semantic frames:

- **Capital Stock** – mentions of shares, stocks, stock types, issuers, and shareholders.
- **Commercial Transaction** – buying/selling events, buyers, sellers, goods, and monetary amounts.
- **Business** – organizations, locations, and descriptive attributes.

## Features

### Entity Correction
- Fixes and augments named entities (NER) using a custom gazetteer and manual heuristics.

### Financial Frame Detection
- Detects:
  - **Capital Stock**
  - **Commercial Transaction**
  - **Business**

### Frame Element Extraction
- Retrieves key semantic elements such as:
  - **Capital Stock**: shareholder, amount, stock, stock type, issuer
  - **Commercial Transaction**: buyer, seller, money, goods, unit
  - **Business**: company, descriptors, location

### WordNet Similarity Scoring
- Uses **Wu-Palmer** and **Leacock-Chodorow** similarity measures to detect lexical unit matches.

## How It Works

### 1. Tokenization & POS Tagging
- Uses NLTK to split text into tokens and assign part-of-speech tags.

### 2. Named Entity Recognition (NER)
- Extracts named entities and fixes misclassifications with a custom gazetteer.

### 3. Frame Identification
- Matches words against pre-defined lexical units for each frame.
- Uses WordNet similarity scores to detect semantically related terms.

### 4. Frame Element Extraction
- Searches surrounding tokens/entities for relevant elements.
- Handles special cases like multi-word amounts, monetary expressions, and possessives.

## Output
- Prints sentence along with detected frames and elements in a structured format.
