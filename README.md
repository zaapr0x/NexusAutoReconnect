
# Nexus Node ( WEB ) Auto Reconnect

Paste This Code In Your Browser Console
```js
function checkAndClick() {
    let offlineText = Array.from(document.querySelectorAll("p")).find(p => p.textContent.includes("CONNECT TO NEXUS")); // Check if the text "CONNECT TO NEXUS" is present on the page
    let switchButton = document.querySelector("div.relative.w-24.h-16.rounded-full.cursor-pointer"); // Select the switch button based on its class

    if (offlineText) {
        console.log("Offline detected! Turning the switch back on...");
        if (switchButton) {
            switchButton.click();
            console.log("Switch has been clicked.");
        } else {
            console.log("Switch button not found!");
        }
    }
}

// Run the check periodically every 2 seconds
setInterval(checkAndClick, 2000);
```
> If You don't know how to open browser console

  
It's So Simple, You Can Do Right Click Then Select Inspect Element Or Press `F12` Then Navigate To Console Tab


<img src="https://raw.githubusercontent.com/zaapr0x/NexusAutoReconnect/refs/heads/main/guide.webp" width=100%/>
