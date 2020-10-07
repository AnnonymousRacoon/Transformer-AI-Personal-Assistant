# Transformer Personal Assistant with AI

**Mac OS Compatible only*

<a href = "https://drive.google.com/drive/folders/1m5mkpB4ERoy6kCGKUEscoAKVcs-VBAWn?usp=sharing">Click here for link (Too large for git)</a>

## Quickstart

To start run `ChatBot.py` and talk or type to your bot

## Commands

The bot takes voice or keyboard input, it is listening all the time

### Music
to play a song use `play...` or `play by...`

to skip a song use`skip`

to pause use `pause`

to skip to the next song use `skip`

### Search

to search google use `google...`

to search wikipedia say `wiki...` or `tell me about...`

### System

to send a message use `message...#` or `text...#`

to open a program use `open` (depending on your directory set up you may need to edit or append the dictionary of programs)

### Camera

to ask your bot to look around and identify objects say `look`

### Misc

for help say or type `help`

to quit use `quit`

to interupt your bo tmid scentence say `shut up`, `quiet` or `hush`



## Using the generative responses

### Using the pre-trained model

in `ChatBot.py` uncomment the following lines

```

# from TransformerChatbot import predict

```

and 

```
# self.previous = predict(' '.join(self.previous.split()[-5:]) + reply) if self.previous else predict(reply)
# self.say(self.previous)

```

and finally comment out the default response

```
self.say("I gotta be honest I can't think of a reply for that")
```

### Generating your own model

Currently the default model doesn't predict text very well. Largely down to the fact it requires a fast GPU and a significant number of days to train. If you fancy a crack at training it follow the steps bellow 

in `TransformerChatbot.py` uncomment the following lines:

```
# transformer.load_weights(checkpoint_filepath)
# # Model weights are saved at the end of every epoch
# transformer.fit(dataset,epochs=EPOCHS, callbacks=[model_checkpoint_callback])
```

Run your code and wait (a while)



