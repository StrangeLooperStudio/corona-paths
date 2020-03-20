# CoronaPaths.com

Track your path when leaving your house.  If you get diagnosed, share your paths over the last couple days to the public blockchain database.  Still healthy?  Automatically get updates if your path crossed with someone who was diagnosed.  All data is stored on your phone until you share it to the blockhain.  We collect no data.  Visit our website and search your area to see the paths shared near you.

accessible first
almost backend-less

privacy issues
- dont share the path from your home to your first destination
- don't share the path from your last destination to your home
- our app will alert you if you're trying to share paths close to your home (if you've entered your home address)
- same goes for any addresses you enter

need to invent an efficient browser based blockchain
- peerjs for p2p
- research preexising block chains with data storage, but needs to be quick and cheap
- or roll-our-own with a generic blockchain lib
- taylor it to this specific data set: shared geojson data, tightly restricted to a template
- bonus points if the proof-of-work validates the geojson against a template
- bonus points if it allows clients to only have to download/track data within certain areas
- bonus points if the system allows the sharer to update or append statuses
- peerjs has user ids but they should be separate from the bc id's
- is there such thing as a sparsely distributed blockchain?  bandwidth and data storage issues are a concern
- we will have to spin up node.js servers to serve as stable/fast blockchain nodes
- we might have to spin up fastboot servers to serve no-js/no-bandwidth users in 3rd countries
- may need some type of authenticity score, i.e. if enough people flag a path as unreasonable/invalid, its supressed

poc
- ui: track a path (full flow, show/track on map/delete)
- ui: connect to a p2p block-chain
- ui: share paths (basic wizard, with ability to update status, i.e. false alarm)
- ui: receive path updates (browse, dsiplay on map)
- ui: check path updates for intersections and notify

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Node.js](https://nodejs.org/) (with npm)
* [Ember CLI](https://ember-cli.com/)
* [Google Chrome](https://google.com/chrome/)

## Installation

* `git clone <repository-url>` this repository
* `cd corona-paths`
* `npm install`

## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).
* Visit your tests at [http://localhost:4200/tests](http://localhost:4200/tests).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Linting

* `npm run lint:hbs`
* `npm run lint:js`
* `npm run lint:js -- --fix`

### Building

* `ember build` (development)
* `ember build --environment production` (production)

### Deploying

Specify what it takes to deploy your app.

## Further Reading / Useful Links

* [ember.js](https://emberjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)
