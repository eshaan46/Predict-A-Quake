# Earthquake Prediction Using LSTM

## Overview

Earthquakes are catastrophic natural disasters that can cause immense damage to lives and infrastructure. Early prediction of earthquakes can significantly reduce the impact by giving people and authorities time to prepare. This project leverages Long Short-Term Memory (LSTM) neural networks to predict the likelihood of an earthquake using micro-vibration data and other seismic features.

---

## Motivation

The idea for this project stems from the observation that **micro-vibrations**—which are imperceptible to humans—often occur days or weeks before a major earthquake. By analyzing these minute vibrations and other seismic indicators such as tectonic activity and proximity to fault lines, we aim to predict the likelihood of an earthquake with high accuracy.

---

## Project Highlights

- **Data Sources:** Synthetic datasets and real-world data (e.g., from the Bhuj earthquake) were used for training and testing.
- **Model Architecture:** A 5-layer **LSTM** model with 55 hidden units per layer was employed to learn temporal dependencies in seismic data.
- **Loss Achieved:** 
  - **Training Loss:** 0.04 (Mean Squared Error)
  - **Testing Loss:** 0.04 (Mean Squared Error)
- **Micro-Vibration Data:**
  - Micro-vibrations are measured in terms of amplitude and frequency over time.
  - These vibrations were analyzed in 10-time step sequences for prediction.

---

## Why LSTM?

- **Sequential Data:** LSTMs are ideal for handling time-series data because they can learn patterns and dependencies over time.
- **Capturing Long-Term Dependencies:** Unlike traditional RNNs, LSTMs solve the vanishing gradient problem, making them effective for analyzing long seismic patterns.
- **High Accuracy:** Our LSTM model achieved remarkable accuracy in predicting earthquake likelihoods, making it a reliable tool for early warnings.

---

## Model Input and Output

- **Input:** 
  - Sequences of 10 time steps, each containing features like:
    - Vibration Levels
    - Fault Proximity
    - Tectonic Activity
    - Historical Seismic Data
  - Shape: `(batch_size, sequence_length, input_size)`
- **Output:** 
  - Predicted earthquake likelihood as a percentage (1–100%).

---

## Key Results

1. The model successfully predicted earthquake likelihood with an **MSE of 0.04**.
2. Validation on synthetic and Bhuj earthquake data showed high reliability.
3. The model identified critical likelihood ranges:
   - **80–100%:** Imminent earthquake
   - **60–80%:** Likely earthquake within hours/days
   - **40–60%:** Moderate risk, requires monitoring

---

## Micro-Vibration Detection

The project relies on:
1. **Sensitive Vibration Sensors:** To detect subtle vibrations in the Earth's crust.
2. **Seismic Features:** Including fault proximity, tectonic shifts, and historical patterns.
3. **Advanced AI:** To analyze and classify vibration patterns as indicators of seismic activity.

### Why Micro-Vibrations?
- Micro-vibrations often precede major seismic events by hours to weeks.
- Analyzing these vibrations allows us to predict earthquakes **before they occur**, providing valuable time for preparation.

---

## Future Plans

1. **Integration with IoT Devices:**
   - Deploy vibration sensors in major cities.
   - Use satellite communication to transmit real-time seismic data.
2. **Improving Dataset Diversity:**
   - Incorporate real-world seismic data from global earthquake events.
3. **Open-Source Deployment:**
   - Make the model and codebase accessible for researchers and government agencies.

---
