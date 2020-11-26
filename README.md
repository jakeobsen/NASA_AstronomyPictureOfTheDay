# NASA Astronomy Picture of the Day downloader

This is my NASA APOD downloader. It gets the last picture published by
NASA on their [APOD](https://apod.nasa.gov/apod/astropix.html) site.

You can also specify a specific image to download using the `--url`
option.

## Usage

```
usage: nasapicofday [-h] [--url [URL]] [output_dir]

Download NASA Astronomy Picture of the Day

positional arguments:
  output_dir              Output dir for download script.

optional arguments:
  -h, --help              show this help message and exit
  --url [URL], -u [URL]   Custom URL to download from
```

## Automatic update

The script does some basic checking before udpating the images to ensure
you don't download the same picture twice. So you can easily put this in a
cronjob and have it run in the background.

Just run `crontab -e` and add a line like this:

`1 0 * * * * /path/to/nasapicofday ~/Pictures/APOD`

Remember to update the actual path to the location you put in
`nasapicofday`.

When you've added it to cron or run it the first time, then simply point
your desktop background manager to the latest file in the output directory
and you'll get the latest picture as your wallpaper!

## License

```
NASA Astronomy Picture of the Day downloader
Copyright (C) 2020 Morten Jakobsen

This program is free software; you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation; either version 2 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT
ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more
details.

You should have received a copy of the GNU General Public License along with
this program; if not, write to the Free Software Foundation, Inc., 51
Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.  Or use this link:
https://www.gnu.org/licenses/old-licenses/gpl-2.0.txt
```
