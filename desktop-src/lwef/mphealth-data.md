---
title: Структура MPHEALTH_DATA (Мпклиент. h)
description: Данные уведомления о работоспособности.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA структуры устаревшие функции среды Windows
- Функции PMPHEALTH_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701089"
---
# <a name="mphealth_data-structure"></a>\_Структура данных мфеалс

Данные уведомления о работоспособности.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**двнотификатионтипе**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Тип уведомления.

</dd> <dt>

**двнотификатионфлаг**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





