# Validation
We put two videos recorded during the validation to show how our validation method works.
Other videos can be found [here](validation/video1.zip) and [here](validation/video2.zip).

## Case 1
This example shows an app with the VUI implemented by the variant version of Google VUI SDK.
In this example, the script clicks the microphone button to invoke the VUI and then immediately enters "G" to the text box.
We can see that the text box shows "G", then the VUI-related dialog is opened.
A one or two seconds after we speak to the VUI, the VUI results returned.
The VUI is invoked before GUI, but the responses return after that of GUI.
<div style="position:left">
      <video id="video" controls="" preload="none" poster="case1.jpg" width=200>
            <source id="mp4" src="case1.mp4" type="video/mp4">
      </videos>
</div>

## Case 2
This example shows an app with the VUI implemented by the Google VUI SDK.
In this example, the script clicks the microphone button to invoke the VUI and the user says "hello" to the VUI.
After that, the script clicks the ``,'' button and the text box shows "," immediately.
A one or two seconds after we speak to the VUI, the VUI results returned.
The final result is ",hello" instead of "hello,".

<div style="position:left">
      <video id="video" controls="" preload="none" poster="case2.png" width=200>
            <source id="mp4" src="case2.mp4" type="video/mp4">
      </videos>
</div>