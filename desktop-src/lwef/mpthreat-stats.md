---
title: Структура MPTHREAT_STATS (Мпклиент. h)
description: Статистика, связанная с угрозами.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS структуры устаревшие функции среды Windows
- Функции PMPTHREAT_STATS указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891853"
---
# <a name="mpthreat_stats-structure"></a>\_Структура статистики мпсреат

Статистика, связанная с угрозами.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a>Члены

<dl> <dt>

**среаткаунт**
</dt> <dd>

Тип: **uint**

</dd> <dd>

Число обнаруженных угроз.

</dd> <dt>

**суспиЦиауссреаткаунт**
</dt> <dd>

Тип: **uint**

</dd> <dd>

Число обнаруженных угроз с мониторингом поведения.

</dd> <dt>

**Reserved**
</dt> <dd>

Тип: **uint \[ 4 \]**

</dd> <dd>

Поля, зарезервированные для будущего использования.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





