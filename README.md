# Project


This project was built using a modified version of the Harlowe Story format from [Twine](https://twinery.org/). The modified version of in [modified-harlowe-format.js](format.js).

This modified version of Harlowe adds supports for radio buttons, Bootstrap v4 and A-Frame.

## Getting Started

To use the modified harlowe format as the story format for your Twine story you need to import the custom format file into Twine.

1. Open the Twine story selection window.

2. On the right-hand panel click Formats

3. Click the Add a New Format tab.

4. Enter the following URL to get the latest version of reach, and click Add.

    https://cdn.jsdelivr.net/gh/FanMediaLab/webxr-twine/format.js


## Resources Used
Homepage Template source: https://startbootstrap.com/theme/creative

Image sources
* Scenario 1 homepage background: <a href='https://www.freepik.com/photos/drugstore'>Drugstore photo created by mrsiraphol - www.freepik.com</a>
* Scenario 2 homepage background: <a href='https://www.freepik.com/photos/pharmacist'>Pharmacist photo created by gpointstudio - www.freepik.com</a>
* Scenario 3 homepage background: <a href='https://www.freepik.com/photos/pharmacist'>Pharmacist photo created by aleksandarlittlewolf - www.freepik.com</a>
* Pharmacy Background and Nurse: <a href='https://www.freepik.com/vectors/shop-counter'>Shop counter vector created by pch.vector - www.freepik.com</a>
* Scenario 1 Waiting Area: <a href='https://www.freepik.com/vectors/hospital-patient'>Hospital patient vector created by pch.vector - www.freepik.com</a>


## Hosting
This project is hosted on [Netlify](https://www.netlify.com/). You can view the live version of the project on: https://elearning-pharmacy.netlify.app/. Netlify can easily be linked to your Github repo and deploy automatically when new changes are made.


## Web Speech API
The web speech api enabled the use of synthesized voices to read out the dialog. You can learn more about how it works [here](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API).
### Problems Encountered
* Keeping voices consistent across browsers and devices. Different operating systems provide different names for voices so we ran into an issue where the gender of voices would be different depending on the device and/or browser. Chrome also ships with own set of voices. We resolved this by identifying the the names and gender of voices avaiable on different operating systems and only using voices within our list. You can view [this website](https://talkrapp.com/speechSynthesis.html) to view the list of Apple related voices and this [StackOverflow link](https://stackoverflow.com/questions/51937113/what-are-the-standard-web-speechsynthesis-voices) for Microsoft related voices

* Reading stops mid text because provided text was too long. You can learn more about the problem [here](https://bugs.chromium.org/p/chromium/issues/detail?id=768199&q=component%3AInternals%3ESpeechSynthesis%20&colspec=ID%20Pri%20M%20Stars%20ReleaseBlock%20Component%20Status%20Owner%20Summary%20OS%20Modified). We resolved this by keeping the length of text provided to the `speak` to less than 230 characters. You can take a look at an [altervative workaround](https://stackoverflow.com/questions/57667357/speech-synthesis-problem-with-long-texts-pause-mid-speaking) from StackOverflow.
