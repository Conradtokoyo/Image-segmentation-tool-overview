# Image-segmentation-tool-overview
Overview of an image segmentation tool created for a studio project 2020.
<br>
Readme created with https://github.com/rd123myb

Project team members
<br>
https://github.com/rd123myb
<br>
https://github.com/christenaong
<br>
https://github.com/t-chien-ho




# Overview
This UI created was in Tkinter which focuses on using superpixels via quickshift to segment images. Developed in collobaration with the Pattern Recognition and Machine Learning Lab (PRML) at the University of Otago.

![Overview Image](https://github.com/Conradtokoyo/Image-Segmentation-Tool/blob/main/Images/UI%20Overview.png)

# Steps
In order to get this application to work you need to install the dependancies.
To get started run the 'Superpixel Segmenation Tool.py' file.

## Load plastination image into application
The first thing to do is load the image into the application using the 'upload' button. The app accepts both JPG and PNG files but the type must be selected in the window to be visible (as shown below).
![Alt Text](https://gyazo.com/52661d8a56f63f087b6bc0a61864f4f2.gif)

## Sharpen the image
This increases the effectivness of the algorithms through exaggerating the distinctions between the pixels.

![Alt Text](https://gyazo.com/3c3d61b6a8eba5e19309b5219a05e331.gif)

## Create Over-segmentation
Once you have the file loaded in, experiment with different parameters using the sliders on the superpixel panel. The superpixel algorithm used in the UI is Quickshift and take three params: kernal size, max distance, and ratio. Check the wikipage for more details on the algorithm and how it works. 
![Alt Text](https://gyazo.com/1eb56099dd9fa25daa70181ac15c0019.gif)

## Clicked pixels to a mask
The superpixels are able to be selected by a mouse click to group superpixels to appropriate classes. Once the superpixels have been selected, click the 'combine' button to merge them into a mask. Two windows will pop up to show the binary index map and the applied merged superpixel. After closing the mask pop up windows, the image on the tkinter canvas will also have the superpixel regions merged.
![Alt Text](https://i.gyazo.com/40b8dda4575e94ea08a439b05326e328.gif)

## Colour
The "bound" button can be pushed to colour each unique superpixel to help identify each segment for merging.

# Alternative class splitting
There is also an option to use different algorithms to split classes. These would be great for further splitting superpixels that contain more than one class (future work).

RAG: Region Adjacency Graph
![Alt Text](https://gyazo.com/4e76e8a40809b41c1e508cc9a54b0755.gif)

GMM: Gaussion Mixture Model

![Alt Text](https://gyazo.com/e3c9a52ab19a4477686be0773232012a.gif)

K-Means:
![Alt Text](https://gyazo.com/d642e5a8fe7e974ee8896f8d78aefdf4.gif)

## Label merged pixels with tissue type ID
All the pixels of the same type in the image can now be semantically labeled. This is done with a JSON shapefile that goes with the regular image and is saved in the directory same directory as the .py file.

![Alt Text](https://gyazo.com/00acaae0000f4b85d25a3a693df0fa59.gif)




