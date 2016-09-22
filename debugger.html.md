# debugger.html

<https://github.com/devtools-html/debugger.html/>

## How I install on Windows with Firefox Developer Edition
1. `git clone https://github.com/devtools-html/debugger.html.git`
2. `cd debugger.html`
3. `npm install`
4. Start Firefox Developer Edition
5. (_one time only_) Open <about:config> and change these settings then restart Firefox Developer Edition
  * `devtools.debugger.remote-enabled` to `true`
  * `devtools.chrome.enabled` to `true`
  * `devtools.debugger.prompt-connection` to `false`
6. Press `shift+F2` and type `listen`
7. Debugger at <http://localhost:8000>
