---
title: Перечисление MPTHREAT_ACTION (Мпклиент. h)
description: Возможные действия по угрозе.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION перечисления устаревших Windows компонентов среды
- PMPTHREAT_ACTIONные компоненты среды Windows указателя перечисления
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a3cd46583b9736ad8304c16e3b12d4f0157edcdb319fd0923a0fe737d504415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247268"
---
# <a name="mpthreat_action-enumeration"></a>\_Перечисление действий мпсреат

Возможные действия по угрозе.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**\_действие управления угрозами \_ \_ неизвестно**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**\_ \_ Очистка действия угрозы пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**\_ \_ Карантин действий пакета \_ управления**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**\_ \_ действие удаления угроз \_ пакета управления**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**\_действие для \_ действия \_ угроз пакета управления**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**\_ \_ пользователяопределенные действия для пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**действие при действии угрозы пакета управления — \_ \_ \_ действие**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**\_ \_ блок действий угроз для пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**\_ \_ \_ Максимальное \_ значение действия угрозы пакета управления**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





