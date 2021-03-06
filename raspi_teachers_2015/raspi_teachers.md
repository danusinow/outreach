# DDPSC Raspberry Pi Teacher's Workshop: Working with Raspberry Pi

##Introduction to Raspberry Pi

*  See slide decks [here](https://github.com/danforthcenter/outreach/tree/master/raspi_teachers_2015/Presentations)
*  See these websites for more information on how to use Raspberry Pis:
    *  [https://www.raspberrypi.org/](https://www.raspberrypi.org/)
    *  [http://sonic-pi.net/](http://sonic-pi.net/)
    *  [https://learn.adafruit.com/category/raspberry-pi](https://learn.adafruit.com/category/raspberry-pi)
    *  [http://www.raspberrypitutorials.yolasite.com/](http://www.raspberrypitutorials.yolasite.com/)

##Putting the Operating System (OS) on the Raspberry Pi
In this session we will learn to work with Raspberry Pi computers and later the Raspberry Pi camera module. Raspberry Pi computers are small, single-board computers that cost between $20-35.
The Raspberry Pi computers you will work with today are Pi 2 Model B ($35, 4-core ARM CPU, 1GB RAM) [Link](https://www.raspberrypi.org/products/raspberry-pi-2-model-b/).
Our Raspberry Pis are running a Linux operating system "Raspbian" which is a fork of Debian 7 "Wheezy." The operating system is on the microSD card in your Pi. We've 'flashed' the cards for you
but if you want to do one yourself you can download the operating system from the [Raspberry Pi website](https://www.raspberrypi.org/downloads/). For Mac users we recommend using the free program
ApplePi-Baker that is available [here](http://www.tweaking4all.com/hardware/raspberry-pi/macosx-apple-pi-baker/) putting a disk image on a card, scroll down to download the **non-sudo version**.
For Windows users options for flashing cards can be found [here](http://www.tweaking4all.com/hardware/raspberry-pi/install-img-to-sd-card/#windows).  

##Next we will set up the Raspberry Pi configurations

For more information see the [Raspberry Pi Github Page](https://github.com/raspberrypi/documentation/blob/master/configuration/raspi-config.md). There will be more on using github later.

To go back to the configuration window

```

sudo raspi-config

```


In addition to the command-line interface, Raspberry Pi computers can run a desktop environment. To start it type after logging in:

```
startx

```

##Basic Linux operations  

What is Linux?: Linux is an operating system, which is software that supports basic computer functions.
Other examples of operating systems are Unix, Mac OS, Windows XP or Windows 7. You can do things like,
make files, move files, copy files, make directories (folders) etc. etc. but instead of seeing icons like a
Windows or Mac interface you would use text (the command line).


From the desktop you can run a terminal program to continue to use the command-line interface (called LXTerminal).

##Basic Linux shell commands  

If you need help on how/why to use a command the best thing to do is to google it.  

**pwd** - print the current working directory path. The "working directory" means the folder you are currently in.  

**ls** - list the files and directories in the current working directory

**cd** - change directories directly to *home*

**cd** ***dir*** - change directories from the current working directory to *dir*

**touch** ***file*** - create the empty file *file*

**rm** ***file*** - remove the file *file*

**mkdir** ***dir*** - make the directory *dir*

**rmdir** ***dir*** - remove the directory *dir* (has to be empty)

**cp** ***file1*** ***file2*** - create a copy of *file1* called *file2*

**cp -r** ***dir1*** ***dir2*** - create a copy of *dir1* and its contents called *dir2*

**mv** ***file1*** ***file2*** - move/rename *file1* to *file2*

**head** ***file*** - print the first 10 lines of *file* to *stdout*

**tail** ***file*** - print the last 10 lines of *file* to *stdout*

**less** ***file*** - opens *file* using a paging viewer

**htop** - display the current running processes (task manager/activity monitor). It is a modern version of **top** which should be available if **htop** is not.

**df -h** - display disk usage with human-readable units

**gzip** ***file*** - compress *file*

**gunzip** ***file.gz*** - decompress *file.gz*

**tar zcf** ***archive.tar.gz*** ***dir*** - create a compressed archive of *dir* (or a set of files)

**tar zxf** ***archive.tar.gz*** - decompress and extract the contents of *archive.tar.gz*

**Ctrl+C** - stop the current command

**exit** - log out of the current session

**sudo** ***command*** - execute *command* with administrator privileges

**apt-get install** ***program*** - apt-get is the Debian Linux package manager. You can use it to install new software on your computer

**apt-get update** - update the installed packages on your system 


##Introduction to Github and other websites of interest.

*  [Github](https://github.com/): Github is a way to code collaboratively, or to find code to jumpstart your project.
Github + Jekyll + Markdown is also an easy way to set up a website for your projects. 


To clone a repository in LXterminal type:

```

git clone https://github.com/danforthcenter/outreach.git

```

We won't be doing this today, but you can also add data to a repository if you've made changes.

Four steps add data to a repository (that you have permissions to you can also do a 'pull' request that is asking for permission to push):
1)  To add data to a repository: (make sure you are in right folder)

```
# the . means to add all
# instead of adding all you can add specific files
git add .

```
2)  To commit data to a repository:

```
# commit the additions to the repository
# minimally needs a metadata message
git commit -m "adding new data to this repository"

```

3)  Pull the repository so that you make sure you are adding data to the newest version of the repository.

```
# make sure your version of the files are up to date before you try to add new things to the repository
git pull

```

4)  Push your data to the repository.

```
# push your new data to the repository
git push

```

Other important websites to check out:
*  Thingiverse has lots of patterns to 3D print [here](https://www.thingiverse.com/)
*  Raspberry Pis are computers but Arduino microcontrollers are also very useful for projects [here](https://www.arduino.cc/)
*  OpenScad is a free program to design 3D objects [here](http://www.openscad.org/)
*  More info on github pages [here](https://pages.github.com/)
*  Jekyll is a tool to help develop your website with Github [here](https://help.github.com/articles/using-jekyll-with-pages/)

##Pi passwords and backing up disk images

**More from Noah**

**Changing Pi Passwords**

**Backing up files etc.**

You should always have a backup of programs that you've spent significant time on. One method of doing that is to have a github
repository with all of your important working scripts that you can download if something gets deleted or modified.
Another method is to save a disk image.


##Introduction to Soldering

Soldering is basically like metal glue. We will be soldering a small IR light panel so that we can take images at night.

*  More on how to solder [here](https://learn.adafruit.com/adafruit-guide-excellent-soldering/tools)
*  And [here](https://github.com/danforthcenter/outreach/tree/master/raspi_teachers_2015/How%20to%20solder)


##Using the Raspberry Pi camera

The Raspberry Pi camera module is a 5 megapixel, fixed-focus camera add-on for the Raspberry Pi. Each of your Raspberry Pi computers has a camera module installed. Your camera module is the Pi NoIR model (the infrared filter has been removed).

## Take a picture

To take a picture, see it, and save it with the name *image.jpg* use the following command:

```python

# This command will take a picture but it will put it in whatever
# working directory (folder) you are in.

# The -o is an option/flag that tells the program what we want to
# name the image and also where to put it. If it is just the name
# it puts the image in whatever folder you are currently in.

raspistill -o image1.jpg

# To see where you've save the image
# (what folder you are currently in) type:

pwd

# To see the names of the files in your current folder type

ls -l

```

**Pro-tip, if you want to rerun a command that you recently used, you can hit the uparrow to get to previous commands**

To actually view the image, you can go to the file folder icon on the desktop and open the file or on the command line...

```

display /home/pi/images/image1.jpg

```

##Flip a picture if it is upside down

Is your picture upsidedown when you look at it? If it is you will need to add the -vf (vertical flip) flag to your command.

```

raspistill -vf -o image1.jpg

```

## Save images with unique names and some metadata
If you add the current date and time to the name of your images you can use the same command over and over again because each image will have a unique name and doesn't get overwritten.


To take a picture, see it, and save it with the date and time in front of the name image.jpg in the directory images in your home folder use the following command: 

```
# the name of the image below would include the current year,
month, day, hour, minute, and second

raspistill -o /home/pi/images/$(date +"%Y-%m-%d_%H:%M:%S")_images.jpg

# now press the up arrow, the command you just ran
should show up, take another picture.
```

##Configure the Bright Pi module to add lighting to our images
In order to use the Bright Pi module we need to set up our Raspberry Pi computers to use the GPIO pins following the instructions at [Adafruit](https://learn.adafruit.com/adafruits-raspberry-pi-lesson-4-gpio-setup/configuring-i2c).

Next, wire your Bright Pi light module following the wiring instructions on screen and at [Pi Supply](https://www.pi-supply.com/bright-pi-v1-0-assembly-instructions/).

Because our Bright Pi LED lights are infrared we cannot look at them to see if they are on and working. But, because we are combining the Bright Pi light modules with the PiNoIR camera modules we can use the camera to see if the lights work. The [Pi Supply](https://www.pi-supply.com/bright-pi-v1-0-code-examples/) page describes the basics of controlling the Bright Pi with I2C [Inter-Integrated Circuit](https://en.wikipedia.org/wiki/I%C2%B2C) commands.

For today's workshop we will demonstrate controlling both the Bright Pi light module and the camera module using the Python programming language. Let's go over the example script, LightsCameraAction.py, that was cloned with the Github repository.

```
python LightsCameraAction.py --help

usage: LightsCameraAction.py [-h] [--on] [--white] [--ir] [--off]

Turn on/off Pi Bright LED lights.

optional arguments:
  -h, --help  show this help message and exit
  --on        Turn all the lights on (default: False)
  --white     Turn on the white lights only (default: False)
  --ir        Turn on the IR lights only (default: False)
  --off       Turn all the lights off (default: False)
```

## Take a time-lapse

After you take a few pictures and are satisfied with the setup you can take a time-lapse

```
# to take a timelapse you need to use the -tl option, which is the time between images, but the time is in milliseconds
# you also need the -t option, which tells the program how long to run timelapse
# the command below takes an image named using the timestamp every 3 seconds for 1 min
# We cannot use the timestamp to name the images because how the program is written, but we can use another way of naming the images
# by nameing the images image%05d.jpg we tell the program to give the image a 5 digit number at the end of the name
# So the first image would be named image00001.jpg

raspistill -t 60000 -tl 3000 -o /home/pi/images/image%05d.jpg 

```

## What happens if the computer shuts off during the time-lapse?  

In order to make sure that the computer will keep running the time-lapse if the computer shuts off you need to modify
crontab.

## Use cron to take images on a schedule (time-lapse)

Crontab is an easy way to schedule repeating tasks so it can be used as another way to do time-lapse imaging, like time-lapse imaging.  

First we will disable the red light on your camera  

```
#This opens up the config.txt file in using the leafpad text editor program  

sudo leafpad /boot/config.txt  

#Then add the following to the end of the file to diable 

disable_camera_led=1

#Then save and exit
```  
Now make a folder called timelapse and open crontab in a text editor

```

#let's make another folder so that we don't confuse it with the first timelapse

mkdir /home/pi/timelapse2

#This opens up the crontab file in using the leafpad text editor program

sudo leafpad /etc/crontab
```

Crontab file format:

```
# Example of job definition:
# .---------------- minute (0 - 59)
# |  .------------- hour (0 - 23)
# |  |  .---------- day of month (1 - 31)
# |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
# |  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
# |  |  |  |  |
# *  *  *  *  * command to be executed
```

add the following line to the cron file (you should see a list of commands that also start with an astericks).

```
#this tells the command to run every 10 min of every hour every day of the month every day of the week.

*/10 * * * * pi /usr/bin/raspistill -o /home/pi/timelapse2/$(date +"\%Y-\%m-\%d_\%H:\%M:\%S")_timelapse.jpg

#save the file and close it

```

now we need to restart the cron and the pi to make sure the changes take effect. On the command line type

```
sudo service cron restart  

sudo reboot

```

Can I test my commands before putting them into crontab?
- Yes! Just run them on the command line first in the terminal!!!!
- Why use crontab?
  - It will automatically run task as scheduled, even after reboot!
  - Time is set after booting and internet access, but if no internet, it will set time to last available time, which can cause problems. Hope you have wifi!!!!
  - Alt: can hardwire a clock with battery.


## Assembling your time-lapse into a short movie

first we need to write all of image names into a text file, but we can do that using the command line  

```

# This takes all of jpg files in your current folder and writes their names to a file called stills.txt 

cd /home/pi/timelapse2/

ls *.jpg > stills.txt

#If you only wanted to use every other image (we won't be doing this)
awk 'NR%2==0' stills.txt > stills_even.txt

```  

now we can assemble the files into a time-lapse movie  


```
# -ocv tells the mencoder program what video format to use  
# -lavcopts tells the opctions you want for the video format (size etc.)
# -o tell the program what to name your file
# -mf tells the program what file format and the number of frames per second that you want, as well as the file with all the image names

mencoder -nosound -ovc lavc -lavcopts vcodec=mpeg4:aspect=16/9:vbitrate=8000000 -vf scale=1920:1080 -o timelapse.avi -mf type=jpeg:fps=24 mf://@stills_even.txt

#if you need to flip your images
mencoder -nosound -ovc lavc -lavcopts vcodec=mpeg4:aspect=16/9:vbitrate=8000000 -vf scale=1920:1080 -flip -o timelapse.avi -mf type=jpeg:fps=24 mf://@stills_even.txt

```

To see your videos we will also add them to a playlist here

[playlist link](https://www.youtube.com/playlist?list=PLimbrUa_ArHwJ9n_HL_IQsU0pAGpnxtPD)

##Now let's move your movie to a folder with your name

```

#let's make a directory (folder) with your name (no spaces)

mkdir /home/pi/yourname

#for example: mkdir /home/pi/malia

# then let's list the files to see if your folder is there

ls -l /home/pi/

# you should see a folder with your name

#now let's move your timelapse.mp4 movie there, make sure you replace the "yourname" with your actual name

mv /home/pi/images/timelapse2/timelapse.mp4 /home/pi/yourname/timelapse.mp4

#check that the file is in there

ls -l /home/pi/yourname/

```

##Introduction to Raspberry Pi Sensors

There are numerous sensors that are available for Raspberry Pi computers and also for Arduino microcontrollers.

*  Adafruit has a nice selection of sensors and tutorials [here](http://www.adafruit.com/category/35)
*  The best way to find out how to use a sensor is to google it and find online tutorials.

We will be using four different 'sensor' modules today  
1)  Light panel: Bright Pi, more information [here](https://github.com/danforthcenter/outreach/tree/master/raspi_teachers_2015/Bright%20Pi%20assembly%20instructions)  
2)  Temperature sensor: More information [here](https://www.adafruit.com/product/1893)
3)  Temperature sensor #2 : More information [here](http://www.adafruit.com/products/393)
5)  Light sensor: More information [here](https://www.adafruit.com/products/439)

How to make your Raspberry pi more 'rugged'
*  Weather proofing in a coffee can by Jim at fotosyn [here](http://www.fotosyn.com/simple-timelapse-camera-using-raspberry-pi-and-a-coffee-tin/)
*  See post on 5 different cases [here](http://www.makeuseof.com/tag/5-ways-to-ruggedise-your-raspberry-pi/)
*  This Rustoleum coating might work [here](http://www.geek.com/chips/neverwet-makes-the-raspberry-pi-and-other-gadgets-waterproof-1564340/)

##Connecting a sensor to a Google doc

**More here from Noah**

##Opensource tools for image analysis

Collecting time lapse images are great for demonstrating concepts of plant growth, plant movement, and circadian rhythms.
But you might want to actually measure plant growth and plant movement. There are several opensource tools that make these measurements easier.

*  ImageJ is [here](http://fiji.sc/Fiji)
*  OpenCV (Open Computer Vision) is a library of image processing functions for a few languages (C/C++, Java, Python) that is widely used.  
There is documentation [here](http://opencv.org/). OpenCV is a very powerful library but it is not the most user friendly.
We built PlantCV (Plant Computer Vision) to process plant images specifically, building off of OpenCV and other available Python libraries.  
*  PlantCV documentation and information is located [here](http://plantcv.danforthcenter.org/)
*  R is a programming language that is used for statistical analysis, more information [here](http://www.r-project.org/)
*  R studio is a free graphical user interface (GUI) to make running R code easier. More info [here](https://www.rstudio.com/)

**Process images with ImageJ**

[ImageJ](imagej.nih.gov/ij/) is a free image quantification software developed by the National Institutes of Health (NIH). Go [here](http://imagej.nih.gov/ij/docs/guide/index.html) for detailed instructions.

Install imageJ on your Raspberry Pi using the following commands:  

```
sudo apt-get update	
```  

```
sudo apt-get install imageJ
```
After installation, imageJ will be installed in the Menu-->Graphics tab

Open imageJ, and open a file (This can be any image, or the ImageJ/sample_image_ruler.jpg')

An example of how to measure length and angles can be found [here](https://www.youtube.com/watch?v=8IrTXUDqmXI)

To measure length:  
1. Use the line tool to draw a known length (use 1 cm in example)  
2. Select Analyze--> Measure  
3. Select Analyze--> Set Scale  
4. Set known distance to 1, unit of length to cm  
5. Draw line over stem in picture  
6. Select Analyze--> Measure  

**Process images with PlantCV**

[PlantCV](http://plantcv.danforthcenter.org/) is software we wrote at the Danforth Center to extract biologically meaningful information from images of plants. Go to [here](http://plantcv.danforthcenter.org/pages/documentation/function_docs/vis_tutorial.html) for detailed instructions.

Pick an image and look at the name to determine which script to run most scripts are in dev (see example below) type:

```
path_to_script -i path_to_image -o destination_folder_for_output_images -D
```

For example:

```python

#The first part is the script that is being run.
#The -i is the path to the image you want analyzed
#The -o tells the program where to put the output images. A . means it will put the images in whatever directory you are currently in.
#The -D option at the end tells the program you are running it in debug mode, this means that every image at every step will get printed out (there are lots of steps, so lots of images)

/home/pi/plantcv/scripts/dev/vis_sv_z2500_L2_e82.py -i /home/pi/nsf_reu_workshop/sample_images/brachypodium/VIS_SV_0_z2500_h2_g0_e82_300296\ copy.png -o . -D

```

You just processed one image, you will see a bunch of information print out to the screen, and lots of new images appear in your working directory.
If you had many images to process you would then use the "parallelization" script, which runs the 'single image script' over a bunch of images and
then saves the data to a database. We won't be doing that today but the instructions are [here](http://plantcv.danforthcenter.org/pages/documentation/function_docs/vis_tutorial.html).
If you had run a full set of data (many plants growing over a period of time) you could then use R to analyze the data.


##Introduction to Scratch

**More here from Meter**

##Tech Trunk Discussion Notes

**Moderated by Terry**

**Notes:**

##Module planning notes

**Moderated by Terry**

**Notes:**
