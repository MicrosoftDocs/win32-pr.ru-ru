---
title: Структура MPRESERVED_DATA (Мпклиент. h)
description: Зарезервированные данные уведомления.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA структуры устаревшие функции среды Windows
- Функции PMPRESERVED_DATA указателя структур в устаревшей среде Windows
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
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136478"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





