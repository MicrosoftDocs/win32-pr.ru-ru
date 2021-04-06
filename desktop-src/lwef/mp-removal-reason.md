---
title: Перечисление MP_REMOVAL_REASON (Мпклиент. h)
description: Причина удаления подписи Фастпас.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- MP_REMOVAL_REASON перечисления устаревшие функции среды Windows
- PMP_REMOVAL_REASON указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803539"
---
# <a name="mp_removal_reason-enumeration"></a>\_Перечисление причин удаления пакета управления \_

Причина удаления подписи Фастпас.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**Удаление пакета управления \_ \_ неизвестно**
</dt> <dd>

Неизвестно.

</dd> <dt>

<span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**\_руководство по удалению пакета управления \_**
</dt> <dd>

Вручную.

</dd> <dt>

<span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**\_Автоматическое удаление пакета управления \_**
</dt> <dd>

Автоматический.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





