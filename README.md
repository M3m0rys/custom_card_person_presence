# custom_card_person_presence
this is a Custom Card for the awsome Home Assistant "theme" Minimal-Lovelace-UI

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
