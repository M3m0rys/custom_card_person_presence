# custom_card_person_presence
this is a Custom Card for the awsome Home Assistant "theme" Minimal-Lovelace-UI.
Tested with ESPresence and ESPHome

![191694379-b8250f5c-5036-47bc-878c-d064d7060d21](https://user-images.githubusercontent.com/66369207/191695033-b881dee4-7b07-459a-9d1b-f34146e9e0e8.png)

This Custom Card adds fuctionality to display current room in the Lable if the selected Person is Home

# Lovelace Config

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

Room Sensor can be defined as the BLE_sensor if you use ESPresence or a Template sensor if you use ESPHome.

# Template Sensor 

        template:
          - sensor:
              - name: "person_room"
                state: >-
                  {% if is_state('binary_sensor.person_room1','on') %}Room1
                  {% elif is_state('binary_sensor.person_room2','on') %}Room2
                  {% elif is_state('binary_sensor.person_room3','on') %}Room3
                  {% elif is_state('binary_sensor.person_room4','on') %}Room4
                  {% else %} Unknown
                  {% endif %}
