---
title: Back up dynalist custom css code
---

This is a back up for dynalist custom css code. 

```
/* change the font to IBM Plex Sans KR and do hack for aliasing */
/* @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+KR:wght@300&display=swap');*/
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+KR&display=swap');

.Node{
font-family: 'IBM Plex Sans KR', sans-serif;
transform : rotate(0.04deg); 
}

/* Documents Settings */
/* bold title*/
.Node.is-currentRoot > .Node-self
{
font-weight: bold;
}

/* change italics to underline */
.node-italics {
  text-decoration: underline;
  font-style: normal;
}

/* enlarge images when hovering */
.node-displayed-image:hover { 
    max-width: 100%;
    max-height: 100%;  }
.node-displayed-image {
    max-width: 400px;
    max-height: 400px;
}

/* checkbox on mobile does not trigger zoom */
.is-mobile .Node-bullet {
pointer-events: none;
}

/* don't show icon for Dynalist links. */
.node-link-internal.is-displayed:before {
    content: none;
}

/* add icons to some tags */
/* Set up Material Icons */ 
@font-face { 
font-family: 'Material Icons'; 
font-style: normal; 
font-weight: 400!important; 
src: url(https://fonts.gstatic.com/s/materialicons/v38/flUhRq6tzZclQEJ-Vdg-IuiaDsNcIhQ8tQ.woff2) format('woff2'); 
} 

a[title^="Filter #CheckLater"] { 
visibility: hidden; 
position: relative; 
margin-right: -100px; 
float: left; 
} 

a[title^="Filter #CheckLater"]:after { 
font-family: 'Material Icons'; 
font-weight: normal; 
font-style: normal; 
line-height: 1; 
letter-spacing: normal; 
text-transform: none; 
display: inline-block; 
white-space: nowrap; 
word-wrap: normal; 
direction: ltr; 
text-rendering: optimizeLegibility; 
-webkit-font-smoothing: antialiased; 
visibility: visible; 
/* position: absolute; */ 
top: -5px; 
left: 0; 
content: " \e85d"; 
font-size: 22px; 
color: cornflowerblue; 
float: left; 
} 

/* change the design of color labels */
/* ----------------------------------
Specialized Color Labels For Color Tags 2(orange) and 6(purple)
----------------------------------*/
  .Node-contentContainer.has-color.mod-color-label-2:before
  {
    background: #ff8700;
  }

  .Node-contentContainer.has-color
  {
    background: none;
    position: relative;
  }

  .Node-contentContainer.has-color.mod-color-label-2:before
  {
    content: "";
    position: absolute;
    top: 2px;
    left: -6px;
    width: 6px;
    height: 20px;
    border-radius: 2px;
  }

  .Node-contentContainer.has-color.mod-color-label-6:before
  {
    content: "";
    position: absolute;
    top: 2px;
    left: -6px;
    width: 6px;
    height: 20px;
    border-radius: 2px;
  }

  .Node-contentContainer.has-color.mod-color-label-6:before
  {
    background: purple;
  }

/*----------------------------------
Specialized Color Labels For Color Tags 1(red),3(yellow),4(green),5(blue)
----------------------------------*/

  .set-color-label[data-color="1"], .Node-contentContainer.mod-color-label-1
  {
    background: #ffebeb !important;
    padding-left: 3px !important;
    border-left: solid FireBrick;
    border-radius: 0;
    max-width: 90%;
  }

  .set-color-label[data-color="3"], .Node-contentContainer.mod-color-label-3
  {
    background: #FFF9D3 !important;
    padding-left: 3px !important;
    border-left: solid #FFE84A;
    border-radius: 0;
    max-width: 90%;
  }

  .set-color-label[data-color="4"], .Node-contentContainer.mod-color-label-4
  {
    background: #C2E0C6 !important;
    padding-left: 3px !important;
    border-left: solid green;
    border-radius: 0;
    max-width: 90%;
  }
  .set-color-label[data-color="5"], .Node-contentContainer.mod-color-label-5
  {
    background: #EDF4FF !important;
    padding-left: 3px !important;
    border-left: solid #09387D;
    border-radius: 0;
    color: #09387D !important;
    max-width: 90%;
  }


/*----------------------------------
Make Color Tags 1 and 2 white on "#s|b:#333|c:white", PowerPack black background
Optional Can Delete Below
----------------------------------*/
  .Node[style^="background: rgb(51, 51, 51)"] .Node-contentContainer.has-color.mod-color-label-1,.Node[style^="background: rgb(51, 51, 51)"] .Node-contentContainer.has-color.mod-color-label-2
  {
    color: white !important;
  }

  .Node[style^="background: rgb(51, 51, 51)"] .node-inline-code:not(.hljs)
  {
    color: purple !important;
    font-weight: bold;
  }

  .Node[style^="background: rgb(51, 51, 51)"] .Node-content.node-line,.Node[style^="background: rgb(51, 51, 51)"] .Node-renderedContent.node-line,.Node[style^="background: rgb(51, 51, 51)"] .node-line.Node-contentContainer,.Node[style^="background: rgb(51, 51, 51)"] .Node-renderedNote,.Node[style^="background: rgb(51, 51, 51)"] .Node-note.needsclick
  {
    color: white !important;
  }

  .Node[style^="background: rgb(51, 51, 51)"] .Node-contentContainer.mod-color-label-6
  {
    background: purple !important;
  }

  .Node[style^="background: rgb(51, 51, 51)"] .Node-contentContainer.mod-color-label-5
  {
    background: darkblue !important;
  }

  .Node[style^="background: rgb(51, 51, 51)"] .Node-contentContainer.mod-color-label-4
  {
    background: darkgreen !important;
  }

  .Node[style^="background: rgb(51, 51, 51)"] .Node-contentContainer.mod-color-label-3
  {
    background: brown !important;
  }

  .Node[style^="background: rgb(51, 51, 51)"] .node-bold
  {
    color: plum;
  }

  .Node[style^="background: rgb(51, 51, 51)"] .node-italics
  {
    font-style: normal;
  }

/* Remove all Vertical lines except first 1 in current view */
  .Node.is-currentRoot .Node .Node > .Node-children
  {
    border-left: 0px !important;
  }

/* Hide All Bulletpoints (1st and 2nd in current view) */
  .Node.is-currentRoot .Node .Node-bullet:before
  {
    visibility: hidden;
  }
/* Displays Any Collapsed bulletpoint */
  .Node.is-currentRoot .Node .is-collapsed>.Node-bullet:before
  {
    visibility: visible;
  }

/* Override 2nd bulletpoint in current view */
  .Node.is-currentRoot .Node .Node .Node-bullet:before
  {
    content: "–";
    visibility: visible;
  }

/* Overrides 3rd Bulletpoint in current view */
  .Node.is-currentRoot .Node .Node .Node .Node-bullet:before
  {
    content: "•";
    visibility: visible;
  }

/* Overrides 4th Bulletpoint in current view */
  .Node.is-currentRoot .Node .Node .Node .Node .Node-bullet:before
  {
    content: "◦";
    visibility: visible;
  }
/* Overrides 5th Bulletpoint in current view */
  .Node.is-currentRoot .Node .Node .Node .Node .Node .Node-bullet:before
  {
    content: "■";
    visibility: visible;
  }
/* Overrides 6th Bulletpoint in current view */
  .Node.is-currentRoot .Node .Node .Node .Node .Node .Node .Node-bullet:before
  {
    content: "◻";
    visibility: visible;
  }
/* Overrides 7th Bulletpoint in current view */
  .Node.is-currentRoot .Node .Node .Node .Node .Node .Node .Node .Node-bullet:before
  {
    content: "◆";
    visibility: visible;
  }
/* Change the font size of katex */  
.katex { font-size: 1em !important; } 
```
