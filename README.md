# Lingo Blend

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)

---

This repository contains Python implementations for language classification and English translation tasks, specifically designed for Bengali, Hindi, Punjabi, Tamil, and Telugu languages.

## Overview

- Framework used: PyTorch, HuggingFace Transformers
- Languages: Bengali, Hindi, Punjabi, Tamil, Telugu

## Language Classification

Our language classification process utilizes the MuRIL (Multilingual Representations for Indian Languages) model. MuRIL is a state-of-the-art multilingual representation model developed specifically for Indian languages. The text is processed through the MuRIL to obtain embeddings which are passed through a dense layer for probability prediction. MuRIL is designed to handle code-mixed text effectively, making it ideal for processing Romanized code-mixed sentences.

## English Translation

Our process involves identifying the language, transliterating the text to the native script, and then translating it into English. We employ the MuRIL to identify the language of the given text as described in the language classification task. Once the language is identified, we transliterate the text into its native script using the Python-based transliteration tool IndicXlit, a multilingual transliteration model developed by AI4Bharat. After transliteration, we translate the text into English using a distilled version of the NLLB-200 (No Language Left Behind) model, primarily intended for research in machine translation, especially for low-resource languages.

## Acknowledgments
- The MuRIL model: [MuRIL model card](https://huggingface.co/google/muril-base-cased)
- IndicXlit: [IndicXlit GitHub Repository](https://github.com/AI4Bharat/IndicXlit)
- The NLLB-200 model: [NLLB-200 model card](https://huggingface.co/facebook/nllb-200-distilled-600M)

Feel free to contribute to the development and improvement of this project! Your contributions are valuable in advancing multilingual text processing techniques.
