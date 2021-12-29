# imread_unchanged
OpenCV: imread() Method “IMREAD_UNCHANGED” Flag Is Explained


```ruby
cv2.imread(“filename”, flags=)
```

**It requires us to input two arguments.**

The first argument is “filename” as string.
The filename can be written in two ways.

```ruby
cv2.imread(“C:/Users/cagat/Desktop/image.png”, flags=)
```

Here is some important notes to avoid errors.
-Write whole string in quotation mark: “ ”
-Use “/” while writing the location. Location information can be found under the properties of the picture.
-Write image name correctly with its extension or format
-Do not change the image location after coding

![image](https://user-images.githubusercontent.com/84636881/147708004-d984fcd1-c75d-430f-b7cb-16c326977164.png)

**2. Just image name and format but with one condition.**

```ruby
cv2.imread(“image.png”, flags=))
```

You can also declare image location just with its name and format BUT the project file (.py file) and image must be in the same folder!

![image](https://user-images.githubusercontent.com/84636881/147708025-2ddfe9fe-1015-4286-a32e-e4e13fa1e693.png)

I suggest you to use this method which gives a clean coding and more organized file structure for you.

Let’s continue with the second argument: Flags=
Flags are like options. You choose how image should be read from the source. For this method flags are called as ImreadModes or imread flags. We have 13 different modes to set the type of flags. These methods can be found in the documentation of OpenCV at docs.opencv.org

![image](https://user-images.githubusercontent.com/84636881/147708042-a9057c5f-1422-49c9-a1fd-ac0d862be95e.png)

In this story, I will just focus on IMREAD_UNCHANGED flag which is described as below in the documentation.

![image](https://user-images.githubusercontent.com/84636881/147708052-c3cd45ec-a931-48c8-84ea-42c441d3503c.png)

Let’s focus on the term “with alpha channel”..
You can think the image as the complied color values in an array. An image has 3 color channels: Red, Green and Blue Channel and the forth one is Alpha Channel.

![image](https://user-images.githubusercontent.com/84636881/147708064-0ab5c43c-71ab-48aa-ad8a-ea20a8229c0c.png)

IMREAD_UNCHANGED allows us to read the Alpha Channel of an image.

Alpha channel describes the transparency of the image. Transparency can be described as it is or with the term “Opacity” or “Alpha Value”. Let me visualize it for you.

![image](https://user-images.githubusercontent.com/84636881/147708077-97a51900-91ab-4682-8670-1f289191cf58.png)

So I assume that I clarified the Alpha Channel part.

![image](https://user-images.githubusercontent.com/84636881/147708082-49c694e2-16b2-44ae-a308-447f0150b66c.png)


Let’s continue with the term “Ignore EXIF information”
EXIF is the abbreviation of Exchangeable Image File Format which stores numerous information in its metadata at the moment that we shoot. These information may include values as it shown below.

![image](https://user-images.githubusercontent.com/84636881/147708096-1d5ce5d5-970f-48db-bd10-4a2415de9476.png)

The important EXIF information for us when we read an image with IMREAD_UNCHANGED flag is “orientation” of an image. EXIF orientation information stores the positioning of the camera with respect to the ground. This allows us to take pictures disregarding the orientation of the camera.

![image](https://user-images.githubusercontent.com/84636881/147708103-4ff391c9-ee8b-453a-9ccd-2506fe566c77.png)

So basically EXIF orientation is ignored with IMREAD_UNCHANGED flag.

One line of code stores many stories inside. This is all from me for now..



