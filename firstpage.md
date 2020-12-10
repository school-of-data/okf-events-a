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
- explore formatting in sheets and transport integrity 
- assign js model data to Liquid variables (can't: Liquid processing precedes JS execution. Is possible to add extra processing step, import sheet data to static JSON file in GitHub backend and process on page via Liquid operations, but adds complexity to no great obvious benefit).

TODO
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

  function showInfo(data, tabletop) {
    alert('Successfully processed!')
    console.log(data);
  }

  function showInfo(data, tabletop)  {
    data.forEach(function(data) {
      // dates transferred as text: need as dates to be evaluated in front-page listing for ordering events
      event_access.innerHTML = data.event_access;
      event_agenda.innerHTML = data.event_agenda;
      event_agendashow.innerHTML = data.event_agendashow;
      event_background.innerHTML = data.event_background;
      event_childcare.innerHTML = data.event_childcare;
      event_codeofconduct.innerHTML = data.event_codeofconduct;
      event_costs.innerHTML = data.event_costs;
      event_enddate.innerHTML = data.event_enddate;
      event_facilitators.innerHTML = data.event_facilitators;
      event_language.innerHTML = data.event_language;
      event_liveresources.innerHTML = data.event_liveresources;
      event_livestream.innerHTML = data.event_livestream;
      event_livestreamshow.innerHTML = data.event_livestreamshow;
      event_location.innerHTML = data.event_location;
      event_organiser.innerHTML = data.event_organiser;
      event_outputs.innerHTML = data.event_outputs;
      event_preparation.innerHTML = data.event_preparation;
      event_prerequisites.innerHTML = data.event_prerequisites;
      event_presurvey.innerHTML = data.event_presurvey;
      event_presurveyshow.innerHTML = data.presurveyshow;
      event_postsurvey.innerHTML = data.event_postsurvey;
      event_postsurveyshow.innerHTML = data.event_postsurveyshow;
      event_series.innerHTML = data.event_series;
      event_startdate.innerHTML = data.event_startdate;
      event_structure.innerHTML = data.event_structure;
      event_summary.innerHTML = data.event_summary;
      event_timing.innerHTML = data.event_timing;
      event_title.innerHTML = data.event_title;
      if (data.event_washupshow = "TRUE") {
          event_washup.innerHTML = data.event_washup;
          } else {
          document.getElementById("retro").style.display = "none";
          }     
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
<div id="event_background"></div>
<div id="retro">
<h3>Event retro</h3>
<p id="event_washup"></p>
</div>
<p id="event_timing"></p>
<p id="event_location"></p>
<p>event_livestreamshow, boolean to control display of livestream link, currently assumed to be a URL, and in this case the 'embed' code copied from YouTube and pasted to the spreadsheet cell, so an iframe. <span id="event_livestreamshow"></span>: <br/>
<span id="event_livestream"></span></p>
<h3>Prerequisites</h3>
<p id="event_prerequisites"></p>
<h3>Facilitators</h3>
<p id="event_facilitators"></p>
<h3>Access</h3>
<p id="event_access"></p>
<p id="event_language"></p>
<h3>Preparation</h3>
<p>To prepare for this event you should review these materials:</p>
<p id="event_preparation"></p>
<h3>Agenda</h3>
<p id="event_agendashow"></p>
<p id="event_agenda"></p>
<h3>Prompts during the event</h3>
<p id="event_liveresources"></p>
<p><strong>Childcare</strong><span id="event_childcare"></span></p>

