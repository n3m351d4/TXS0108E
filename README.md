# TXS0108E
ПРЕОБРАЗОВАТЕЛЬ ЛОГИЧЕСКИХ УРОВНЕЙ (8 КАНАЛОВ)

Так как электроника Ардуино работает от напряжения в 5 В, а большая часть flash-карт, сенсоров, экранов и других устройств работает от 3.3 В, возникает необходимость в их безопасном соединении. Самым простым решением является использование резисторов, но в такой схеме будут возникать задержки.

К тому же логические уровни во всех устройствах будут работать только однонаправленно, поэтому, если необходимо задать обратное направление, понадобятся лишние провода. Таких проблем можно избежать, используя преобразователь.

Восьмиканальный двунаправленный конвертер-преобразователь работает в диапазоне напряжений от 1.8 до 6 В. Выводы A1-A6 предназначены для включения устройств с 5 В логикой, а B1-B6 – с 3.3 В логикой. На питающий вход VCA следует подавать напряжение одного логического уровня, а на VCB – другое.

Единственным, но устранимым недостатком конвертера-преобразователя является некорректная работа с интерфейсом I2C: сенсор определения направления сбивается, когда в схеме присутствуют резисторы большого сопротивления. Если их невозможно убрать, то следует использовать резисторы номиналом более 50 кОм.

Направление преобразования распознаётся и выполняется автоматически. Обязательным условием является общий отрицательный вывод для всех источников питания, в том числе и раздельных. Чтобы модуль работал, необходимо припаять два коннектора, идущие в комплекте, к плате конвертера.

UPD:
datasheet:

The TXS0108E device is a directionless voltage-level translator specifically designed for translating logic voltage 
levels. The A-port accepts I/O voltages ranging from 1.2 V to 3.6 V. The B-port accepts I/O voltages from 1.65 V 
to 5.5 V. The device uses pass gate architecture with edge rate accelerators (one shots) to improve the overall 
data rate. The pull-up resistors, commonly used in open-drain applications, have been conveniently integrated so 
that an external resistor is not needed. While this device is designed for open-drain applications, the device can 
also translate push-pull CMOS logic outputs

To ensure the Hi-Z state during power-up or powerdown
periods, tie OE to GND through a pull-down
resistor. The minimum value of the resistor is
determined by the current-sourcing capability of the
driver.

Right description:
http://we.easyelectronics.ru/Shematech/soglasovanie-logicheskih-urovney-5v-i-33v-ustroystv.html
