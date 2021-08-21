---
title: Перечисление MPSTATUS_FLAG (Мпклиент. h)
description: Возможные общие битовые флаги состояния продукта.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG перечисления устаревших Windows компонентов среды
- PMPSTATUS_FLAGные компоненты среды Windows указателя перечисления
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d850f0e8de9a3b0ed18a1a1353dfdef40d41bcb1ce4d17265ec245e82ba73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747038"
---
# <a name="mpstatus_flag-enumeration"></a>\_Перечисление флагов мпстатус

Возможные общие битовые флаги состояния продукта.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**\_флаг состояния точки управления \_ \_ нет**
</dt> <dd>

Флаги состояния не заданы (неинициализированное состояние).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**\_ \_ Служба флагов состояния пакета управления \_ \_ недоступна**
</dt> <dd>

Служба не запущена.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**\_флаг состояния пакета управления \_ \_ мпенгине \_ недоступен**
</dt> <dd>

Служба запущена без механизма защиты от вредоносных программ.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**\_требуется флаг состояния пакета управления для \_ \_ угрозы \_ FULLSCAN \_**
</dt> <dd>

Ожидание полной проверки из-за действия угрозы.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**\_ \_ \_ \_ требуется перезагрузка угрозы с флагом состояния пакета управления \_**
</dt> <dd>

Ожидается перезагрузка из-за действия угрозы.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**\_ \_ Пошаговое руководство по отметке состояния пакета управления — \_ \_ \_ \_ требуются действия**
</dt> <dd>

Ожидаются ручные действия из-за действия угрозы.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**флаг состояния пакета управления — \_ \_ \_ \_ \_ сигнатура AV**
</dt> <dd>

Антивирусные сигнатуры устарели.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_флаг состояния пакета управления \_ \_ из-за \_ \_ сигнатуры**
</dt> <dd>

Устарели сигнатуры антишпионского по.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**флаг состояния пакета управления — \_ \_ \_ \_ Быстрая \_ Проверка**
</dt> <dd>

Быстрая проверка не выполнялась в течение указанного периода.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**\_флаг состояния пакета управления \_ \_ из-за \_ полной \_ проверки**
</dt> <dd>

Полная проверка не выполнялась в течение указанного периода

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**\_флаг состояния пакета управления \_ \_ выполнение \_ \_ проверки системы**
</dt> <dd>

Выполняется проверка, инициированная системой.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**Установка \_ флага состояния пакета управления \_ \_ выполнение \_ очистки подпрограммы \_**
</dt> <dd>

Выполняется очистка, инициированная системой.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**\_ \_ Примеры выполнения флагов состояния пакета \_ управления \_**
</dt> <dd>

Имеются образцы, ожидающие отправки.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_ \_ режим вычисления флага состояния пакета \_ управления \_**
</dt> <dd>

Продукт работает в режиме оценки.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**флаг состояния пакета управления — \_ \_ \_ неподлинная**
</dt> <dd>

продукт работает в режиме Windows без подлинности.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**\_ \_ \_ \_ истек срок действия продукта для флага состояния пакета управления**
</dt> <dd>

Срок действия продукта истек.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**\_требуется флаг состояния пакета управления \_ \_ THREAT \_ Каллисто \_**
</dt> <dd>

Каллисто требуется автономное сканирование.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ Служба флагов состояния пакета управления \_ \_ при \_ \_ завершении работы системы**
</dt> <dd>

Служба завершает работу в процессе завершения работы системы.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ \_ критический сбой службы флагов состояния пакета управления \_**
</dt> <dd>

Критическая ошибка при исправлении угроз.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**\_ \_ \_ \_ \_ некритический сбой службы флага состояния \_ пакета управления**
</dt> <dd>

Исправление угроз не было критическим.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**\_ \_ инициализировано состояние флага состояния пакета управления \_ \_**
</dt> <dd>

Флаги состояния не заданы (правильно инициализированное состояние).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**\_ \_ \_ обновление платформы из-за флага состояния пакета \_ управления \_**
</dt> <dd>

Неактуальная версия платформы.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**\_флаг состояния пакета управления \_ \_ \_ обновление платформы \_ выполняется**
</dt> <dd>

Выполняется обновление платформы.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_ \_ платформа флага состояния пакета управления \_ \_ \_ , которая должна \_ быть \_ устаревшей**
</dt> <dd>

Платформа скоро будет устаревшей

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ \_ конец \_ \_ срока действия флага состояния пакета управления**
</dt> <dd>

Подпись или окончание срока жизни платформы находится в прошлом или ожидает.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**\_ \_ максимальный флаг состояния пакета управления \_**
</dt> <dd>

Максимальный допустимый флаг.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**\_флаг состояния пакета управления \_ \_ все**
</dt> <dd>

Максимально возможное значение.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





