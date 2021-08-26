---
title: Структура MPSTATUS_DATAEX_UNUSED (Мпклиент. h)
description: Фиктивная структура для не-SRP.
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- MPSTATUS_DATAEX_UNUSED структуры устаревшие функции среды Windows
- функции PMPSTATUS_DATAEX_UNUSED Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245315d12b5fbe76ec2f552e510336aa3974753678e04f87c33546737f180c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961094"
---
# <a name="mpstatus_dataex_unused-structure"></a>МПСТАТУС \_ датаекс \_ неиспользуемая структура

Фиктивная структура для не-SRP.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a>Члены

<dl> <dt>

**двноне**
</dt> <dd>

Тип: **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





