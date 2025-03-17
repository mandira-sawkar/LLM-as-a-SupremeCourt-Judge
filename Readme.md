
---

# **README: Judicial Case Analysis Script**

## **Overview**
This script processes and analyzes the **JUSTICE** dataset to evaluate judicial decisions, normalize nested data, and uses an **OpenAI API** to perform deliberation analysis. It reads a JSON file (`oyez.json`) containing court case data and structures it for further analysis.

---

## **Features**
1. **Data Import and Normalization**:
   - Reads JSON data (`oyez.json`) into a structured `pandas.DataFrame`.
   - Flattens and normalizes nested JSON structures (e.g., votes, decisions) for cleaner tabular analysis.

2. **Exploding Nested Fields**:
   - Handles nested fields like `decisions` and `dec_votes` using `explode` to expand lists into individual rows.

3. **Data Cleaning**:
   - Removes unnecessary columns such as `joining`, `href`, `member.thumbnail` data, and more for cleaner output.

4. **Use of OpenAI API**:
   - Integrates the OpenAI API (key placeholder included) for further analysis, like summarization and opinion classification.

5. **Visualization**:
   - Uses `Matplotlib` and `Seaborn` for plotting trends and visualizing processed results.

---

## **Setup Instructions**

### **Dependencies**
This script requires the following Python libraries:
- `openai`
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `rapidfuzz`
- `scikit-learn`

Install dependencies using:
```bash
pip install openai pandas numpy matplotlib seaborn rapidfuzz scikit-learn
```

### **API Key Configuration**
To use the OpenAI API:
1. Replace the placeholder key `mykey` with your actual OpenAI API key.
   ```python
   mykey = "YOUR_API_KEY_HERE"
   ```

---

## **File Requirements**
- `oyez.json`: Input dataset containing judicial case details in JSON format.
- The script expects this file in the same directory as the script.

---

## **Usage**
1. Place `oyez.json` in the working directory.
2. Run the script: FinalVersion.ipynb
3. Outputs include:
   - A normalized `DataFrame` with clean, exploded fields.
   - Visualizations for data trends.

---

## **Output**
- A cleaned and normalized `DataFrame` for further analysis.
- Parquet files containing intermediate outputs of generated summaries or opinions.

---

## **Notes**
- The script processes nested JSON fields using `pandas.json_normalize` and `explode`.
- Replace the placeholder API key before use.
- OpenAI API usage may incur costs, so monitor API calls.

---
