# Magical_cloak
Many of us know the magical cloak in HARRY POTTER which Harry uses to become invisible 
Here i have created a sample of that by using open compuer vision software which replaces the cloth with the background image.

Lets see what i have done to get the magic......

First i have captured the background image and stored it in background variable 

I iterated 30 times because to get perfect background 

Then i read the video from cap.read for ongoing changes and if the ret is not null the process continues basically ret is boolean. cap.read() returns two things one is boolean and another is image .

I used red colour cloth for this, We can use any of RGB but we should make changes in code for each colour 

Afterwards i converted the image from RGB to HSV.The purpose is we have advantage with HSV rather than RGB

