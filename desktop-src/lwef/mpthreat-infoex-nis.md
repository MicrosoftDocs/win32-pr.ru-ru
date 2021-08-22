---
title: Структура MPTHREAT_INFOEX_NIS (Мпклиент. h)
description: Содержит сведения, относящиеся к NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- MPTHREAT_INFOEX_NIS структуры устаревшие функции среды Windows
- функции PMPTHREAT_INFOEX_NIS Windows указателя структур в устаревшей среде
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
ms.openlocfilehash: 8320070f80000ec5c2b235a815dc075f96f82ddd3c6d56c4022b9d60759c3e44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746903"
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

**DestinationIP**
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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





