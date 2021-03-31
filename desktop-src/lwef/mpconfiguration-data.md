---
title: Структура MPCONFIGURATION_DATA (Мпклиент. h)
description: Содержит данные об изменениях конфигурации, включая старые и новые значения.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA структуры устаревшие функции среды Windows
- Функции PMPCONFIGURATION_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071475"
---
# <a name="mpconfiguration_data-structure"></a>\_Структура данных мпконфигуратион

Содержит данные об изменениях конфигурации, включая старые и новые значения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**ConfigurationName**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Имя измененной конфигурации.

</dd> <dt>

**DataType**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Тип используемых данных.

</dd> <dt>

**превиаусдатасизе**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Размер предыдущих данных в байтах.

</dd> <dt>

**ппревиаусдата**
</dt> <dd>

Тип: **Byte \** _

</dd> <dd>

Указатель на предыдущие данные.

</dd> <dt>

_ *Куррентдатасизе**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Размер новых данных в байтах.

</dd> <dt>

**пкуррентдата**
</dt> <dd>

Тип: **Byte \***

</dd> <dd>

Указатель на новые данные.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





