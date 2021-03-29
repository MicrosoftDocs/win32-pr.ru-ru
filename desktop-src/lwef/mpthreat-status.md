---
title: Перечисление MPTHREAT_STATUS (Мпклиент. h)
description: Возможное состояние угрозы.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- MPTHREAT_STATUS перечисления устаревшие функции среды Windows
- PMPTHREAT_STATUS указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978a152d6f14d7b3577ece0a2e8bd5a8ba741a3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661870"
---
# <a name="mpthreat_status-enumeration"></a>\_Перечисление состояния мпсреат

Возможное состояние угрозы.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**\_ \_ Неизвестное состояние угрозы пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**\_ \_ обнаружено состояние угрозы пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**\_ \_ Очистка состояния угрозы пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**\_состояние угроз пакета управления \_ \_ помещено в карантин**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**\_состояние угрозы пакета управления \_ \_ удалено**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**\_состояние угрозы пакета управления \_ \_ разрешено**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**\_состояние угрозы пакета управления \_ \_ заблокировано**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**\_ \_ \_ сбой очистки состояния угрозы \_ пакета управления**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**\_ \_ \_ сбой карантина состояния угрозы пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**\_ \_ \_ не удалось удалить состояние угрозы пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**\_ \_ \_ не удалось разрешить состояние угрозы пакета управления \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**\_состояние угрозы пакета управления \_ \_ прервано**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**\_ \_ \_ сбой блока состояния угрозы \_ для пакета управления**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





