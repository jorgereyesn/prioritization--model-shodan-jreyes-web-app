# Getting Started

To define the input data, it is necessary to carry out a previous research in Shodan through its official website (https://www.shodan.io/), where the following search string must be entered: org: "Organization\_Name". Once the different IPs that are visible in Shodan have been collected, we enter them into the prototype to perform the necessary queries and map the information to be displayed in the modules.

## Input Data

In the project directory, you can search /src/Pages/MainPage/main-page.component.js and and set the IPs previously found in const [ips]

## Creating environment variables

Create `.env` file and put the variable `REACT_APP_SHODAN_API_KEY=YOUR API KEY` 

Execute `npm install`

Execute `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

## Prototype Operation

Three modules are presented

The Vulnerability Overview Dashboard Module shows general information related to the network and the detected vulnerabilities, this process is achieved by applying the algorithm extractVulns as it is responsible for extracting vulnerability and network information to be analyzed and mapped into fields. The objective of this module is to provide a global vision of the resulting data. 

After knowing the general information about the set of vulnerabilities detected, it is important to have detailed information on how they were detected, i.e. the vulnerabilities for each IP. The Detailed Vulnerability Banners by IP Module contains in detail the information related to each scanned IP and the vulnerabilities that have been identified in it, in addition the links of the vulnerabilities are referenced towards NVD for a more detailed investigation, the IP plus the ports are concatenated for a review of the content hosted in each port and a link is generated according to the detected hostname, also for investigative purposes. 

Finally, the Prioritization Table Module contains every vulnerability and the corresponding calculated prioritization variables, this is achieved with Algorithm risk-factor plus some simple calculations to get the values of the environment variables. They have been ordered from highest to lowest (i.e., according to the risk factor evaluated) to suggest the user's order of review. In addition is possible download data in cvss format.

## Utility commands

`npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

`npm build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.
