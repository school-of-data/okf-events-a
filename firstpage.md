---
layout: event
title: Learning to do a thing
series: What is Data?
permalink: /firstpage/
publicSpreadsheetURL: https://docs.google.com/spreadsheets/d/1cXHJ8DsS7kndV2xfdR48RNx1s2ySxOOH92EQIIa6-Wc/edit?usp=sharing
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
- align to MVP-spedified content fields

TODO
- make it look right
- productionise to templates and content instances
- front page
- nav


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
<p><strong>Structure: </strong><span id="event_structure"></span></p>
<h3>Prompts during the event</h3>
<p id="event_liveresources"></p>
<p><strong>Childcare: </strong><span id="event_childcare"></span></p>
<p><strong>Code of conduct: </strong><span id="event_codeofconduct"></span></p>
<p><strong>Costs: </strong><span id="event_costs"></span></p>
<p><strong>Facilitators: </strong><span id="event_facilitators"></span></p>
<p><strong>Organiser: </strong><span id="event_organiser"></span></p>
<p><strong>Outputs: </strong><span id="event_outputs"></span></p>
<p><strong>Presurvey: </strong><span id="event_presurvey"></span></p>
<p><strong>Presurvey show: </strong><span id="event_presurveyshow"></span></p>
<p><strong>Postsurvey: </strong><span id="event_postsurvey"></span></p>
<p><strong>Postsurvey show: </strong><span id="event_postsurveyshow"></span></p>
<p><strong>Series: </strong><span id="event_series"></span></p>

<h3>Script test</h3>
<p>Arabic: <span>سيتم توفير الترجمة الفورية من خلال سماعات الرأس للمندوبين الذين يحضرون شخصيًا.</span></p>
<p>Amharic: <span>በአካል ተገኝተው ለሚሳተፉ ልዑካን በአንድ ጊዜ ትርጉም በጆሮ ማዳመጫ በኩል ይሰጣል ፡፡</span></p>
<p>Japanese: <span>直接出席している代表者には、ヘッドホンを介して同時通訳が提供されます。</span></p>



