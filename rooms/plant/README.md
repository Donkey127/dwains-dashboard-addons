# Plant Add-on (rooms)
##### Created by [Jeroen Klompen](https://github.com/klumpke/)


### Installation
- Add the following repository to your HACS settings: https://github.com/thomasloven/lovelace-flower-card
- Install [Lovelace Flower Card](https://github.com/thomasloven/lovelace-flower-card), [card-tools](https://github.com/thomasloven/lovelace-card-tools) and [mini-graph-card](https://github.com/kalkih/mini-graph-card) from [HACS](https://hacs.xyz).
- In the HomeAssistant GUI, go to `Configuration` -> `Lovelace Dashboards` -> `Resources` -> `+` and add the following information.
  - URL: /hacsfiles/lovelace-flower-card/flower-card.js
  - Resource type: JavaScript Module
  - URL: /hacsfiles/lovelace-card-tools/card-tools.js
  - Resource type: JavaScript Module
  - URL: /hacsfiles/mini-graph-card/mini-graph-card-bundle.js
  - Resource type: JavaScript Module
- Follow the [Lovelace Flower Card instructions](https://github.com/thomasloven/lovelace-flower-card#instructions) to create the `data.js` file and get flower images.
- Copy the files `page.yaml` and `button.yaml` to your `<config dir>/dwains-dashboard/addons/rooms/<your room>/plant` directory.
- Configure your `rooms.yaml` file in `<config dir>/dwains-dashboard/configs` with config below.
- Restart Home Assistant.


### Usage
To use this add-on in your Dwains Dashboard, add the following to your `rooms.yaml` file:
```yaml
# Example rooms.yaml entry
  - name: Living Room
    addons:
      - name: Olive Tree
        icon: fas:leaf
        path: 'dwains-dashboard/addons/rooms/livingroom/plant/page.yaml'
        button_path: 'dwains-dashboard/addons/rooms/livingroom/plant/button.yaml'
        data:
          plants:
            - entity: plant.olijfboom
              species: olea europaea
            - entity: plant.drakenbloed
              species: dracaena marginata
```


### Screenshots
**Light theme:**<br>
![light](https://github.com/Klumpke/dwains-dashboard-addons/blob/master/rooms/plant/.github/screenshots/light.png "Light")

**Dark theme:**<br>
![dark](https://github.com/Klumpke/dwains-dashboard-addons/blob/master/rooms/plant/.github/screenshots/dark.png "Dark")


### Changelog
#### 1.1.1
- **BREAKING CHANGE**: ***The addon is now more dynamic than ever!*** You can add all plants via the `rooms.yaml` file. *Make sure you overwrite both the button.yaml and the page.yaml file when you update to the newest version of the addon*
- Add native HA translations to the button
#### 1.1.0
- **BREAKING CHANGE**: It's now possible to define your sensors in the `rooms.yaml` file so you don't have to edit the `page.yaml` file
- Tablet view
- Added history graphs
#### 1.0.0
- First release

---

If you like my work please feel free to buy me a coffee

<a href="https://www.buymeacoffee.com/klumpke" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/white_img.png" alt="Buy Me A Coffee"></a>