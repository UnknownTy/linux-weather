# linux-weather
Linux Weather is a very basic system service for linux devices, created in Ubuntu.
Linux Weather updates the system's MOTD hourly with the system's local weather.
This is done using data from [wttr.in](http://wttr.in/) [(Github Link)](https://github.com/chubin/wttr.in).

## Installation

Linux-weather should work with most linux systems that use systemctl.
To install follow these steps:

1. Download the linux-weather repository
2. Place the linux-weather repository in your home directory
3. Open the wthr.service file
4. Change the `ExecStart` directory to your home directory <sup>1</sup>
5. Change the `WorkingDirectory` directory to your home directory <sup>1</sup>
6. Use the `mv wthr.* /etc/systemd/system` command <sup>2</sup>
7. Use the `sudo systemctl daemon-reload` command <sup>3</sup>

The service is now installed!


<sup>1</sup>By default the service is set to `/home/vagrant`. If you are using a vagrant machine you do not need to change anything

<sup>2</sup>This moves the service and timer to the system's running directory

<sup>3</sup>This reloads the systemctl running services to to include the weather service
