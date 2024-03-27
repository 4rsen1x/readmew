## Requirements:
* Golang 21 version
* Python 3.8 version
* Matterbridge ([installation](https://github.com/42wim/matterbridge?tab=readme-ov-file#building-with-whatsapp-beta-multidevice-support))

## Setup:
* clone this repo
* ```python3 -m venv venv```
* ```source venv/bin/activate```
* ```pip install -r req.txt```
* ```matterbridge -conf matterbridge.toml (scan QR-code)```
* ```python main.py```
* edit config.env file if needed
* to add or remove bot admins - edit list of admins in src/load_config.py file

This bot allows you to manage groups and filters that help you search for the necessary information in the whatsapp.

## To add new group you have to specifiy group's id:
### Get WhatsApp group id (JID) from WhatsApp web

Open WhatsApp web and navigate to the relevant group:

![Whatsapp web](https://github.com/t0mer/matterbridge-custom-notifier/blob/main/screenshots/smart_home_group.png?raw=true)

Open Developer tools, click the inspect toll and click on one of the messages:

![Developer tools](https://github.com/t0mer/matterbridge-custom-notifier/blob/main/screenshots/jid.png?raw=true)

In the data-id you will see string that looks like that: **true_1203631xxxxxxxxx @g.us_3EB072082B43E417EA35_xxxxxxxxxxxx@c.us**.
Copy the part that start right after **true_** and ends with **@g.us**. this is the JID you will need.
