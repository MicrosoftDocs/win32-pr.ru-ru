---
description: Категория " \_ Категория датчика" \_ содержит датчики, которые предоставляют информацию, относящуюся к механическим устройствам и измерениям.
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: SENSOR_CATEGORY_MECHANICAL (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbac9a00895b08bd99106af7f0b6986118b4645dac690fd190f734e1499940dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666714"
---
# <a name="sensor_category_mechanical"></a>\_механическая категория \_ датчика

Категория " \_ Категория датчика" \_ содержит датчики, которые предоставляют информацию, относящуюся к механическим устройствам и измерениям.

**Типы датчиков, определяемые платформой**

В эту категорию входят следующие типы датчиков, определяемые платформой.



| Тип датчика                                                                                                                                                                                                                                                                                                           | Описание                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**Датчик \_ \_Логический \_ коммутатор типа**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt> </dl>                    | Параметры с двумя состояниями (OFF или on).<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**Датчик \_ Тип \_ логического \_ \_ массива коммутатора**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt> </dl> | Массив параметров с двумя состояниями (OFF или on).<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**Датчик \_ Введите \_ Force**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt> </dl>                                                | Принудительное использование датчиков.<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**Датчик \_ \_Многозначный \_ параметр типа**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> </dl>           | Переключатели с несколькими позиционированиями.<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**Датчик \_ \_Нажим типа**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt> </dl>                                       | Датчики давления.<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**Датчик \_ \_Масштаб типа**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt> </dl>                                                | Датчики веса.<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**Датчик \_ Тип \_ напряжений**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt> </dl>                                             | Датчики напряжений.<br/>                          |



**Поля данных, определяемые платформой**

Ключи свойств, определяемые платформой для этой категории, основаны на \_ \_ \_ \_ механических \_ GUID типа данных датчика:

{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}

Эта категория включает следующие поля данных, определяемые платформой.



| Имя поля данных и идентификатор процесса                                                                                                                                                                                                                                                                                                         | Описание                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**Датчик \_ \_Нестрогое давление типа данных \_ \_ \_ Pascal**</dt> <dt> (PID = 5)</dt> </dl>          | **VT \_ R8**<br/> Абсолютное давление, в стилях Pascal.<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**Датчик \_ \_ \_ \_ \_ \_ Состояния массивов логических коммутаторов типа данных**</dt> <dt>(PID = 10)</dt> </dl> | **VT \_ UI4**<br/> Поля состояния для массива логических коммутаторов.<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**Датчик \_ \_ \_ \_ \_ Состояние логического переключения типа данных**</dt> <dt>(PID = 2)</dt> </dl>                       | **Логическое значение VT \_**<br/> Поле состояния для \_ \_ логического \_ коммутатора типа датчика.<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**Датчик \_ \_Тип данных \_ Force \_ невтонс**</dt> <dt> (PID = 4)</dt> </dl>                                            | **VT \_ R8**<br/> Force, в невтонс.<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**Датчик \_ \_Нехватка \_ датчика типов данных \_ \_ Pascal**</dt> <dt> (PID = 6)</dt> </dl>                   | **VT \_ R8**<br/> Относительная нагрузка датчика в стилях Pascal.<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**Датчик \_ \_ \_ \_ \_ Состояние многозначного коммутатора типа данных**</dt> <dt> (PID = 3)</dt> </dl>             | **VT \_ R8**<br/> Поле состояния для \_ \_ многозначного \_ коммутатора типа датчика.<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**Датчик \_ \_ \_ Ограничение типа данных**</dt> <dt> (PID = 7)</dt> </dl>                                                                  | **VT \_ R8**<br/> Нагрузку.<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**Датчик \_ \_ \_ Масса \_ килограмма типа данных**</dt> <dt> (PID = 8)</dt> </dl>                                   | **VT \_ R8**<br/> Вес, в килограммах.<br/>                             |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Заголовок<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




