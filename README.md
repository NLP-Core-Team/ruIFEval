# ruIFEval: Instruction Following Eval in Russian

This repository with source code and data was based on the original [article](arxiv.org/abs/2311.07911) and it was adapted aking into account the peculiarities of the Russian language.

## Install

Please make sure that all required python packages are installed via:

```
pip3 install -r requirements.txt
```

## How to run

You need to create a jsonl file with two entries: prompt and response.
Then, call `evaluation_main` from the parent folder of
instruction_following_eval. For example:

```bash
# Content of `--input_response_data` should be like:
# {"prompt": "Напиши 300+ слов ...", "response": "PUT YOUR MODEL RESPONSE HERE"}
# {"prompt": "Я планирую отправиться в путешествие ...", "response": "PUT YOUR MODEL RESPONSE HERE"}
# ...
python3 -m evaluation_main \
  --input_data=./data/ruIFEval.jsonl \
  --input_response_data=./data/response_gemini_pro.jsonl \
  --output_dir=./data/
```