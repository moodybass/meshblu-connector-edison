## Steps

1. Set up Edison with latest image, wifi, and ssh
2. Shell into edison
3. Run "npm install -g meshblu-util"
4. git clone this repo to /node_app_slot
5. npm i
6. npm run generate:schema
7. meshblu-util register -o -t device:edison > meshblu.json
8. meshblu-util update -f schemas.json
9. meshblu-util claim
10. npm start 
