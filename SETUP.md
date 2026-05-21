# Environment Setup Guide

## Prerequisites
- Python 3.10 or higher
- pip (Python package manager)
- Git

## Installation Steps

### 1. Clone the Repository
```bash
git clone https://github.com/yuslizayusoff/AI-for-Mathematics.git
cd AI-for-Mathematics
```

### 2. Create a Virtual Environment (Recommended)

**On Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**On macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook
```

Navigate to the `modules` folder to start with Module 1.

## Troubleshooting

### Issue: "Python command not found"
**Solution:** Ensure Python is in PATH. On macOS/Linux, try `python3` instead.

### Issue: "pip: command not found"
**Solution:** Ensure pip is installed: `python -m pip install --upgrade pip`

### Issue: Jupyter notebook won't start
**Solution:** 
```bash
pip install --upgrade jupyter
jupyter notebook --version
```

## Verifying Setup

Run this command to check all packages:
```bash
python -c "import numpy, pandas, sklearn, tensorflow; print('✅ All packages installed!')"
```

---
**Happy learning! 🚀**