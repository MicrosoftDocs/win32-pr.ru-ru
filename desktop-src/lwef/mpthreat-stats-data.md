---
title: Структура MPTHREAT_STATS_DATA (Мпклиент. h)
description: Дополнительные данные статистики угроз.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- MPTHREAT_STATS_DATA структуры устаревшие функции среды Windows
- Функции PMPTHREAT_STATS_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135794"
---
# <a name="mpthreat_stats_data-structure"></a>\_ \_ Структура данных статистики мпсреат

Дополнительные данные статистики угроз.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**двсреаткаунт**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Число угроз.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





