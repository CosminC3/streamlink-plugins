This repository was originally made by Damianonymous:
https://github.com/Damianonymous/streamlink-plugins

I added a few recorders for Chaturbate (Recorder_CB), MyFreeCams (Recorder_MFC), BongaCams (Recorder_BC), Camsoda (Recorder_CS) and Cam4 (Recorder_C4).
But, with just a little bit of work, many other sites can be added.

They are based on the Showup.bat recorder made by Damianonymous:
https://github.com/Damianonymous/streamlink-plugins/tree/master/Recorder

But with some improvements:
- the files/folders used by the recorders are searched and used in the folder where Recorder_\*.cmd is started. 
This way it is now truly portable.
- the title of the command/cmd window shows the status of the recorder:

Select model:

Name of the model (when is waiting between Streamlink attempts).

Name of the model written in uppercase - when it tries to connect and when is succeeding.
- the time interval between attempts is no longer a fixed value, it is randomly chosen between 45 and 75 seconds.
- if something was recorded during an attempt the next attempt will be started in 22..37 seconds.
Why a random value and not a fixed value: because, when you start multiple sessions, they tend to syncronize all together and then spam the site.
In a few minutes the site will temporary block your connection.

Usage:

1. Download Recorder_\*.cmd and \*\_Model.txt (same string for \* on both).
2. Download Streamlink_portable.zip and Streamlink_portable.z01 into the same folder.
3. Then decompress Streamlink_portable.zip into the same folder where you downloaded/copied Recorder_*.cmd.
4. Populate the \*\_Model.txt text file with the models names (only lowercase, one model per line, ONLY the names)..
5. Start Recorder_\*.cmd, choose model by index and hit Enter/Return. And repeat for all the models.

Useful informations:
- the time interval between attempts was calculated for an average PC/Laptop, for an average internet connection and for 5..10 sessions.
For other characteristics you may need to increase/decrease it.
- at the end of each of the Recorder_\*.cmd files you'll find a string looking like this "720p_alt,720p,best". Here you can set the video quality of the recording. 720p and 1080p are preffered; "best" automatically chooses the highest value but it isn't always preffered...

Have fun :)

TODO:
1. Set and use models' preferred hours. (wait time between attempts will be lower during and higher outside);
2. Combine all in one cmd batch and one models list;
3. Better handling errors;
4. Automatic start and stop for a model at specific time;
5. When model is in private enter in spy mode (payed).  But I think that should be implemented in Streamlink or in Streamlink plugins.
6. When it starts recording to notify the user by audio and/or by bringing the cmd window in front and so on. But that should be implemented in Streamlink or in Streamlink plugins, because Streamlink has full control when it starts downloading the stream.
7. Add an entry to the context menu of the default browser to add the model under the mouse cursor into the *_Model.txt.

