# Day 01 — Python Virtual Environment

## The Problem
Different machines have different package versions.
Priya's laptop: scikit-learn 1.4.2
My server:      scikit-learn 0.24.1
Same code → different results.

## Why venv?
venv = isolated Python environment per project
     = like a separate VM for each project

| Concept | Linux Equivalent |
|---------|-----------------|
| venv | Separate VM |
| activate | SSH into VM |
| pip install | apt install inside VM |
| requirements.txt | Pinned package list |

## What I Did

### 1. Create virtual environment
```bash
python3 -m venv .venv
```

### 2. Before activate
```bash
which python3
# /usr/bin/python3  ← system Python
```

### 3. Activate
```bash
source .venv/bin/activate
```

### 4. After activate
```bash
which python3
# /root/code/datashield/fraud-detection/.venv/bin/python3  ← isolated
```

### 5. Install packages
```bash
pip install numpy pandas scikit-learn matplotlib
```

### 6. Snapshot versions
```bash
pip freeze > requirements.txt
```

## Key Learning
- `-m` flag = run Python module by name (like systemctl vs full path)
- `.venv` = industry standard name (hidden folder, auto-detected by editors)
- `pip freeze` = snapshot current environment
- `>` = redirect output to file (same as Linux)
- Never push `.venv/` to GitHub — add to `.gitignore`

## Output
- `requirements.txt` — exact pinned versions of all packages
