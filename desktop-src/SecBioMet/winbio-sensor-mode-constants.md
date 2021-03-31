---
title: Константы WINBIO_SENSOR_MODE (Винбио \_ types. h)
description: Задайте режим адаптера датчика.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803904"
---
# <a name="winbio_sensor_mode-constants"></a>\_ \_ Константы режима датчика винбио

Следующие значения используются в функции [**сенсорадаптерсетмоде**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) для установки режима адаптера датчика.



| Константа                                                                                                                                                                                                        | Описание                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**\_неизвестный \_ \_ режим датчика винбио**</dt> </dl>          | Неизвестный режим работы.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**\_ \_ базовый режим датчика \_ винбио**</dt> </dl>                | Использовать датчик в базовом режиме. Датчик действует только как устройство записи. Любые существующие возможности обработки или хранения не используются.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**\_ \_ Расширенный режим датчика \_ винбио**</dt> </dl>       | Использовать датчик в расширенном режиме. Датчик может собирать образцы и выполнять функции сопоставления и хранения.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**\_ \_ режим навигации датчика \_ винбио**</dt> </dl> | Использовать датчик в качестве панели мыши. Сейчас такая возможность не поддерживается.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**\_ \_ режим сна датчика \_ винбио**</dt> </dl>                | Работа датчика в спящем режиме.<br/>                                                                                                                   |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





