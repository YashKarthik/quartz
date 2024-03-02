Hi, my name is Yashashwin and welcome to my MIT Maker Portfolio. Today, I want to show you a project that I have been working on for the past two weeks: a Chrome extension that uses OpenAI's GPT-3 to summarize articles and help understand complex text.

==VO start==
There are three major components to this project:
1. The browser extension for users.
2. A backend for the client to query.
3. A database to temporarily store information for rate-limiting.
==VO end==

#### Backend

I started by building the backend. This would act as proxy to the OpenAI servers, allowing me to use environment variables without leaking them.

While I had experience working with ExpressJS and Flask I decided to use Netlify's serverless functions because this application does not require an always-on server, and I wanted to see how this approach differs from a traditional server.

As I tested the API, I realized that the endpoint could be easily spammed.

==VO Start==
To protect the endpoint, I implemented a rate-limiting system that using the fixed-window algorithm. The algorithm divides time into windows of 20 seconds each. For each client it uses the request timestamp to determine the window, and a counter to check if the client has exceeded the request limit. If the counter exceeds the set limit, the request is rejected.
==VO End==

#### Browser Extension

Next, I focused on building the browser extension. The extension is made up of several "pages".

==VO Start==
There is the extension page, which opens when the user clicks on the extension, it has its own HTML, CSS, and JavaScript. There is also a background script that listens for events from the extension page.

I used the background script to place a button in the right-click menu when the user selects some text. When the button is clicked, the background page grabs the selected text from the DOM using the `chrome.scripting` API and sends it to the proxy server. The response is stored in browser memory and the result is display in the extension UI.
==VO End==

In the future, I plan to use fine-tuned language models for specific tasks like explanations and even for understanding code.

While this is my latest project, I'm always building something new. Like after moving to New Delhi, a highly polluted city, I developed Breathe. A web service that alerts user of dangerous pollution levels. And I also contribute to open-source projects, like recently I've been involved in building Farcaster–a blockchain powered social media.