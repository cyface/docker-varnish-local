Varnish Local Caching Proxy
=====================

This repo has a container setup local caching proxy to your development server. Useful for developing cache configurations.

How to use this repo
====================

First Time Only
---------------
* Install Docker for Mac https://docs.docker.com/docker-for-mac/install/

Starting Up the Server
----------------------
* Start your local python server on http://localhost.www.fool.com:8000 however you normally do
    * Edit /etc/hosts to map `localhost.www.fool.com` to localhost if you haven't already
* From the command line, in this project's directory, type `docker-compose up`
    * Or, you can click on docker-compose.yml in PyCharm, right click and choose "run"
* Browse to http://localhost.www.fool.com/ and you should see your project via https
* To stop the server, hit ctrl-c in the terminal if you started it that way, or click the Stop button in PyCharm.
    * If you are making changes to your server, you will want to do `docker-compose down` after you stop the server to ensure it gets rebuilt when you start it again.

Customization
--------------

* The Varnish config file in config/varnish/default.vcl is where you want to do any customization of how this project works.
* Unless; you want to change what ports it responds on, and those are in docker-compose.yml.