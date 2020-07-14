# Magical_cloak
Many of us know the magical cloak in HARRY POTTER which Harry uses to become invisible 
Here i have created a sample of that by using open compuer vision software which replaces the cloth with the background image.

Lets see what i have done to get the magic......

First i have captured the background image and stored it in background variable 

I iterated 30 times because to get perfect background 

Then i read the video from cap.read for ongoing changes and if the ret is not null the process continues basically ret is boolean. cap.read() returns two things one is boolean and another is image .

I used red colour cloth for this, We can use any of RGB but we should make changes in code for each colour 

Afterwards i converted the image from RGB to HSV.The purpose is we have advantage with HSV rather than RGB

As i took red colour, In HSV red colour ranges from 0 to 10 degrees and 170 to 180 degrees So i took lower range and upper range by using numpy 

Now we got two ranges mask1 and mask2 our goal is to eliminate red colour and replace it with background 
so i added two masks
mask1 contains only the cloth part
mask2 contains all image except cloth 

MORPH_OPEN and MORPH_DILATE functions in opencv makes image more clear by eliminating noises

By using Bitwise operaters in OpenCV  i have added image , mask2 and background mask1.This step removes the cloth part in image and replace it with background

Then i added two results linearly by addWeighted() Function

Finallly we get the output video by c2.imshow()...


(Here "27" is the org key of escape By pressing esc screen will get vanish..!)
