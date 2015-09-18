---
layout: project
title: Pyxis
permalink: /pyxis/
category: pyxis
description: Defunct Linux Command Line Interface Client for SIRIUS/XM Radio Streaming.
thumb: pyxis.png
image: pyxis.png
---

Pyxis is a rewrite of the Sipie project that allowed Linux users to listen to SiriusXM radio streams through the command line. At the time the streams were implemented using windows specific codecs that didn't play nicely with the browsers. Sipie allowed the user to validate through the command line and would get the stream and play it through mplayer.

A change to the SiriusXM authentication caused it to break and I fixed it and created a patch, however to do this I became familliar with the code base and there were several other improvements I decided to implement. Due to the original maintainer not having the time to keep up with my flurry of changes Pyxis was born and was supported until SiriusXM changed to a flash based player that broke the authentication once more. However now that the web player was using flash functionality on Linux was supported so Pyxis support was dropped.