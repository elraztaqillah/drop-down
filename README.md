<h2><b>Intro</b></h2>

Hi everyone! this fix the problem drop-down in main.dart
>" lib/main.dart:38:30: Error: The argument type 'void Function(int)' can't be assigned to the parameter type   
'void Function(int?)?' because 'int?' is nullable and 'int' isn't. <p>OR</p> lib/main.dart:40:32: Error: A value of type 'int?' can't be assigned to a variable of type 'int' because
'int?' is nullable and 'int' isn't. "

please feedback and click star(top right corner) to support me. Thank you :)

<h2><b>How to fix the problem</b></h2>

![fixs](https://user-images.githubusercontent.com/76187141/133720384-b5762f0e-0959-4caf-bdd6-6fbe21fa4165.JPG)

<h2><b>Solution</b></h2>

![image](https://user-images.githubusercontent.com/76187141/133724857-00a14153-ab76-48b6-a61e-010c84ec16c0.png)

>There are tons of similar questions on SO. The issue is coming from the null safety feature adding the nullable types noted with a question mark int?.

You need to use the correct type just as putting a String into an int. Here you need to adapt you code in order to provide the correct types.

Sometimes you can use non nullables everywhere, perform manual checking, etc. You can read more about it here.

Regarding your issue, I'd say you have to modify you anonymous function codeSent:
<p>Example: </p>
(String verificationID, int? resendToken) => ...

https://stackoverflow.com/questions/68393585/how-to-fix-error-the-argument-type-void-functionstring-int-cant-be-assign

![image](https://user-images.githubusercontent.com/76187141/133724622-0f1114d8-276c-439f-b757-1254f721157e.png)

