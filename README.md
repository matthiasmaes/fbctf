# FBCTF [![Build Status](https://travis-ci.org/facebook/fbctf.svg)](https://travis-ci.org/facebook/fbctf)

## What is FBCTF?

The Facebook CTF is a platform to host Jeopardy and “King of the Hill” style Capture the Flag competitions.

<div align="center"><img src="screencapture.gif" /></div>

## How do I use FBCTF?

* Organize a competition. This can be done with as few as two participants, all the way up to several hundred. The participants can be physically present, active online, or a combination of the two.
* Follow setup instructions below to spin up platform infrastructure.
* Enter challenges into admin page
* Have participants register as teams
* Enjoy!

For more information, see the [Admin Guide](https://github.com/facebook/fbctf/wiki/Admin-Guide)

# Installation

The FBCTF platform was designed with flexibility in mind, allowing for different types of installations depending on the needs of the end user. The FBCTF platform can be installed either in Development Mode, or Production Mode.

[Quick Setup Guide](https://github.com/facebook/fbctf/wiki/Quick-Setup-Guide) (_Recommended Installation_)

The [Quick Setup Guide](https://github.com/facebook/fbctf/wiki/Quick-Setup-Guide) details the quick setup mode which provides a streamlined and consistent build of the platform but offers less flexibility when compared to a custom installation. If you would prefer to perform a custom installation, please see the [Development Installation Guide](https://github.com/facebook/fbctf/wiki/Installation-Guide,-Development) or [Production Installation Guide](https://github.com/facebook/fbctf/wiki/Installation-Guide,-Production).

# Quick Setup Guide - One container per machine

In order to give more flexibility and decrease the load in the machine, we decide as well split the containers and use machines smallest machines to manage one container per machine.
We create a bash script to do a fast implementation and upload the images with the parameters that we need in order to later run the containers on each machine.
1. We need to do a docker login to upload the images in our repositories.
`docker login`
2. We're going to execute the script with the requested parameters.
`./build-images.sh -c [CACHE_SERVER_IP] -m [MYSQL_SERVER_IP] -s [HHVM_SERVER_IP] -r [USER_PUBLIC_REPOSITORY]`
3. If you have some doubts about that you can type the following command.
`./build-images.sh --help`


## Reporting an Issue

First, ensure the issue was not already reported by doing a search. If you cannot find an existing issue, create a new issue. Make the title and description as clear as possible, and include a test case or screenshot to reproduce or illustrate the problem if possible.

If you have issues installing the platform, please provide the entire output of the provision script in your issue. Also include any error messages you find in `/var/log/hhvm/error.log`.

## Contribute

You’ve used it, now you want to make it better? Awesome! Pull requests are welcome! Click [here](https://github.com/facebook/fbctf/blob/master/CONTRIBUTING.md) to find out how to contribute.

Facebook also has [bug bounty program](https://www.facebook.com/whitehat/) that includes FBCTF. If you find a security vulnerability in the platform, please submit it via the process outlined on that page and do not file a public issue.

Feel free to join our slack by registering your email here: https://fbctf-slack.herokuapp.com/

## Have more questions?

Check out the [wiki pages](https://github.com/facebook/fbctf/wiki) attached to this repo. You can also ask on Slack by registering your email here: https://fbctf-slack.herokuapp.com/.

## License

This source code is licensed under the Creative Commons Attribution-NonCommercial 4.0 International license. View the license [here](https://github.com/facebook/fbctf/blob/master/LICENSE).
