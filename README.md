Below is a description on how to setup a clean and simple Home Assistant dashboard card.

Before we start you'll need the following things:

-  Have [HACS]([https://example.com](https://github.com/hacs)) installed
-  Have the [trueNAS integration](https://community.home-assistant.io/t/truenas-integration/410431) for HA installed. **Note:** I had to install the latest beta version in order for me to have the integration working (v1.4b4)
-  Through HACS make sure you have the following installed as well:
    - [card-mod](https://github.com/thomasloven/lovelace-card-mod) – Allows you to apply custom CSS styles to cards in Home Assistant.
    - [stack-in-card](https://github.com/custom-cards/stack-in-card) – Lets you stack multiple cards inside a single card without extra borders/margins.
    - [multiple-entity-row](https://github.com/benct/lovelace-multiple-entity-row) – Display multiple entity values in a single row.
    - [apexcharts-card](https://github.com/RomRider/apexcharts-card) – Highly customizable charts, used here for the radial gauges.
    - [mushroom-cards](https://github.com/piitaya/lovelace-mushroom) – Modern, minimalistic cards used for entities and stats.
    - [mini-graph-card](https://github.com/kalkih/mini-graph-card) – Compact and good-looking line graphs.
    - [vertical-stack-in-card](https://github.com/ofekashery/vertical-stack-in-card) – Combine multiple cards vertically into one card without extra borders.

When evertything is installed its a good idea to refresh or restart HA and also check if all you trueNAS entities are found.

To make the dashboard nicer I used some added some template sensors in my configurations.yaml, this helps rounding values, adds °C and even creates a new sensor which shows the free capacity of your data pool in %. Here is my example:

- **Template sensors** → [`truenas_template_sensors.yaml`](truenas_template_sensors.yaml)

After reloading we can finaly setup the actual card, my example is linked below:

**Dashboard card** → [`nas_dashboard.yaml`](nas_dashboard.yaml)

