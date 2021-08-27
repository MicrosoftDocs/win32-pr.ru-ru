---
title: Структура MPHEALTH_DATA (Мпклиент. h)
description: Данные уведомления о работоспособности.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA структуры устаревшие функции среды Windows
- функции PMPHEALTH_DATA Windows указателя структур в устаревшей среде
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
ms.openlocfilehash: cb04224d38e639d053b8e20370e2b0db0dc15f44cc647e7205911362112e4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976004"
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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





