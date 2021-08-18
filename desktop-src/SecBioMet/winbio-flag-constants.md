---
title: Константы WINBIO_FLAG (Винбио \_ types. h)
description: Укажите конфигурацию биометрического модуля и характеристики доступа для нового сеанса.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e018b1d810e3a57b4adea1116aa9bebc7b82dd44888b2d720e018329d31acf4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910314"
---
# <a name="winbio_flag-constants"></a>\_Константы флага винбио

Следующие константы можно использовать в функции [**винбиупенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) для указания конфигурации биометрического модуля и характеристик доступа для нового сеанса.



| Константа                                                                                                                                                                                     | Описание                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**\_флаг винбио \_ по умолчанию**</dt> </dl>             | Флаг конфигурации датчика. Биометрические единицы работают так, как указано во время установки.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**\_базовый флаг \_ винбио**</dt> </dl>                   | Флаг конфигурации датчика. Биометрические единицы работают только как базовые устройства записи.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**\_Расширенный флаг \_ винбио**</dt> </dl>          | Флаг конфигурации датчика. В биометрических единицах используются внутренние возможности обработки и хранения.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**\_необработанный флаг винбио \_**</dt> </dl>                         | Требуемый флаг доступа. Клиентское приложение захватывает необработанные биометрические данные с помощью [**винбиокаптуресампле**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**\_обслуживание флагов винбио \_**</dt> </dl> | Требуемый флаг доступа. Клиент выполняет определяемые поставщиком операции управления на биометрической единице, вызывая [**винбиоконтролунитпривилежед**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





