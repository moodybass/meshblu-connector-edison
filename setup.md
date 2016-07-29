## Steps

This might change in the coming days, but this should get you started.

Still working on a good way to auto-boot this.

1. Set up Edison with latest image, wifi, and ssh
2. Shell into your edison
3. Run "npm install -g meshblu-util"
4. "git clone https://github.com/sqrtofsaturn/meshblu-connector-edison"
5. "cd meshblu-connector-edison" then "npm install"
6. meshblu-util register -o -t device:edison > meshblu.json
7. meshblu-util update -f schemas.json
8. Goto https://app.octoblu.com/profile and copy your account UUID
9. meshblu-util update -d '{"owner": "YOUR-UUID-FROM-PREVIOUS-STEP"}'
10. npm start
11. Goto https://app.octoblu.com/things/my
12. Find the newly created device named "DEVICE:EDISON" - It will look like an EDISON
13. Configure your board with some components and click Save.
14. Go to the "Flows" page and create a new flow.
15. From the sidebar drag your Edison from the Things tab into the designer area.
16. When the node is selected you'll see options for crafting a message on the Inspector
17. For each available action, components you added from the device detail page will show up in a drop down.
18. Attach a debug to the right output of the node, if you added any sensors, they'll output to this when you deploy the flow.

Note: When configuring a sensor on an analog pin, be sure to enter it as the format "A0", if you use 0 it will try to use digital pin 0.
