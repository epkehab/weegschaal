# weegschaal

## Use Medisana BS444 scale with ESPHome in HomeAssistant

### how to setup

    esp32_ble_tracker:
      scan_parameters:
        interval: 30000ms
        window: 1100ms
        active: false

    ble_client:
      - mac_address: "00:00:00:00:00:00"
        id: medisababs44_ble_id

    sensor:
      - platform: medisana_bs444
        ble_client_id: medisababs44_ble_id
        weight_1:
          name: "Weight User 1"
        kcal_1:
          name: "kcal User 1"
        fat_1:
          name: "Fat User 1"
        tbw_1:
          name: "Water User 1"
        muscle_1:
          name: "Muscle User 1"
        bone_1:
          name: "Bone User 1"
        bmi_1:
          name: "BMI User 1"

        weight_2:
          name: "Weight User 2"
        kcal_2:
          name: "kcal User 2"
        fat_2:
          name: "Fat User 2"
        tbw_2:
          name: "Water User 2"
        muscle_2:
          name: "Muscle User 2"
        bone_2:
          name: "Bone User 2"
        bmi_2:
          name: "BMI User 2"


up till 8 users can be specified....

## make sure time is specified

    time:
      - platform: homeassistant
        id: homeassistant_time
