# Spearphish-Company

<h2>Description</h2>
Project consists of spearphising a company through HR by attaching shell to a pdf fake resume in a new persona.
<br />

<h2>Languages and Utilities Used</h2>

- <b>Putty(Linux)</b>
- <b>Remote Desktop</b>
- <b>Firefox Thunderbird</b>
- <b>Metasploit</b>


<h2>Environments Used </h2>

- <b>Amazon WorkSpace</b>

<h2>Spearphish Company through HR</h2>

To get an executable to spearphish, I use metasploit. I ran exploit/windows/fileformat/adobe_pdf_embedded_exe. From here, I set all the parameters to create an emebbed adobe file to attach to my resume.

I moved my resume over to the attack box. I tested it and it spawned the shell. I did a few persistence methods to ensure my shell remains open. I used local persistence and made two copies. One in the C:\Users\ephemeral\documents
And the other in the default temp folder.

After, I migrated the resume shell to be able to remain open even when the resume itself is closed. I migrated it to explorer.exe. I am currently working on escalating privileges to be able to create a shadow copy using vss_privilege. 


<p align="center">
Connection shell<br/>
<img src=https://s3.amazonaws.com/gbstool/submissions2020/269128/adobeshell.PNG?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20240301T150947Z&X-Amz-SignedHeaders=host&X-Amz-Expires=36900&X-Amz-Credential=AKIAJBIZLMJQ2O6DKIAA%2F20240301%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=223e405a29909e0f95566d36ef820d56192598ee8d9c4f97015b2404a9c42dff
<br />

<p align="center">
Resume/Persistence<br/>
<img src=https://s3.amazonaws.com/gbstool/submissions2020/269128/localpersistence.PNG?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20240301T150947Z&X-Amz-SignedHeaders=host&X-Amz-Expires=36900&X-Amz-Credential=AKIAJBIZLMJQ2O6DKIAA%2F20240301%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=054d7b542ca0cb42cc809edfcce579b14b3c3798c1fcfbe9626488fa96ec79a9
<br />


<p align="center">
Migrate<br/>
<img src=https://s3.amazonaws.com/gbstool/submissions2020/269265/persistence1hr.PNG?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20240301T151522Z&X-Amz-SignedHeaders=host&X-Amz-Expires=36900&X-Amz-Credential=AKIAJBIZLMJQ2O6DKIAA%2F20240301%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=88fdbeea3fcca2c2b71cf04b2ff3abebd94f7a1b6d193967ea47b06d130a5b71
<br />

<b>Message in persona</b>

Gregor,

 

I was able to gain access to . I used an embedded adobe pdf disguised as a resume to gain access to the device of an HR computer. In order to maintain persistence, I put a copy in the temp file named r35me000.exe and migrated the resume to explorer.exe. Attached is the screenshot of the HR desktop, proof of connection and persistence methods.

 

CeleanaS00

<p align="center">
HR Desktop<br/>
<img src=https://s3.amazonaws.com/gbstool/submissions2020/269265/cTRdjZpK.jpeg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20240301T151522Z&X-Amz-SignedHeaders=host&X-Amz-Expires=36900&X-Amz-Credential=AKIAJBIZLMJQ2O6DKIAA%2F20240301%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=5519067220838c87b48e1c44f315f76b4e51907e4d15f942b2850a9df5319d13
<br />

<p align="center">
GETUID<br/>
<img src=https://s3.amazonaws.com/gbstool/submissions2020/269265/hrscreenshot.PNG?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20240301T151522Z&X-Amz-SignedHeaders=host&X-Amz-Expires=36900&X-Amz-Credential=AKIAJBIZLMJQ2O6DKIAA%2F20240301%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=0f4ea3569560a5cf940375d5fc033f83f84def9556712e29a96fe8b7b9a12949
<br />
