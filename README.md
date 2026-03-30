# 🌍 Language Detector (Mini NLP Project)

## 🚀 Overview

This is a **beginner-friendly NLP project** that detects the language of a given text input using the `langdetect` Python library.

👉 Example:

* Input: `Bonjour`
* Output: `French`

The project demonstrates how computers can identify languages based on **text patterns** without understanding meaning.

---

## 🧠 What You Learn

* Basics of **Natural Language Processing (NLP)**
* How **pretrained models** work
* Concept of **character patterns (n-grams)**
* Handling real-world issues like **incorrect detection**

---

## 🛠️ Technologies & Libraries Used

### 1. Python 🐍

* Main programming language used for implementation

### 2. langdetect 📦

* A lightweight NLP library used for language detection
* Based on **statistical analysis of character patterns**
* Works **offline** (no internet required after installation)

#### Key Functions:

* `detect(text)` → Returns language code (e.g., `"en"`, `"fr"`)
* `detect_langs(text)` → Returns probabilities of possible languages

---

## ⚙️ How It Works

```text
Input Text → Pattern Analysis → Language Code → Human-readable Output
```

### Steps:

1. User enters text
2. `langdetect` analyzes character patterns
3. It compares patterns with known language profiles
4. Returns a **language code**
5. Code is mapped to a readable language name

---

## 💻 Implementation

```python
!pip install langdetect

from langdetect import detect, LangDetectException

language_map = {
    "en": "English",
    "fr": "French",
    "hi": "Hindi",
    "es": "Spanish",
    "de": "German",
    "it": "Italian",
    "pt": "Portuguese",
    "nl": "Dutch"
}

try:
    text = input("Enter text: ")
    lang_code = detect(text)
    print("Detected Language:", language_map.get(lang_code, "Unknown"))

except LangDetectException:
    print("Text too short or unclear!")
```

---

## 🌐 Supported Languages

The model supports **50+ languages**, including:

* English
* French
* Hindi
* Spanish
* German
* Italian
* Portuguese
* Dutch
* And many more...

⚠️ Note: Only languages included in `language_map` will display properly. Others will show `"Unknown"`.

---

## ❗ Limitations (IMPORTANT)

### 1. Roman Hindi / Hinglish ❌

* Input: `namaste kaise ho`
* Output: Incorrect / Unknown

👉 Reason:
The model is trained on **native scripts**, not transliterated text.

✔ Works:

* `नमस्ते कैसे हो`

---

### 2. Very Short Text ❌

* Input: `Hi`
* Output: May be incorrect

👉 Reason:
Not enough data to detect patterns

---

### 3. Mixed Languages ❌

* Input: `Hello kaise ho`
* Output: Unreliable

---

### 4. Limited Mapping ❌

* If detected language code is not in `language_map`, output becomes `"Unknown"`

---

## ✅ Advantages

* Fast and lightweight ⚡
* No training required
* Works offline
* Easy to implement (beginner-friendly)

---

## 🔍 Example Outputs

| Input      | Output  |
| ---------- | ------- |
| Bonjour    | French  |
| Hello      | English |
| Hola amigo | Spanish |
| नमस्ते     | Hindi   |

---

## 🚀 Future Improvements

* Add **more languages** to `language_map`
* Handle **Roman Hindi / Hinglish**
* Show **confidence scores** using `detect_langs`
* Build a **web app using Streamlit**
* Support **multi-language detection**

---

## 📌 Key Takeaway

👉 This project shows that:

> Computers don’t understand language like humans — they detect patterns and make statistical guesses.

---

## 🧾 Conclusion

This mini project is a great starting point for NLP. It helps understand:

* How text is processed
* How models make predictions
* Real-world limitations of simple NLP systems

---

## 🙌 Author

Built as a beginner NLP project to understand the fundamentals of language detection.

---
