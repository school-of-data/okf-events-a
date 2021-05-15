---
title: Read me
---

Simple static site based on GitHub Pages made to detail and publicise Open Knowledge Foundation training events.

Details of a training event are added to a Google Sheet, which is read in real-time when a page is rendered. This means that event details can be updated by anyone at any time and should be useful, for example, for adding event details during and after an event without the need to commit/push/publish changes.

At the back end, adding a new event or series of events is accomplished by adding a file per event to the Git repo. The file contains several lines of 'front matter' identifying the event and the location of the Google Sheet which contains details of the event. Committing/pushing changes causes the site to be regenerated and republished.

## Adding an event

### 1: Add a Google Sheet and publish it

Open the Google Sheet event template at https://docs.google.com/spreadsheets/d/1joh7ZY165t5fp2DXa6F4T-z9a_cQbFeiYf3JtrLERAE/edit?usp=sharing and make a copy with the name of the event as its title.

Add information about the event following the basic guidance in the template. You can return later and complete any information that you don't have now and the webpage will be immediately updated.

Publish the Sheet through File > Publish to the web with settings 'main' and 'Comma-separated values (.csv). Copy and keep safe the URL.

### 2: Add a page to the site to hold the event data

You will need permission to commit to the GitHub repository and permission to push commits or to make a pull request for approval. Talk to Cédric Lombion (cedric.lombion@okfn.org) if you need this to be set up for you.

It helps if you have a 'local' version of the site on your computer so that you can test and preview changes that you make before committing. If you are not familiar with setting up a local version of GitHub Pages see the instructions at https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll.

Event pages are created in inside the **events folder**. Create a file with a useful name such as csv-manip-mumbai.html. 

In that file add the required 'front matter' to allow the site to organise access to your event page and complete an entry for each item, eg

```
---
layout: event
title: "[event title]"
description: "[Short description/summary of the event]"
permalink: /[where you want the page to be located or accessed]/
series: [The name of any series that this is a part of. Otherwise leave blank]
serieslink: /[The name of a file describing the series if it exists. Otherwise leave blank]/
date: [Date on which he event occurs or starts in format yyyy-mm-dd]
publicSpreadsheetUrl: [Full URL of the Google Sheet which contains the details of the event]
lang: [Language of the event description in ISO two-letter format, eg 'en', 'fr' etc.]
location: [The place where the event occurs. Can be a city, country, or just 'Zoom' etc for fully-online events]
---
```

Save the file and if you have a local site regenerate it (this is normally automatic) and test it. You should see your new event listed in date order on the front page, and clicking on the link should give you the event details.

Commit and push to live.

### 3: Removing an event from the site

It's not the intention that events should ever be removed from the site. The event listing pushes 'past events' to the bottom beneath a suitable heading, and they may contain useful lessons or outputs from the event, as well as serving as a reminder for attendees.

If you must remove event details, just delete the corresponding event file at the top level of the Git repo.

### 4: Adding a 'series' container

The front of the site lists all upcoming events. Some may be part of a programme or series where it's useful to know all the related events and if it is important to attend all of them.

You can create a series by creating a series file and linking to it from each of the events which are part of it.

Create a file inside the **series folder** of the Git repo with a useful name such as 'open-geodata-programme.html'.

Populate the file with 'front matter' and some text (you can use html or markdown for the text) which will introduce a listing of all the events linked to the series. Like this:

```
---
layout: series
title: [Title of the overall series]
description: [Short description of the series]
permalink: /series/<name-of-series>
---

**permalink** should used in the **serieslink** front matter of an event under the series.
