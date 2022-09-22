# custom_card_person_presence
this is a Custom Card for the awsome Home Assistant "theme" Minimal-Lovelace-UI.
Tested with ESPresence and ESPHome

![191694379-b8250f5c-5036-47bc-878c-d064d7060d21](https://user-images.githubusercontent.com/66369207/191695033-b881dee4-7b07-459a-9d1b-f34146e9e0e8.png)

This Custom Card adds fuctionality to display current room in the Lable if the selected Person is Home

        - type: 'custom:button-card'
          template: custom_card_person_presense
          entity: <person>
          variables:
            ulm_card_person_presense_entity: <person>
            ulm_card_person_presense_use_entity_picture: true
            ulm_card_person_presense_battery: <battery sensor>
            ulm_card_person_presense_eta: <traveltime sensor>
            ulm_card_person_presense_room: <room sensor>        #defines the Text of the room lable
            ulm_address: <geocoded sensor>

Room Sensor can be defined as the BLE_sensor if you use ESPresence or a input_text witch recives text via a automation if you use ESPHome.
