---
title: Структура MPSAMPLE_DATA (Мпклиент. h)
description: Данные уведомления передаются в функцию обратного вызова отправки образца.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA структуры устаревшие функции среды Windows
- функции PMPSAMPLE_DATA Windows указателя структур в устаревшей среде
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
ms.openlocfilehash: aafafd2ff7162dcb50bd5e2ea92cd56ab9f073332238dc0742845f9c48c5a588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747417"
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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





