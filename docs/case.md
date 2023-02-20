# Case Study
Some typical apps from the dataset are selected for the case study. 

## Case 1
The first figure shows the interface of our motivating example "com.voicenotebook.voicenotebook" app.
If we click the green microphone button on the left in the second picture, the VUI starts.
Then we say "hello word" to the app.
After that, as the third figure shows, we click the "," button.
Immediately, the "," text shows on the text box.
Then the ASR process returns and "hello word" is appended to the text box as the fourth figure shows.
Finally, the text box shows ",hello word" instead of "hello word,"

<center class="half">
    <img src="com.voicenotebook.voicenotebook.apk/page0.png" width = 175 text = "page0"/>
    <img src="com.voicenotebook.voicenotebook.apk/page1.png" width = 175 />
    <img src="com.voicenotebook.voicenotebook.apk/page2.png" width = 175 />
    <img src="com.voicenotebook.voicenotebook.apk/page3.png" width = 175 />
</center>


## Case 2
​The below four figures show the interafaces of the "com.kuarkdigital.android" app.
If we click the orange microphone button on the top left in the first figure, the VUI starts.
In the second figure, we say "Hello" to the app, place the cursor at the beginning of the text box, and tap "f" three times on the keyboard.
The "fff" text shows immediately on the text box as the third figure shows.
In the end, the ASR results returns and "Hello." is displayed on the text box.

<center class="half">
    <img src="com.kuarkdigital.android.apk/page0.png" width = 175 text = "page0"/>
    <img src="com.kuarkdigital.android.apk/page1.png" width = 175 />
    <img src="com.kuarkdigital.android.apk/page2.png" width = 175 />
    <img src="com.kuarkdigital.android.apk/page3.png" width = 175 />
</center>

The conflicting GUI action "enter the text to the text box" does not have a corresponding function like "onClick" to the "click a button" action.
GUI actions on widgets like "EditText" are implicit, but should be taken into consideration.


## Case 3
In the last case, we introduce an app that GV co-write, but successfully avoid the GV-race.
The first figure shows the interface of the "com.gawk.voicenotes" app.
If we click the microphone button on the left, the VUI starts.
Then a dialog fragment displayed at the bottom of this page.
We say "Hello how are you" to the VUI.
During the ASR process, the conflicting GUI actions are all disabled.
Besides, if we close the dialog fragment manually, the conflicting GUI actions are enabled but the VUI is cancelled immediately.
Finally, the ASR results return as the third figure shows.

<center class="half">
    <img src="com.gawk.voicenotes.apk/page0.png" width = 175 text = "page0"/>
    <img src="com.gawk.voicenotes.apk/page1.png" width = 175 />
    <img src="com.gawk.voicenotes.apk/page2.png" width = 175 />
</center>