# TASI_ERAv2_S21

## Objective

1. Train the 124M parameter GPT2 model on the provided input data such that loss is less than 0.099999
2. Upload the model to HuggingFace Spaces as a Gradio App

## Dataset
Collection of William Shakespeare plays
- tiktoken - gpt2 tokenizer is used for tokenization
- Number of total tokens - 338025

## Steps


### Model Training
1. Refactored code in [gpt2_training](https://github.com/Azreal18/TSAI-ERAv2-S21/blob/main/gpt2_training.ipynb) notebook and model.py
2. Added model code to add the text generator function.
3. Added unscaling of GradientScaler before gradient clipping to fix high values of gradient norm values
4. Added code to save model arguments and weights that would need to be used for inferencing later
5. Pushed the model.py and saved model files to HuggingFace Model Hub using HuggingFace API from this [notebook](https://github.com/Azreal18/TSAI-ERAv2-S21/blob/main/gpt2_training.ipynb)

### Results
1. Model training achieved loss of 0.096994
2. Training speed was around 17k tokens / second
3. It took 397 steps to reach there.

### Gradio App in HuggingFace Spaces
1. Created app.py that can read the model  from HuggingFace Model Hub and launch the app
2. Pushed the model.py, app.py and requirements.txt to HuggingFace spaces using huggingface Upload option.

## The HuggingFace Spaces Gradio App

The app is available [here](https://huggingface.co/spaces/Azreal18/GPT2)  

![image](https://github.com/Azreal18/TSAI-ERAv2-S21/blob/main/imgs/GPT2_text.png)

