# Alpaca Image Recognition: Image Acceptable Alpaca

Alpaca IR is a mini image-acceptable Chat AI can run on your own laptop. The chat model is based on [stanford-alpaca](https://github.com/tatsu-lab/stanford_alpaca) and [alpaca-lora](https://github.com/tloen/alpaca-lora).

## Example outputs

### Recognization 

**Image**:

 <img src="https://github.com/tripincloud/Alpaca_image_recognition/blob/master/examples/woman%20bath.png" width="350" height="200">

**Chat**: what is in the image

**Alpaca IR**: Three people in bathing suits are in a pool.

---

**Image**: 

<img src="https://github.com/tripincloud/Alpaca_image_recognition/blob/master/examples/food.jpeg" width="350" height="200">

**Chat**: what I can make for dinner if have food ingredients like these, and tell me how to do it

**Alpaca IR**: If you have food ingredients like these, you can make a vegetable stir-fry. Start by heating a tablespoon of oil in a large skillet over medium-high heat. Add the vegetables and stir-fry for 2-3 minutes, until the vegetables begin to soften. Add the garlic and ginger and stir-fry for an additional 1-2 minutes. Add the soy sauce and stir-fry for an additional 1-2 minutes, until the vegetables are cooked through. Serve the stir-fry over a bed of...


---

### Generation

**Image**: 

<img src="https://github.com/tripincloud/Alpaca_image_recognition/blob/master/examples/woman%20flower.png" width="400" height="200">

**Chat**: write a poem for the image

**Alpaca IR**: 

A woman with a flower in her hair, 

A beauty that can't be denied. 

The petals of the flower, so bright and fair, 

A symbol of life, a symbol of care. 

The flower in her hair, a symbol of joy, 

A reminder of life's beauty, a reminder of love. 

A reminder of life's beauty, a reminder of love. 

---

**Image**: 

<img src="https://github.com/tripincloud/Alpaca_image_recognition/blob/master/examples/pulp%20fiction.jpeg" width="250" height="400">

**Chat**: Tell me a story based on the given image

**Alpaca IR**: She was a young woman who had just moved into a new apartment. She was excited to explore her new surroundings, but she was also a bit overwhelmed. She decided to take it slow and started by reading the newspaper that had been delivered to her doorstep. As she read, she began to feel more at home in her new home.

---

**Image**: 

<img src="https://github.com/tripincloud/Alpaca_image_recognition/blob/master/examples/antman.jpeg" width="400" height="200">

**chat**: who you think would be the best actor of this character

**Alpaca IR**: Tom Hardy 

So here is a Tom Hardy fan wants him to be both Antman and Venom :)


### Fail examples 
---

**Image**: 

<img src="https://github.com/tripincloud/Alpaca_image_recognition/blob/master/examples/iphone1.jpg.webp" width="400" height="200">

**Chat**: What is the generation of this iphone?

**Alpaca IR**: It is an iPhone 11 

wrong, it is iPhone1

---


**Image**: 

<img src="https://github.com/tripincloud/Alpaca_image_recognition/blob/master/examples/exeggutor-pokemon.png" width="250" height="300">

**Chat**: What's this?

**Alpaca IR**: It is a stuffed animal toy with a plant in its mouth 

wrong, it is pokemon named Exeggutor.

---

## Usage (`Inference on pre-trained model`)

1. Install dependencies

```
pip install -r requirements.txt
```

2. If bitsandbytes doesn't work, [install it from source.](https://github.com/TimDettmers/bitsandbytes/blob/main/compile_from_source.md) Windows users can follow [these instructions](https://github.com/tloen/alpaca-lora/issues/17).


3. Run 
```bash
python generate.py \
    --load_8bit \
    --base_model 'decapoda-research/llama-7b-hf' \
    --lora_weights 'tloen/alpaca-lora-7b'
```






