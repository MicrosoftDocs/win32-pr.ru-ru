---
title: Структура MPTHREAT_INFOEX_UNUSED (Мпклиент. h)
description: Фиктивная структура для угроз типа изменения без поведения.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- MPTHREAT_INFOEX_UNUSED структуры устаревшие функции среды Windows
- функции PMPTHREAT_INFOEX_UNUSED Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8def13a6f6aff010b9854055abd4636d19f77ef1f0e9867ec5e4d7562baff4f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601104"
---
# <a name="mpthreat_infoex_unused-structure"></a>МПСРЕАТ \_ инфоекс \_ неиспользуемая структура

Фиктивная структура для угроз типа изменения без поведения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
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



 

 





