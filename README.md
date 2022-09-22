# custom_card_person_presence
this is a Custom Card for the awsome Home Assistant "theme" Minimal-Lovelace-UI
![191694379-b8250f5c-5036-47bc-878c-d064d7060d21](https://user-images.githubusercontent.com/66369207/191695033-b881dee4-7b07-459a-9d1b-f34146e9e0e8.png)

This Custom Card adds fuctionality to display current room

        - type: 'custom:button-card'
          template: custom_card_person_presense
          entity: <person>
          variables:
            ulm_card_person_presense_entity: <person>
            ulm_card_person_presense_use_entity_picture: true
            ulm_card_person_presense_battery: <battery sensor>
            ulm_card_person_presense_eta: <traveltime sensor>
            ulm_card_person_presense_room: <input_text.person>  #defines the Text of the room lable
            ulm_address: <geocoded sensor>
