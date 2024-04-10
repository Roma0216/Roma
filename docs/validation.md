# Validation
We put two videos recorded during the validation to show how our validation method works.
We also upload other videos.
Due to the size limitation, they are divided into two zip files ([1](validation/video1.zip), [2](validation/video2.zip)).

## Case 1
This example is an app with the VUI implemented by the variant version of Google VUI SDK.
In this example, the script clicks the microphone button to invoke the VUI and then immediately types "G" to the text box.
We can see that the text box firstly shows "G" and then the VUI-related dialog is opened.
A one or two seconds after we speak to the VUI, the VUI results returned.
The VUI is invoked before GUI, but the responses return after that of GUI.
This app is a translation app, so the GV-race may cause wrong translation results.
<div style="position:left">
      <video id="video" controls="" preload="none" poster="case1.jpg" width=200>
            <source id="mp4" src="case1.mp4" type="video/mp4">
      </videos>
</div>

## Case 2
This example shows an app with the VUI implemented by the Google VUI SDK.
In this example, the script clicks the microphone button to invoke the VUI and the user says "hello" to the VUI.
It is not easy to generate punctuations through the VUI, so the script clicks the "," button to enter a comma.
However, the text box shows the comma immediately.
A one or two seconds after we speak to the VUI, the VUI results returned.
The final result is ",hello" instead of "hello,".
The punctuation is expected to appear after the text, but instead before the text.
This app aims to help take notes, but GV-race results in wrong notes.
To correct this result, the user has to delete the comma and retypes it, complicating the original task.

<div style="position:left">
      <video id="video" controls="" preload="none" poster="case2.png" width=200>
            <source id="mp4" src="case2.mp4" type="video/mp4">
      </videos>
</div>