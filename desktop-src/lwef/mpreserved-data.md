---
title: Структура MPRESERVED_DATA (Мпклиент. h)
description: Зарезервированные данные уведомления.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA структуры устаревшие функции среды Windows
- функции PMPRESERVED_DATA Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faabacdcfb581f9b4fc7e9d9a42464dd61e152ca533865acfb7231a711f02317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747658"
---
# <a name="mpreserved_data-structure"></a>\_Структура данных мпресервед

Зарезервированные данные уведомления.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбресерведдата**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Размер зарезервированных данных в байтах.

</dd> <dt>

**пбресерведдата**
</dt> <dd>

Тип: **Byte \***

</dd> <dd>

Указатель на зарезервированные данные.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





