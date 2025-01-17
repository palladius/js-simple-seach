Self: https://github.com/palladius/js-simple-search/

In xmas 2024, I actually asked Gemini to build me a simple Ring, with a Geocities vibe to it.

I'm not sure if it's a good idea to share this, but I'm sharing it anyway.

## GCP pointers

* Doc:
* CB:
    * JSSS: https://console.cloud.google.com/cloud-build/triggers;region=global?project=puffin-tours
    * Ring25: https://console.cloud.google.com/cloud-build/triggers;region=global?project=puffin-tours
* Custom domains to CRun (wow! See TF):
    * https://jsss.palladius.it
    * https://ring.carlessos.org # probably should be different. Good for another CustomDomain with TF!


## About

This morning I was babysitting with my kids and asking Bard an existential question I had for years: *is there a way to build a VERY simple, rudimental client-side script*?

Well, Bard answered me with an instantly working `index.html` and `script.js`! I was amazed.

More on the Genesis in this <a href="https://medium.com/@palladiusbonton/hey-bard-write-a-responsive-javascript-search-engine-app-for-me-b2585e55385e">Medium Article</a>.

The app is currently served by cloud run here: <https://js-simple-search-bsl7ylv4hq-ew.a.run.app/>

## How I did it?

So how did I do it? I asked Bard, yes!
 <img src='https://github.com/palladius/js-simple-seach/raw/main/app/images/howididit.jpg' height='200' align='right' />

### Initial question

**Q.** I would like to build a small and responsive search engine. The DB Is small and static so I don't need anything complicated. I just want to have a frontend JavaScript where you start typing a word and it searches for all the elements matching this word in title or description. The only important thing to me is responsiveness so every time you type a letter it starts selecting just things matching it, so you want to write say "pistachio", the selection should start kicking in already with 'p', 'pi', 'pis', and so on. Can you help me write the code?

A. Sure, here's the JavaScript code for a small and responsive search engine that works with a static database:

Code copied in See `script.js`.

This code will create a simple search engine with an input field and a results list. As you type in the input field, the results list will be updated to show only the items that match the search term. The search is case-insensitive and will match the search term anywhere in the title or description of the item.

To use this code, you can save it as a JavaScript file and then include it in your HTML page. Here's an example of how to do that:

Code copied in See `index.html`.

This will create a simple search engine with a text input field and a list of search results. The results list will be updated as you type in the input field.

Sources:

* <https://github.com/elybaru/phase-1-project>

## About Bard

* This is great! So i can check this person code too!
    * * I can send the result both via email and via gdoc. Check the first answer's GDoc: <https://docs.google.com/document/d/1y75TsYpu9kr3vh0zEEoq-IpBTfmbJ77fsISVKbHsRRU/edit>

## Result

You can see how the autocompletion works, and also how you can sort by `title` vs `relevance` (score).

This is a GIF of how the result looks like:

 <img src='https://github.com/palladius/js-simple-seach/raw/main/docs/jsss-video-5x.gif' align='center' />

<!--
Video (WIP - I've never embedded a video in my life):
 <video src='docs/jsss-video.mov' width=180/>
 <video src='https://github.com/palladius/js-simple-seach/raw/main/docs/jsss-video.mov' width=180/>
-->
