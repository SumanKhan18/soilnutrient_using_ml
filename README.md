# soilnutrient_using_ml
🌾 ML-based system to predict soil NPK (kg/ha), classify nutrient levels (Low/Med/High), and recommend chemical &amp; biological treatments. Uses Random Forest models with pandas, scikit-learn, and matplotlib for visualization. Ideal for precision agriculture &amp; smart farming.📊🚜 



# 🌾 Smart Crop Suitability & Nutrient Deficiency Analyzer

This Python-based tool helps farmers and agronomists analyze crop suitability based on soil nutrient levels, identify nutrient deficiencies, suggest corrective chemical/biological solutions, and recommend alternative crops for better yield — all backed by data visualization.

---

## 🚀 Features

* ✅ **Crop Suitability Check**
  Predict whether a crop is suitable for cultivation based on soil and environmental conditions.

* 📉 **Nutrient Deficiency/Excess Detection**
  Calculates deviations in NPK and other soil parameters.

* 🧪 **Smart Solution Recommendations**
  Provides both chemical and biological remedies for deficient nutrients.

* 🌾 **Alternative Crop Suggestions**
  Recommends better-suited crops with match percentage.

* 📊 **Interactive Data Visualization**
  Pie, bar, and box plots for nutrient distribution and comparison.

---

## 📁 Dataset Structure

The model expects a CSV file with the following (sample) structure:

| crop\_name | season | n\_kgha | p\_kgha | k\_kgha | ph  | temperature\_c | ... |
| ---------- | ------ | ------- | ------- | ------- | --- | -------------- | --- |
| Potato     | Rabi   | 200-250 | 50-60   | 80      | 6.5 | 28-32          | ... |

ℹ️ You can extend this with additional soil metrics (moisture, sunlight, fertility, etc.).

---

## 🧪 Sample Usage

```python
user_params = {
    'n_(kgha)': 235,
    'p_(kgha)': 56,
    'k_(kgha)': 80,
    'humidity_%': 50,
    'temperature_c': 30,
    'ph': 6.5,
    'moisture_%': 40,
    'sunlight_intensity_lux': 30000,
    'fertility_uscm': 450,
}

test_model(df, "potato", "rabi", user_params)
```

---

## 📦 Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/soil-nutrient-analyzer.git
   cd soil-nutrient-analyzer
   ```

2. Install required packages:

   ```bash
   pip install pandas matplotlib seaborn numpy
   ```

3. Make sure your dataset CSV file is located correctly and path is updated in the script.

---

## 🧠 How It Works

1. Loads dataset and standardizes column names.
2. Parses ideal nutrient and environmental ranges.
3. Compares them with user inputs.
4. Calculates deficiency/excess and recommends actions.
5. Suggests alternative crops using match scoring.
6. Visualizes results using plots (NPK pie charts, bar plots, box plots).

---

## 📈 Visual Outputs

* ✅ Pie Chart for Ideal vs User NPK
* 📊 Bar Chart for Remaining Parameters
* 📦 Box Plots for Light & Fertility
* 🌾 Pie Charts for Alternative Crop NPK Profiles

---

## 📌 File Structure

```
├── soilnutrient.py
├── README.md
└── dataset/
    └── soil_nutrients.csv
```

---

🏁 Conclusion
This system supports decision-making in agriculture by:

Identifying nutrient deficiencies

Providing actionable fertilization guidance

Enabling sustainable farming practices

🛠️ Future Work
Integrate real-time IoT sensor data

Expand to multi-crop prediction

Web or mobile-based recommendation interface


🧪 Requirements
Install dependencies using:

bash

pip install pandas numpy scikit-learn matplotlib seaborn


🚀 Run the Project
Update the file path to your dataset:

python

file_path = r"C:\path\to\your\soil_nutrients.csv"

Then run the Python script to train, evaluate, and visualize the models.

## 📜 License

This project is licensed under the MIT License.


