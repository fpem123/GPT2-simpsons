# GPT2 Simpsons

[![Run on Ainize](https://ainize.ai/images/run_on_ainize_button.svg)](https://ainize.web.app/redirect?git_repo=https://github.com/fpem123/GPT2-simpsons)

This project generate The Simpsons script using GPT-2 model.

Fine tuning data: [Kaggle](https://www.kaggle.com/feniksm/simpsons?select=script_lines.csv)

Model download: [Google drive](https://drive.google.com/file/d/1-HyiwDHft1eSQudleWTi18myDdCPZdEB/view?usp=sharing)

### Model information

    Base model: gpt-2 large
    Epoch: 30
    Train runtime: 20515.6554 secs
    Loss: 0.0394

### How to use

    * First, Choose The Simpsons character name.
    * Second, Fill what the character will say in text. This will be base of script.
    * And then, Fill number in length. Text is created as long as "length". I recommend between 100 and 300.
    * If length is so big, generate time will be long.

### Post parameter

    name: The Simpsons character name.
    text: The base of script.
    length: The size of generated text.(min: 50)

### Output foramt

    {"0": [[character name, dialog], [character name, dialog], ...]}

### Image reference

    static/README.md

## * With CLI *

### Input example

    curl -X POST "https://master-gpt2-simpsons-fpem123.endpoint.ainize.ai/simpsons" -H "accept: application/json" -H "Content-Type: multipart/form-data" -F "name=Homer Simpson" -F "text=Hello everyonew" -F "length=100"

### Output example

    {
      "0": [
        [
          "Homer Simpson",
          " Hello everyone."
        ],
        [
          "Bart Simpson",
          " Homer."
        ],
        [
          "Homer Simpson",
          " Wake up, boy."
        ],
        [
          "Homer Simpson",
          " Be honest. (POINTED) The girl's not doing it well."
        ],
        [
          "Lisa Simpson",
          " She needs to work on her game"
        ]
      ]
    }

## * With swagger *

API page: [In Ainize](https://ainize.ai/fpem123/GPT2-simpsons?branch=master)

## * With a Demo *

Demo page: [End-point](https://master-gpt2-simpsons-fpem123.endpoint.ainize.ai)
