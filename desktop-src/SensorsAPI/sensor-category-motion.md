---
description: '\_ \_ Категория движения категории датчика содержит датчики, которые предоставляют информацию, относящуюся к физическому перемещению.'
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1edcb1b5f0a6d02c481774d18ee111ad4ca5e5cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662262"
---
# <a name="sensor_category_motion"></a>\_движение категории \_ датчика

\_ \_ Категория движения категории датчика содержит датчики, которые предоставляют информацию, относящуюся к физическому перемещению. Акселерометров мера ускорение датчика, включая ускорение гравитатионал. Средство обнаружения движения, такое как обнаружение человеческого движения в системе безопасности, имеет смысл переместить объекты. Изменения в гирометерс смысле в угловой скорости. Скорость измерения спидометр.

**Типы датчиков, определяемые платформой**

В эту категорию входят следующие типы датчиков, определяемые платформой.



| Тип датчика                                                                                                                                                                                                                                                                                              | Описание                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**Датчик \_ Введите \_ акселерометр \_ 1d**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4}</dt> </dl> | Акселерометров с одной осью.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**Датчик \_ Введите \_ акселерометр \_ 2D**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | Акселерометров с двумя осями.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**Датчик \_ Введите \_ акселерометр \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | Акселерометров с тремя осями.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**Датчик \_ Введите \_ гирометр \_ 1d**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | Гирометерс с одной осью.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**Датчик \_ Введите \_ гирометр \_ 2D**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | Гирометерс с двумя осями.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**Датчик \_ Введите \_ гирометр \_ 3D**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | Гирометерс с тремя осями.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**Датчик \_ Введите \_ \_ детектор движения**</dt> <dt>{5C7C1A12-30A5-43B9-A4B2-CF09EC5B7BE8}</dt> </dl>    | Средство обнаружения движения, например те, которые используются в системах безопасности.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**Датчик \_ Введите \_ спидометр**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | Датчиков движения.<br/>                                   |



**Поля данных, определяемые платформой**

Ключи свойств, определяемые платформой для этой категории, основываются на \_ \_ \_ идентификаторе GUID перемещения типа данных датчика \_ :

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

Эта категория включает следующие поля данных, определяемые платформой.



| Имя поля данных и идентификатор процесса                                                                                                                                                                                                                                                                                                                                                                               | Описание                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**Датчик \_ \_Ускорение типов \_ данных \_ X \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Ускорение оси X в *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**Датчик \_ \_Ускорение типов \_ данных \_ Y \_ G**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Ускорение оси Y в *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**Датчик \_ \_Ускорение типов \_ данных \_ Z \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Ускорение оси Z в *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**Датчик \_ Тип данных: \_ \_ угловое \_ ускорение \_ X \_ градусов \_ в \_ секунду в \_ квадрате**</dt> <dt>(PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Ускорение оси x гирометрик, в градусах в секунду в квадрате.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**Датчик \_ \_Тип данных \_ угловое \_ ускорение \_ Y \_ градусов \_ в \_ секунду в \_ квадрате**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Ускорение оси y гирометрик, в градусах в секунду в квадрате.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**Датчик \_ Тип данных: \_ \_ угловое \_ ускорение \_ Z \_ градусов \_ в \_ секунду в \_ квадрате**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Ускорение оси z гирометрик, в градусах в секунду в квадрате.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**Датчик \_ Тип данных: \_ \_ угловая \_ скорость \_ X \_ градусов \_ в \_ секунду**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Скорость оси x гирометрик в градусах в секунду.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**Датчик \_ \_Тип данных \_ угловая \_ скорость \_ Y \_ градусов \_ в \_ секунду**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Скорость оси y гирометрик в градусах в секунду.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**Датчик \_ Тип данных: \_ \_ угловая \_ скорость \_ Z \_ градусы \_ в \_ секунду**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Скорость оси z гирометрик, в градусах в секунду.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**Датчик \_ \_Тип данных \_ " \_ состояние движения**</dt> <dt>" (PID = 9)</dt> </dl>                                                                                                                      | **Логическое значение VT \_**<br/> **True** , если обнаружено перемещение; в противном случае — **значение false**.<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**Датчик \_ \_ \_ Счетчики скорости типа данных \_ \_ в \_ секунду**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> Скорость в метрах в секунду.<br/>                                    |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




