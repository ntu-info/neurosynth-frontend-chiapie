# 🧠 Neurosynth Frontend

A responsive web frontend for exploring and querying neural studies using the Neurosynth backend API.  
🔗 **Page link:** [https://ntu-info.github.io/neurosynth-frontend-chiapie/](https://ntu-info.github.io/neurosynth-frontend-chiapie/)

---

## 🚀 Features

- **Dynamic Term Search:** Automatically fetches and filters related terms while you type — no need to press Enter.

- **Logical Queries:** Supports `AND`, `OR`, and `NOT` (case-insensitive) for combining search terms, e.g.  
  - `emotion AND memory`  
  - `language OR emotion`  
  - `language NOT speech`

- **Real-time Study Display:** Displays up to 50 matched studies per query with metadata like title, authors, journal, and year.

- **Abstract Handling:** Abstracts are not provided by the backend API, so the UI shows  *“Abstract unavailable (not provided by server)”* currently.

- **Clean & Responsive Design:** Built with **TailwindCSS** and optimized for both desktop and mobile screens.

- **Error & Loading Feedback:** Visual loading spinner, API error messages, and graceful fallbacks for network or server issues.

---

## 🧩 API Endpoints

Neurosynth backend hosted at: https://hpc.psy.ntu.edu.tw:5000


### Available Endpoints

| Endpoint | Description |
|-----------|--------------|
| `GET /terms` | Fetch all available research terms |
| `GET /terms/<term>` | Retrieve terms related to a given keyword |
| `GET /query/<term>/studies` | Retrieve studies associated with a term or logical query |

⚠️ *Currently, there is no `/study/<id>` or `/studies/<id>` endpoint. Hence, individual abstracts are not available.*

---

## 🌰 Example Queries

| Type | Example |
|------|----------|
| Single Term | `emotion` |
| Logical Query | `emotion AND memory` |
| Multiple Alternatives | `language OR emotion` |
| Exclusion | `language NOT emotion` |

The logical query processor handles Boolean operations in the correct order:
- **`NOT`** (exclusion)
- **`AND`** (intersection)
- **`OR`** (union)
