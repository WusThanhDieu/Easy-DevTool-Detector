## Code JavaScript "FuckOFF-DevTool" easy block Developer Tool

- [interval] This configuration sets how often the tool will check for DevTools activity. The value 200 means it checks every 200 milliseconds. A lower interval will increase responsiveness but may put more load on the system.

- [redirectURL] This is the URL to which the page will be redirected if DevTools is detected. If the script detects DevTools being open (via the defined checking method), it will redirect the user to this URL. You can customize it based on your needs.
  
- [debug] This option enables debug mode. When enabled, it allows logging of detailed information in the browser’s console. This helps to debug the tool’s behavior during development or troubleshooting.
  
- [preventDevTools] This option enables blocking of DevTools-related shortcuts (e.g., F12, Ctrl+U, etc.). When set to true, it prevents users from opening DevTools through common keyboard shortcuts or right-click menus.
  
- [checkBrowser] When this option is enabled (set to true), the script will check if the browser is supported. It only supports Chrome, Safari, and Cốc Cốc browsers. If the user is using any other browser (e.g., Cyberfox or other outdated browsers), the tool will show a message that the browser is not supported and might replace the body content with a "BROWSER NOT SUPPORTED" message.
  
- [enableDebugger] This enables the use of the debugger tool. If set to true, the script will use the debugger statement to detect if DevTools is open. If the debugger is open, the page will often slow down, and this can be used as an indicator of DevTools activity.
  
- [checkShortcuts] This enables the checking and blocking of DevTools-related keyboard shortcuts (like F12, Ctrl+U, etc.). If enabled, pressing these keys will not trigger their default behavior, such as opening the developer tools or viewing the source code. It aims to prevent users from easily accessing developer tools.

```javascript
// Initialize the FuckDevtool class
const Config = new FuckDevtool({
    interval: 200, // int (Interval in milliseconds to check for DevTools activity)
    redirectURL: '//example.com', // url (Custom redirect URL if DevTools is detected)
    debug: true, // boolean (true|false, Enable or disable debug mode)
    preventDevTools: true, // boolean (true|false, Enable or disable blocking of DevTools shortcuts)
    checkBrowser: true, // boolean (true|false, Enable or disable browser check)
    enableDebugger: true, // boolean (true|false, Enable or disable the debugger for DevTools detection)
    checkShortcuts: true // boolean (true|false, Enable or disable checking and blocking DevTools-related shortcuts)
});
// Call Config (Initialize)
Config.init();
```
