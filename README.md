# fever-log
Visualize fever log at WordCamp Osaka 2018 using RasPi Sense HAT &amp; WordPress RESI API\

## Setup at WordPress Site

1. Put measure-feaver.php into wp-content/plusins, and activate the plugin. The "fever-log" custom post type will be created.
1. Create a static page and put content of graph.txt

## Setup at Raspberry Pi

1. Burn a Raspbian Lite on a micro SD card and do first setup.
1. Do `sudo pip install requests`
1. Edit api line of log-env.py as your WordPress site.
1. Put log-env.py on your home directory
1. do `crontab -e` and write a line as below: 

`* * * * * /home/pi/log-env.py`
