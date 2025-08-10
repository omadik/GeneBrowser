
# 🧬 Gene Browser

An interactive web application for exploring genetic variant data.  
Gene Browser lets you search for a gene, view **gene information**, visualize data in **2D and 3D**, and browse **RSIDs** with short explanations and PubMed evidence counts.

---

## 🚀 Features
- **Gene Info Tab** – Displays a gene’s summary, coordinates, and metadata.
- **2D View** – Visualizes:
  - Mean allele frequency distributions
  - ClinVar variant positions
  - Gene structure diagrams
- **3D View** – Interactive protein structure viewer.
- **RSID Browser** – Searchable list of RSIDs with:
  - Allele frequency
  - HGVS notation
  - PubMed reference counts
  - One-click functional explanations

---

## 📦 Tech Stack
- **Backend:** FastAPI, Python
- **Frontend:** HTML, CSS, Vanilla JavaScript
- **3D Visualization:** NGL Viewer / 3Dmol.js
- **2D Visualization:** Plotly.js, Chart.js

---

## 🛠️ Installation & Usage

### 1. Clone the repository
```bash
git clone https://github.com/<username>/<repository>.git
cd <repository>
```

### 2. Create & activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows

```


### 3. Install dependencies

```bash
pip install -r requirements.txt

```

### 4. Run the backend server

```bash
uvicorn app.main:app --reload --port 8000
```

This will start the FastAPI backend at:

```cpp
http://127.0.0.1:8000
```

### 5. Open the frontend

Open frontend/index.html in your browser.

```cpp
project_root/
├── app/                # FastAPI backend
│   ├── main.py          # Entry point for backend
│   ├── routes/          # API endpoints
│   ├── plots2d_api.py   # 2D visualization routes
│   └── ...
├── frontend/           # Static HTML/JS frontend
│   └── index.html
├── 3d/                 # 3D viewer scripts
├── requirements.txt
└── README.md
```

### 💡 Example Workflow

Enter a gene name (e.g., BRCA1) in the search field.
Click Load Variants to retrieve gene data.
Explore:

    Gene Info – Coordinates, summary, metadata.

    2D View – Charts and gene structure visualization.

    3D View – Protein structure in interactive mode.

Browse RSIDs in the right-hand column and click one to see its functional explanation.
