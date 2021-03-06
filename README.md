SimpleBash
==============

SimpleBash has a simple aim of provind a simple layer on the most used BASH commands via an English Sentence. Once a stable SimpleBash is created we will give an option of *routing* all the commands by default via SimpleBash and if the command is then not found, only then do a bash execute.


Reason for the need of SimpleBash
---------------------------------

- This will be a lightweight *routing* of commands to original commands.
- Every program differs slightly in the way it requires the parameters and you either should've used it a lot to remember or you do a manual check for the command.
- Terminal is daunting for new users because of differing syntax of programs.
- There are some really cool features and commands that are not being used regularly. For example - **sudo !!** which otherwise could have been very unforgetful if it were **simplebash sudo last command**
- Imagine shell scrips which are utterly more readable, doing extremely complex file conversions, uploading and bit manipulation without really knowing the programs needed to do that.



Reasons not to use SimpleBash
-----------------------------

- You need to type a much longer sentence *but you probably can save a lot of time no searching the correct syntax*


Development Approach
---------------------

- This script will be a bash shell script so that there are no dependencies other than bash.
- SimpleBash will follow a plug-in model. i.e. - Any scripts added to the **.simplebash/plugins** folder will be included individually.
- The commands will roughly follow this model **simplebash <english_verb> <parameters_forming_sentence>** 
- You can find the present sytax by typing **simplebash <english_verb> help** . For example - **simplebash find help**
- Every command will have the option of poviding alias for the command via the command line **simplebash create alias for "find param1 in all"**
- Hitting tabs will try to complete the sentence as much as possible with 
- Later versions should have one english sentence can and should use multiple commands to achieve the result, in case others fail. Therefore, future versions can do conversion using different programs and install dependencies itself.


SimpleBash Examples
--------------------

- **simplebash find every file matching the regex "/S.+" in this folder and subfolder and be case insensitive**  // To do *file . -iname "/S.+"*  - which one is more readable?
- **simplebash convert file "audio.mp3" to "audio.wav"** // This will do an *ffmpeg -i audio.mp3 -o audio.wav*
