---
layout: event
title: Learning to do a thing
permalink: /firstpage/
---

# Liquid and markdown and tabletop

Progress:

- tabletop js loads
- in-page script initialises
- data loads from spreadsheet
- data assigns to model
- raw data assigns to innerHTML

TODO
- explore formatting in sheets and transport integrity 
- assign js model data to Liquid variables
- make it look right
- productionise to templates and content instances
- front page
- nav

<script type='text/javascript'>    
  var publicSpreadsheetUrl = 'https://docs.google.com/spreadsheets/d/1cXHJ8DsS7kndV2xfdR48RNx1s2ySxOOH92EQIIa6-Wc/edit?usp=sharing';

  function init() {
    Tabletop.init( { key: publicSpreadsheetUrl,
                     callback: showInfo,
                     simpleSheet: true } )
  }

//  function showInfo(data, tabletop) {
//    alert('Successfully processed!')
//    console.log(data);
//  }

  function showInfo(data, tabletop)  {
    data.forEach(function(data) {
      event_title.innerHTML = data.event_title;
      // dates transferred as text: need as dates to be evaluated in front-page listing for ordering events
      event_startdate.innerHTML = data.event_startdate;
      event_enddate.innerHTML = data.event_enddate;
      event_timing.innerHTML = data.event_timing;
      Event_location.innerHTML = data.Event_location;
      event_livestreamshow.innerHTML = data.event_livestreamshow;
      event_livestream.innerHTML = data.event_livestream;
      event_summary.innerHTML = data.event_summary;
      event_prerequisites.innerHTML = data.event_prerequisites;
      event_facilitators.innerHTML = data.event_facilitators;
      event_access.innerHTML = data.event_access;
      event_language.innerHTML = data.event_language;
      event_preparation.innerHTML = data.event_preparation;
      event_agendashow.innerHTML = data.event_agendashow;
      event_agenda.innerHTML = data.event_agenda;
      event_liveresources.innerHTML = data.event_liveresources;
      event_washupshow.innerHTML = data.event_washupshow;
      event_washupshow.innerHTML = data.event_washupshow;
 });
    }

  window.addEventListener('DOMContentLoaded', init)
</script>
<p>Here's the data</p>
<h2 id="event_title"></h2>
<p><strong id="event_summary"></strong></p>
<p>This event starts on <span id="event_startdate"></span></p>
// hide end date if empty
<p id="event_enddate"></p>
<p id="event_timing"></p>
<p id="Event_location"></p>
<p>event_livestreamshow, boolean to control display of livestream link, currently assumed to be a URL <span id="event_livestreamshow"></span>: <span id="event_livestream"></span></p>
<p id="event_prerequisites"></p>
<p id="event_facilitators"></p>
<p id="event_access"></p>
<p id="event_language"></p>
<p id="event_preparation"></p>
<p id="event_agendashow"></p>
<p id="event_agenda"></p>
<p id="event_liveresources"></p>
<p id="event_washupshow"></p>
<p id="event_washup"></p>
