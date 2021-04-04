---
title: Структура MPSAMPLE_DATA (Мпклиент. h)
description: Данные уведомления передаются в функцию обратного вызова отправки образца.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA структуры устаревшие функции среды Windows
- Функции PMPSAMPLE_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137643"
---
# <a name="mpsample_data-structure"></a>\_Структура данных мпсампле

Данные уведомления передаются в функцию обратного вызова отправки образца.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**двсамплеиндекс**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Индекс образца элемента, для которого сообщается состояние отправки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





