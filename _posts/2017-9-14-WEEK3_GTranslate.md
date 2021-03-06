---
layout: post
title: Thoughts on Google Translate and AR Issues
published: true
---
Google Translate ([translate.google.com](http://translate.google.com)) is considered the gold standard for translation between various languages. It is not surprising to see the addition of "live translation" aka "image translation". This feature succeeds in segmenting an image or live camera feed and recognizing foreign characters. Not only that, it also succesfully supersedes the original text with an English translation (assuming foreign language to english translation is required)!

Let us first see three examples of such translation that I took in various locations on West Taylor Street here in Chicago.

## 1. **Spanish to English**

![Spanish Original]({{ site.url }}/assets/spanish_original.JPG)
![Spanish Translated]({{ site.url }}/assets/spanish.PNG)

The first image shows the original Spanish text taken from the Camera app. The second image shows the live translation feature Google Translate has. Speaking of accuracy, the algorithm did a fine job in translating the text. However, it was a pretty easy one to do.

## 2. **French to English**

![French Original]({{ site.url }}/assets/french_original.JPG)
![French Translated]({{ site.url }}/assets/french.PNG)

Again, we see a similar situation where a piece of French text needs to be translated. In this case, however, we see the application's lack of accuracy when translating the above text. It does a great job translating the syntactic meaning of the words, but fails to translate its semantic tone.

## 3. **Chinese to English**

![Chinese Original]({{ site.url }}/assets/chinese_original.JPG)
![Chinese Translated]({{ site.url }}/assets/chinese.PNG)

The Chinese text example worked really well considering the amount of text the app had to parse through to translate into English. The accuracy can be considered reasonable for the amount of translation done. One thing to notice in live usage was the frame rate considerably dropped to below 15FPS which is a user experience nightmare.

## Effective Use and Possible Future Use

As of now, Google Translate works reasonably well to translate text from one language to another. We can aim our phone's camera towards a piece of text and have it translated. This also requires an internet connection (but it can be waived by downloading the language pack which is about ~35MB). We can also feed the app an image of text to translate locally. However, this feature is limited to our use of the app within our smartphone. Currently, we do not see the world through our smartphone majority of the time (despite the overgrowing concerns that we definitely are!). Our field of view and vision is dependant on our eyes.

A reasonable assumption for the future can be that we might start wearing "smart glasses" (hint hint [Google Glass](https://www.x.company/glass/)) for the majority of our day. There will be a time when these glasses will be like our smartphone and may overtake our smartphones as the number one electronic device we use. I will refer to any future pair of AR glasses or contact lenses as "The Glass". What happens when "The Glass" dictates its features and usage to us rather than the other way around?

One possible test case could be that this translation feature turns on or off when the application feels is appropriate. In that case, if you are wearing "The Glass", how do you distinguish between real text and overlapped, translated text? How much is the user allowed to control of what is augmented and what is real? These are some ethical/implementation questions we must answer to ensure no malicious activity or "fake" information is conveyed to the user. We can assess the effectiveness of this feature by creating a PRO and CON list.

### PROS

1. **Real time translation** of text without any user interaction or prompts. The user does not have to open any application, input any commands, or press any buttons to have text translate. This also eliminates any delay or lag between the time when the user wants the translation and when the result is presented. Currently, when we translate from the Google Translate app, there is considerable delay between when the text is shown and when it is translated. This lag is amplified when the amount of text to be processed increases

2. **Data collection** for datasets so algorithms can train on them. Many translation algorithms use datasets to train their algorithms that do the actual translation. Google's [Neural Machine Translation System](https://research.google.com/pubs/pub45610.html) uses huge datasets to train the system to increase accuracy of translation. Google uses LSTMs (Long Short-Term Memory) Recurrent Neural Networks in its model. This constant stream of translation would definitely help Google train their model

### CONS

1. **Limited control** for user over content augmentation. The user, supposedly, would not have absolute control over how much of his field of vision would be augmented and how much would be real

2. **Accuracy/Authenticity** of translated/augmented data. Given that recent trends have translations increasing in accuracy, you can never be sure if the translation is 100% accurate. Even some photos I took could not reproduce the original intended meaning of the text with even 90% accuracy. There would be a trust issue between the user and the system

3. **Loss of original data** as the user cannot see what was really there. The user would have to turn off the system or remove "The Glass" itself to actually see what is there in real. That seems counterintuitive at best.

4. **Low performance** assuming today's technology. Finally, the performance would be a great deal of issue. With current tech, Google Translate itself suffers from framerate (< 15FPS) when it encounters more than 5 sentences in a foreign language.

## Final Thoughts

I believe the biggest issue is the amount of control the user should get over how much augmentation takes place when using the device ("The Glass"). Companies might be inclined to limit user control in order to provide a better experience (Apple does this too much), but this would lead to a worse experience for the user in the context of AR and translation.


These are some things to consider about the future of AR and Google translation in specific.
