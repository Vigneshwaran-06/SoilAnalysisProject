<h1 align="center">TerraScan</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Tkinter-GUI-FFA500?style=for-the-badge" />
  <img src="https://img.shields.io/badge/pandas-Data-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/CSV-Export-2E8B57?style=for-the-badge" />
</p>

## Overview

**TerraScan** is a Soil Fertility Analyzer — a smart desktop companion for monitoring soil health. It lets you log essential data like soil type, pH, moisture, and nutrient levels through a simple Tkinter interface, then save everything to CSV with a single click. Built for farmers, gardeners, and researchers who want an easy way to track and optimize soil conditions over time.

```
 _____ _____ ____  ____      _    ____   ____    _    _   _ 
|_   _| ____|  _ \|  _ \    / \  / ___| / ___|  / \  | \ | |
  | | |  _| | |_) | |_) |  / _ \ \___ \| |     / _ \ |  \| |
  | | | |___|  _ <|  _ <  / ___ \ ___) | |___ / ___ \| |\  |
  |_| |_____|_| \_\_| \_\/_/   \_\____/ \____/_/   \_\_| \_|
```

<p align="center">======================================================</p>
<p align="center"><b>TERRASCAN 🌱 Soil Fertility Analyzer</b></p>
<p align="center">======================================================</p>

## Features

- **Soil Data Logging**: Record soil type, pH, moisture, and nutrient levels (N, P, K, and more) in one form.
- **One-Click CSV Export**: Save every logged entry straight to a CSV file for easy sharing and record-keeping.
- **Simple Desktop GUI**: Built with Tkinter for a lightweight, no-install-hassle experience.
- **Data Handling with pandas**: Clean, structured data management under the hood for reliable reads and writes.
- **Farmer & Researcher Friendly**: Designed to be usable by anyone tracking soil health, from home gardeners to field researchers.

---

## Modules Used

<p>
  <img src="https://img.shields.io/badge/MODULE-DATA%20ENTRY%20FORM-8A2BE2?style=for-the-badge" />
  <img src="https://img.shields.io/badge/MODULE-SOIL%20TYPE%20LOGGER-1E90FF?style=for-the-badge" />
  <img src="https://img.shields.io/badge/MODULE-PH%20%26%20MOISTURE%20TRACKER-FF8C00?style=for-the-badge" />
</p>
<p>
  <img src="https://img.shields.io/badge/MODULE-NUTRIENT%20LOGGER-20B2AA?style=for-the-badge" />
  <img src="https://img.shields.io/badge/MODULE-CSV%20EXPORTER-DC143C?style=for-the-badge" />
  <img src="https://img.shields.io/badge/MODULE-DATA%20HANDLER%20(PANDAS)-DAA520?style=for-the-badge" />
</p>
<p>
  <img src="https://img.shields.io/badge/MODULE-GUI%20(TKINTER)-2E8B57?style=for-the-badge" />
</p>

---

## Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│  Tkinter GUI     │ -> │  Input Validation │ -> │  Soil Record     │
└─────────────────┘    └──────────────────┘    └─────────────────┘
                                                         │
                        ┌────────────────────────────────┴─────────────────┐
                        │                                                  │
                        ▼                                                  ▼
              ┌─────────────────┐                              ┌─────────────────┐
              │ pH / Moisture    │                              │ Nutrient Levels   │
              │ Fields           │                              │ (N, P, K, etc.)   │
              └─────────────────┘                              └─────────────────┘
                        │                                                  │
                        ▼                                                  ▼
              ┌────────────────────────────────────────────────────────────┐
              │                pandas DataFrame Builder                     │
              └────────────────────────────────────────────────────────────┘
                                          │
                                          ▼
                                ┌─────────────────┐
                                │   CSV Export      │
                                └─────────────────┘
```

---

## Project Structure

```
.
├── main.py                 # App entry point, launches the Tkinter GUI
├── gui/
│   ├── __init__.py
│   └── forms.py             # Soil data entry forms and widgets
├── data/
│   ├── __init__.py
│   ├── handler.py            # pandas-based data handling
│   └── soil_records.csv      # Saved soil data (generated on use)
├── utils/
│   └── validators.py         # Input validation for pH, moisture, nutrients
├── requirements.txt
└── README.md
```

---

## 📦 Installation

```bash
# Clone the repository
$ git clone https://github.com/Vigneshwaran-06/TerraScan.git
$ cd TerraScan

# Install dependencies
$ pip install -r requirements.txt
```

---

## 🚦 Usage

```bash
python main.py
```

1. Launch the app — the Tkinter window opens.
2. Enter soil type, pH, moisture, and nutrient values.
3. Click **Save** to log the entry to CSV.
4. Open the generated CSV anytime to review or analyze past readings.

---

## 🔧 Configuration

- **Output File**: Change the CSV save location/name in `data/handler.py`.
- **Tracked Fields**: Add or remove soil parameters in `gui/forms.py` and `utils/validators.py`.
- **Validation Rules**: Adjust acceptable ranges for pH, moisture, and nutrients in `utils/validators.py`.

---

## 🧪 Testing

```bash
python -m pytest tests/ -v
```

---

## 🤝 Contributing

Contributions are welcome! Please open issues and submit pull requests for improvements.

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

---

## 🔗 Related Technologies

- **Python** — Core language powering the app
- **Tkinter** — Built-in Python GUI toolkit
- **pandas** — Data structuring and CSV I/O
- **CSV** — Lightweight, portable format for soil records

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📞 Support

For questions or issues, please open an issue on GitHub or contact the development team.
