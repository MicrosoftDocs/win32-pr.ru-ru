---
title: Структура MPTHREAT_INFOEX_NIS (Мпклиент. h)
description: Содержит сведения, относящиеся к NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS структуры устаревшие функции среды Windows
- Функции PMPTHREAT_INFOEX_NIS указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071572"
---
# <a name="mpthreat_infoex_nis-structure"></a>\_ \_ Структура NIS мпсреат инфоекс

Содержит сведения, относящиеся к NIS.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a>Члены

<dl> <dt>

**SourceIP**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd></dd> <dt>

**дестинатионип**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd></dd> <dt>

**двсаурцепорт**
</dt> <dd>

Тип: **DWORD**

</dd> <dd></dd> <dt>

**двдестинатионпорт**
</dt> <dd>

Тип: **DWORD**

</dd> <dd></dd> <dt>

**Протокол**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd></dd> <dt>

**Ссылка**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





