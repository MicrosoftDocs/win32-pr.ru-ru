---
title: Перечисление MPCOMPONENT_ID (Мпклиент. h)
description: Возможные компоненты для диспетчера защиты от вредоносных программ.
ms.assetid: 014B400A-880B-419D-9F50-F3354CE945D9
keywords:
- MPCOMPONENT_ID перечисления устаревших Windows компонентов среды
- PMPCOMPONENT_IDные компоненты среды Windows указателя перечисления
topic_type:
- apiref
api_name:
- MPCOMPONENT_ID
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb5acb8d21f7fc947ae83d2b3e6ac9288c5aa38e13c5d4afaa2501b73a3d458
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976084"
---
# <a name="mpcomponent_id-enumeration"></a>\_Перечисление идентификаторов мпкомпонент

Возможные компоненты для диспетчера защиты от вредоносных программ.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPCOMPONENT_ID { 
  MPCOMPONENT_AS_SIGNATURE         = 0,
  MPCOMPONENT_AV_SIGNATURE         = 1,
  MPCOMPONENT_REALTIME_MONITOR     = 2,
  MPCOMPONENT_ONACCESS_PROTECTION  = 3,
  MPCOMPONENT_IOAV_PROTECTION      = 4,
  MPCOMPONENT_BEHAVIOR_MONITOR     = 5,
  MPCOMPONENT_AUTO_SCAN            = 6,
  MPCOMPONENT_AUTO_SIGUPDATE       = 7,
  MPCOMPONENT_IPC                  = 8,
  MPCOMPONENT_NIS                  = 9,
  MPCOMPONENT_ELAM                 = 10,
  MPCOMPONENT_MAXVALUE             = 10
} MPCOMPONENT_ID, *PMPCOMPONENT_ID;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**МПКОМПОНЕНТ \_ как \_ подпись**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**\_ \_ сигнатура мпкомпонент AV**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**\_монитор мпкомпонент реального времени \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**\_Защита мпкомпонент на \_ ЗАЩИЩЕНном доступе**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**\_Защита мпкомпонент защиту ioav \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**\_монитор поведения \_ мпкомпонент**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**\_Автоматическое \_ сканирование мпкомпонент**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**МПКОМПОНЕНТ \_ Auto \_ сигупдате**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**МПКОМПОНЕНТ \_ IPC**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**МПКОМПОНЕНТ \_ NIS**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**МПКОМПОНЕНТ \_ ELAM**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**МПКОМПОНЕНТ \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





