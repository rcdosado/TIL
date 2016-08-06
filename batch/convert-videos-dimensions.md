#Convert Video Dimensions

TIL how to convert dimensions of videos from one to another

I am using FFMPEG, one of the best encoders out there. 

i think having an example explains it best

```Batch
ffmpeg -i in.mp4 -vf scale=394:216 out.avi
```

You may refer to this list for standard dimensions
---------------------------------------------------

```
Best Choice  2nd Best Choice 3rd Best Choice
640 x 480	 608 x 456	     624 x 468 
576 x 432	 544 x 408	     592 x 444 
512 x 384	 480 x 360	     560 x 420 
448 x 336	 416 x 312	     528 x 396 
384 x 288	 352 x 264	     496 x 372 
320 x 240	 288 x 216	     464 x 348 
256 x 192	 224 x 168	     432 x 324 
192 x 144	 160 x 120	     400 x 300 
128 x 96	368 x 276 
 	 	    336 x 252 
      	 	304 x 228 
      	 	272 x 204 
      	 	240 x 180
      	 	208 x 156
      	 	176 x 132
      	 	144 x 108 
      	 	112 x 84 

```
