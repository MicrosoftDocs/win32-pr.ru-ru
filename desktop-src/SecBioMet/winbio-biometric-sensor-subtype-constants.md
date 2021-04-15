---
title: Константы WINBIO_BIOMETRIC_SENSOR_SUBTYPE (Винбио \_ types. h)
description: Укажите битовую маску для возможностей встроенного датчика.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415253"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a>\_ \_ Константы подтипа биометрического датчика винбио \_

Следующие константы можно использовать в качестве битовой маски для параметра *capabilities* структуры [**\_ \_ схемы единицы винбио**](winbio-unit-schema.md) . Они относятся к возможностям встроенного датчика.



| Константа                                                                                                                                                                                                            | Описание                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <dt>**\_неизвестный \_ ПОДТИП датчика \_ винбио**</dt> </dl>     | Неизвестные подтипы датчика.<br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <dt>**\_ \_ \_ считывание подтипа датчика винбио FP \_**</dt> </dl> | Датчик поддерживает прокрутку отпечатков пальцев.<br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <dt>**\_ \_ \_ касание подтипа датчика FP винбио \_**</dt> </dl> | Датчик поддерживает касание пальцами.<br/>     |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> <dt>

[**\_схема единицы \_ винбио**](winbio-unit-schema.md)
</dt> </dl>

 

 





