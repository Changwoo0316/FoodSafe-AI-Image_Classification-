# FoodSafe AI  
### _Food Name Prediction and Allergen Detection Web Application_

![logo](static/logo.png)

---

## Overview
**FoodSafe AI** is a web application that predicts the **food name** from an uploaded image and checks whether the dish contains **allergenic ingredients** or **user-specified ingredients to avoid**.  
It provides **bilingual UI (Korean / English)** and **voice guidance (TTS)** for accessibility and convenience.

---

## Features

### 1. Food Recognition (AI Model)
- Built with **PyTorch (ResNet18)** for image classification  
- Predicts Korean foods such as *bibimbap*, *kimchi stew*, *ramyeon*, *bulgogi*, etc.
- Supports model checkpoint loading (`.pt` or `.pth`)
- Automatically resizes and normalizes input images (224×224)

### 2. Allergen Detection
- Cross-checks predicted food ingredients with the selected allergen list  
- Detects common allergenic ingredients such as:
  - Egg, Milk, Wheat, Shellfish, Soy, Peanut, Pork, Beef, etc.
- Uses **RapidFuzz** for fuzzy matching between predicted food and recipe database (`api_xml.xml`)

### 3. Ingredient Avoidance Check
- User can input ingredients to avoid (e.g., cucumber, coriander, chili)
- The system analyzes recipe ingredients and highlights any matches.

### 4. Bilingual Interface
- **Korean ↔ English** language toggle  
- **Google Cloud Translation API** used (fallback logic included)  
- All UI text and detected results are dynamically translated

### 5. Voice Guidance (TTS)
- Uses **Web Speech API (speechSynthesis)**  
- Automatically announces results in selected language  
- User can replay the voice guide anytime

---

## Tech Stack

| Category | Technologies |
|-----------|---------------|
| **Frontend** | HTML5, CSS3 (inline), Vanilla JavaScript |
| **Backend** | Flask (Python 3.9+) |
| **AI Model** | PyTorch, torchvision (ResNet18) |
| **NLP / Utility** | RapidFuzz, pandas, xml.etree |
| **Translation** | Google Cloud Translate API (fallback supported) |
| **TTS** | Web Speech API (browser-based) |

---

## Project Structure

