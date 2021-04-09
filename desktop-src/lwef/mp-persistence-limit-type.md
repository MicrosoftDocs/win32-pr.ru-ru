---
title: Перечисление MP_PERSISTENCE_LIMIT_TYPE (Мпклиент. h)
description: Тип ограничения сохраняемости.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE перечисления устаревшие функции среды Windows
- PMP_PERSISTENCE_LIMIT_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071936"
---
# <a name="mp_persistence_limit_type-enumeration"></a>\_ \_ Перечисление типов пределов СОХРАНЯЕМости MP \_

Тип ограничения сохраняемости.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**\_неизвестная сохраняемость пакета управления \_**
</dt> <dd>

Неизвестно.

</dd> <dt>

<span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**\_Сохранение пакета управления \_ без \_ ограничения**
</dt> <dd>

Без ограничений.

</dd> <dt>

<span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**\_Длительность сохраняемости пакета управления \_**
</dt> <dd>

Длительность.

</dd> <dt>

<span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**\_версия VDM сохраняемости пакета управления \_ \_**
</dt> <dd>

Версия VDM.

</dd> <dt>

<span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**\_отметка времени сохраняемости MP \_**
</dt> <dd>

Отметка времени.

</dd> <dt>

<span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**\_Принудительное сохранение пакета управления \_**
</dt> <dd>

Обязательна.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





