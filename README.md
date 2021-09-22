# Hack Technology / Project Attempted


## What you built? 

I built a short Alexa Skill that can keep track of the user's birthday, tell them how many days are left until their next birthday, and congratulate them when the big day comes. As this is an audio-based feature, I will attach a video of the complete experience, and some screenshots of the 'test console' Amazon provides for testing, showing the code as it runs.

To accomplish this, I first watched a quick (1h) JavaScript tutorial, as I feel me learning the language is overdue. JavaScript is the primary means of writing Skills, with Python also available. Then, I followed a tutorial by Amazon on how to create your first Skill, Cake Time. I did some small improvements to its capabilities of recognizing less 'correct' speech patterns (missing out on saying the month/year/day, some common ways of introducing the sentence such as 'my birthday is' or 'it's').

Demo on annexed videos (sorry! couldn't find a way to add to Markdown)

First video: named First Part

Second video: named Second Part

## Who Did What?

I, Gui, did everything :)

## What you learned

The first thing I learned is that JavaScript is quite convenient. I was a bit scared it would be too different from Java, which I know wasn't the smartest thing, as it turns out the Java in JavaScript helped me a lot in understanding it. As it is very likely my project could have something to do with web development or even Alexa itself (I am curious about IoF and assistive technology to do with scheduling), becoming more familiar with JavaScript could be useful later.

The meat of the project, however, was the Skill itself. Amazon Skills, turns out, are built on the Amazon Developer platform, which is quite handy. It is easy to navigate between writing back-end code for interpreting commands, front-end code to talk to the user and understand inputs, test the Skill itself with an online Alexa, and check AWS S3 for the data your Skill saves about the user. I learned a skill is built of a few main components:

**Back end:** 

* **Handlers** handle spoken commands from user, and speak back to user or prompt them for a new command.

* **Interceptors** take over command from a handler if we already have a piece of information saved; kind of an if statement function.

  ![](C:\Users\Gui Marinho\Desktop\dumdum\hack-a-thing-21f-1-gui-marinho\code.png)

**Front end:**

* **Invocation** is the process to call on your Skill to open. Mine simply opens when one says "Alexa, open Gui's BirthdayBot."

  ![](C:\Users\Gui Marinho\Desktop\dumdum\hack-a-thing-21f-1-gui-marinho\calls.png)

* **Intents** are the possible answers a user can give; all possible formats should be covered for how the user may answer, and one must also specify which handler should be called by the intent.

  ![](C:\Users\Gui Marinho\Desktop\dumdum\hack-a-thing-21f-1-gui-marinho\intent.png)

Now, of course, not everything is a rose garden. Alexa has some big limitations; the one that bothered me the most had to do with intents. An intent requires you providing it with all possible answers by users; when it comes to "when is your birthday?", answers with one or all of the components "month day year" **in this order** work fine. As a non-American, I quickly learned this system was already in need of improvement, as "day month year" did not work. One can easily think of answers that would be quite complicated to untangle, such as "next Tuesday" or "in two months" or "today". And all of this just to get one date! I can imagine how hard it would be to interpret more complicated patterns, with more boxes or more possibilities. I tried working on adding more possible answer types, but due to time and to my noob-ness in JavaScript it is taking some time.

On the flipside, Alexa has a number of useful presets developers can use as jumping off points. Have an agenda-related Skill? There's a template for that (which I plan to play with now that I know how to make a skill). Something like a simple game? Yes, there's a template. Looking for a month within the user's response? Alexa can do it for you. It is quite handy, and makes development a lot faster, since I can abstract away these simpler necessities. If I need to choose a personal assistant platform for my project, I'd definitely consider Alexa due to these development perks.

My final opinion was that Alexa is a very accessible platform to developers, with powerful text processing capabilities.  

## Authors

Gui Marinho '22'

## Acknowledgments

JavaScript tutorial I watched to get acquainted: https://www.youtube.com/watch?v=W6NZfCO5SIk

Alexa Skill tutorial: https://developer.amazon.com/en-US/alexa/alexa-skills-kit/get-deeper/tutorials-code-samples/build-an-engaging-alexa-skill/module-3