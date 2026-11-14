# WildFire-RiskLoss-AI-Model
**Veritas AI High School Hackathon (Nov 14–15, 2026)** | *Climate, Finance & Health*

## What This Project Does
Forest fires are becoming bigger and more dangerous every year. They hurt our **planet (Climate)**, destroy homes and cost billions of dollars to put out **(Finance)**, and fill the air with toxic smoke that makes people sick **(Health)**.

I built an AI tool that looks at weather conditions (temperature, wind speed, humidity) and satellite heat signals to predict:
1. **How big** a wildfire could get (burn area in hectares)
2. **How much money** it could cost in property damage and firefighting ($ USD)
3. **How dangerous the smoke** will be for people breathing nearby (EPA Air Quality levels)

## How I Built It
- **15,500+ Real Fire Records:** I started with a global dataset of 15,500 wildfires across different regions and seasons.
- **Adding Realistic Finance & Health Data (21 → 27 Columns):** Since raw weather tables don't include dollar costs or smoke danger, I wrote Python formulas using real forestry cost rates and EPA air quality rules to add 6 new columns across all 15,500 rows.
- **Training the AI:** I tested two machine learning models—**Random Forest** and **XGBoost**. **XGBoost** scored better (`R² = 0.3169` vs. `0.3067`), meaning it learned the weather-to-damage patterns more accurately.
- **Testing on Real Historic Fires:** I tested the AI on two famous real-world disasters it had never seen before—the **2018 Camp Fire** and the **2025 Palisades Fire** in California. The AI accurately flagged both as multi-billion-dollar disasters with **Hazardous** air quality.

## Try the Interactive Simulator
Open `wildfire_risk_loss_model.ipynb` in Google Colab and scroll to **Cell 5** to use the live sliders. You can change the region, temperature, wind speed, and humidity to see how wildfire costs and health risks change in real time!
