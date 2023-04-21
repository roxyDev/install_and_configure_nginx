# Install and configure Nginx
Nginx (pronounced as “Engine-X”) is an open source web server that is often used as reverse proxy or HTTP cache. It is available for Linux for free. In this tutorial we’ll install Nginx and set up a basic site.

## Installing Nginx
To install Nginx, use following command:
sudo apt update
sudo apt install nginx

## Start Nginx
Starting Nginx is very simple. Just use the following command:
service nginx start
If you're using a systemd based version such as Ubuntu Linux 16.04 LTS and above, use systemctl within the command, like so:
systemctl start nginx

## Stop Nginx
Stopping Nginx will kill all system processes quickly. This will terminate Nginx even if there are open connections. In order to do so, run one of the following commands:
service nginx stop
systemctl stop nginx
Example response:
Stopping nginx Server...
This command can still, however, take some time on busy servers. Therefore, if you want Nginx to stop even faster, you can also use:
killall -9 nginx

## Restart Nginx
Restarting Nginx basically performs a stop then a start. Use one of the following commands to run an Nginx restart:
service nginx restart
systemctl restart nginx
Example response:
Stopping nginx Server... [ OK ]
Starting nginx Server... [ OK ]

## Reload Nginx
Reload is a bit different from restart in that, again, it is more gracefully. According to Nginx, reload is defined as "start the new worker process with a new configuration, gracefully shut down old worker processes.". You can reload Nginx by using one of the following commands:
service nginx reload
systemctl reload nginx
Example response:
Reloading nginx Server... [ OK ]

## View server status
Check what the current status of your Nginx web server is with one of the following commands:
service nginx status
systemctl status nginx
Example response:

## Test Nginx configuration
You can test your Nginx server's configuration file before restarting or reloading it completely. This helps prevent any unforeseen errors which can cause your website to gown down. To do this there are two separate commands you can use, both return the same information:
nginx -t


