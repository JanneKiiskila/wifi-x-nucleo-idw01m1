# Prototype Driver for STM Wi-Fi Expansion Boards based on the SPWFxx Module for STM32 Nucleo #

Currently supported boards:
 * [X-NUCLEO-IDW01M1](http://www.st.com/content/st_com/en/products/ecosystems/stm32-open-development-environment/stm32-nucleo-expansion-boards/stm32-ode-connect-hw/x-nucleo-idw01m1.html), by setting `mbed` configuration variable `idw0xx1.expansion-board` to value `IDW01M1`
 * [X-NUCLEO-IDW04A1](http://www.st.com/content/st_com/en/products/ecosystems/stm32-open-development-environment/stm32-nucleo-expansion-boards/stm32-ode-connect-hw/x-nucleo-idw04a1.html), by setting `mbed` configuration variable `idw0xx1.expansion-board` to value `IDW04A1`. You might also need to define macro `IDW04A1_WIFI_HW_BUG_WA`.

## Configuration examples

### IDW01M1

Add this section to your `mbed_app.json` in `target-overrides` -section.

``` json
        "idw0x11": {
            "expansion.board": "IDW01M1"
        }
```

`IDW01M1` is the default value in the [mbed_lib.json](https://github.com/JanneKiiskila/wifi-x-nucleo-idw01m1/blob/master/mbed_lib.json), so this is not mandatory for `IDW01M1`.


### IDW04A1

Add this section to your `mbed_app.json` in `target-overrides` -section.

``` json
        "idw0x11": {
            "expansion.board": "IDW04A1"
        }
```

### Adding the HW-workaround for IDW04A1

You can add the HW workaround acivation macro the `macros` section in your `mbed_app.json`.

``` json
   "macros": [...,"IDW04A1_WIFI_HW_BUG_WA"],
```
