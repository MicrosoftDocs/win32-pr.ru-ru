---
description: Категория датчика \_ « \_ электрическая категория» содержит датчики, предоставляющие сведения о электрической системе.
ms.assetid: c4efa821-fb9f-4606-898a-5be103581f39
title: SENSOR_CATEGORY_ELECTRICAL (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3487b779cfefc78a541fcc72d1f2c5c5e7c0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662267"
---
# <a name="sensor_category_electrical"></a>Категория датчика " \_ \_ Электрический"

Категория датчика \_ « \_ электрическая категория» содержит датчики, предоставляющие сведения о электрической системе.

**Типы датчиков, определяемые платформой**

В эту категорию входят следующие типы датчиков, определяемые платформой.



| Тип датчика                                                                                                                                                                                                                                                                                              | Описание                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="SENSOR_TYPE_CAPACITANCE"></span><span id="sensor_type_capacitance"></span><dl> <dt>**Датчик \_ \_Емкость типа**</dt> <dt>{CA2FFB1C-2317-49C0-A0B4-B63CE63461A0}</dt> </dl>                 | Датчики емкостей.<br/>         |
| <span id="SENSOR_TYPE_CURRENT"></span><span id="sensor_type_current"></span><dl> <dt>**Датчик \_ Введите \_ текущий**</dt> <dt>{5ADC9FCE-15A0-4BBE-A1AD-2D38A9AE831C}</dt> </dl>                             | Электрические датчики тока.<br/>  |
| <span id="SENSOR_TYPE_ELECTRICAL_POWER"></span><span id="sensor_type_electrical_power"></span><dl> <dt>**Датчик \_ Введите \_ \_ электроэнергию**</dt> <dt>{212F10F5-14AB-4376-9A43-A7794098C2FE}</dt> </dl> | Электрические датчики электропитания.<br/>    |
| <span id="SENSOR_TYPE_FREQUENCY"></span><span id="sensor_type_frequency"></span><dl> <dt>**Датчик \_ \_Частота типов**</dt> <dt>{8CD2CBB6-73E6-4640-A709-72AE8FB60D7F}</dt> </dl>                       | Датчик электрических частот.<br/> |
| <span id="SENSOR_TYPE_INDUCTANCE"></span><span id="sensor_type_inductance"></span><dl> <dt>**Датчик \_ Введите \_ индуктанце**</dt> <dt>{DC1D933F-C435-4C7D-A2FE-607192A524D3}</dt> </dl>                    | Датчики индуктанце.<br/>          |
| <span id="SENSOR_TYPE_POTENTIOMETER"></span><span id="sensor_type_potentiometer"></span><dl> <dt>**Датчик \_ Введите \_ потентиометер**</dt> <dt>{2B3681A9-CADC-45AA-A6FF-54957C8BB440}</dt> </dl>           | Потентиометерс.<br/>              |
| <span id="SENSOR_TYPE_RESISTANCE"></span><span id="sensor_type_resistance"></span><dl> <dt>**Датчик \_ Тип \_ сопротивления**</dt> <dt>{9993D2C8-C157-4A52-A7B5-195C76037231}</dt> </dl>                    | Датчики сопротивления.<br/>          |
| <span id="SENSOR_TYPE_VOLTAGE"></span><span id="sensor_type_voltage"></span><dl> <dt>**Датчик \_ Тип \_ напряжения**</dt> <dt>{C5484637-4FB7-4953-98B8-A56D8AA1FB1E}</dt> </dl>                             | Датчики напряжения.<br/>             |



**Поля данных, определяемые платформой**

Ключи свойств, определяемые платформой для этой категории, основаны на \_ типе данных датчика \_ \_ \_ "Электрический GUID":

{BBB246D1-E242-4780-A2D3-CDED84F35842}

Эта категория включает следующие поля данных, определяемые платформой.



| Имя поля данных и идентификатор процесса                                                                                                                                                                                                                                                                                                         | Описание                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CAPACITANCE_FARAD"></span><span id="sensor_data_type_capacitance_farad"></span><dl> <dt>**Датчик \_ \_ \_ \_ Фарад**</dt> <dt>(PID = 4)</dt> — емкостность типа данных. </dl>                                | **VT \_ R8**<br/> Емкостность в фарадс.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_CURRENT_AMPS"></span><span id="sensor_data_type_current_amps"></span><dl> <dt>**Датчик \_ \_Тип данных \_ текущий \_ ампер**</dt> <dt>(PID = 3)</dt> </dl>                                                | **VT \_ R8**<br/> Current в амперес.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_FREQUENCY_HERTZ"></span><span id="sensor_data_type_electrical_frequency_hertz"></span><dl> <dt>**Датчик \_ \_Тип данных \_ Герц- \_ FREQUENCY \_ Гц**</dt> <dt>(PID = 9)</dt> </dl>     | **VT \_ R8**<br/> Электрическая частота в герцах.<br/>                               |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_PERCENT_OF_RANGE"></span><span id="sensor_data_type_electrical_percent_of_range"></span><dl> <dt>**Датчик \_ Тип данных " \_ \_ электрические" \_ процентного \_ \_ диапазона**</dt> <dt>(PID = 8)</dt> </dl> | **VT \_ R8**<br/> Потентиометер чтение в процентах от допустимого диапазона.<br/> |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_POWER_WATTS"></span><span id="sensor_data_type_electrical_power_watts"></span><dl> <dt>**Датчик \_ \_Тип данных \_ \_ Power \_ ватт**</dt> <dt> (PID = 7)</dt> </dl>                | **VT \_ R8**<br/> Электрическая мощность в ваттах.<br/>                                   |
| <span id="SENSOR_DATA_TYPE_INDUCTANCE_HENRY"></span><span id="sensor_data_type_inductance_henry"></span><dl> <dt>**Датчик \_ \_Тип данных \_ индуктанце \_ Генри**</dt> <dt>(PID = 6)</dt> </dl>                                    | **VT \_ R8**<br/> Индуктанце в хенриес.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_RESISTANCE_OHMS"></span><span id="sensor_data_type_resistance_ohms"></span><dl> <dt>**Датчик \_ \_Тип данных \_ сопротивления \_ охмс**</dt> <dt>(PID = 5)</dt> </dl>                                       | **VT \_ R8**<br/> Сопротивление в охмс.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_VOLTAGE_VOLTS"></span><span id="sensor_data_type_voltage_volts"></span><dl> <dt>**Датчик \_ \_Напряжение типа \_ данных \_ напряжений**</dt> <dt>(PID = 2)</dt> </dl>                                             | **VT \_ R8**<br/> Электрические возможности в вольтах.<br/>                               |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




