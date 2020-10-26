# NASA Astronomy Picture of the Day

This is a simple downloader for the
[NASA APOD website](https://apod.nasa.gov/)

You must install the `requests` plugin from pip to use this script:

`pip3 install --user requests`

Then you can simply run:

`python3 main.py ~/Pictures/NASA/`

And the script will download the latest picture to `~/Pictures/NASA/`
where it will create a structure based on the current year and month. And
then the script will symlink the last image to `~/Pictures/NASA/latest`
for your convenience.

If you want the image to auto update, simple point your wallpaper manager
to the `latest` file and setup the script to run on a scheduled base.

You can also download older images by running:

`python3 main.py ~/Pictures/NASA/ --url https://apod.nasa.gov/apod/ap201026.html`

At this poin the script will attempt to download that page, figure out the
data and then download the file accordingly.

Please enjoy these awesome anstronomy pictures!

... oh and btw! some of the files are missing and sometimes NASA puts up
videos. That is generally annoying. However the script should be able to
handle those situations. If not then I will most likely fix the script :)
