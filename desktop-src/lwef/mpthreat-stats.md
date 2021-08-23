---
title: Структура MPTHREAT_STATS (Мпклиент. h)
description: Статистика, связанная с угрозами.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS структуры устаревшие функции среды Windows
- функции PMPTHREAT_STATS Windows указателя структур в устаревшей среде
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
ms.openlocfilehash: 7671b45dc09c8aca494ad270aa69fc386ef3d7c03d5144fdc3e89b4f657bb07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975944"
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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





