[tutoial](https://www.pyimagesearch.com/2017/09/04/raspbian-stretch-install-opencv-3-python-on-your-raspberry-pi/)
> 
```
$ sudo raspi-config
```

```
reboot
```

```
sudo apt-get ....
```

>Q:So, given that, what’s the point of using virtualenv and virtualenvwrapper ?

A: [answer](https://realpython.com/python-virtual-environments-a-primer/)
it’s important to understand that a virtual environment is a special tool used to keep the
dependencies required by different projects in separate places by creating isolated, independent
Python environments for each of them.

## Note: I recommend running the source ~/.profile
## file each time you open up a new terminal to ensure your system variables have been setup correctly.

>mkvirtualenv cv -p python3
s command will create a new Python virtual environment named cv using

>
##Again, I can’t stress this point enough: the cv Python virtual environment is 
entirely independent and sequestered from the default Python version included in t
he download of Raspbian Stretch. Any Python packages in the global site-packages directory
will not be available to the cv virtual environment. Similarly, any Python packages installed 
in site-packages of cv will not be available to the global install of Python. Keep this in mind 
when you’re working in your Python virtual environment and it will help avoid a lot of confusion and headaches

> How to check if you’re in the “cv” virtual environment
```
$ source ~/.profile
$ workon cv
```


##Headaahe part:
> Step #5: Compile and Install OpenCV
```
$ make -j4
```
### be stuck -> wait actually it really need a long time 
### run out of application memory: restart rpi
### every time must cd to the dirc
