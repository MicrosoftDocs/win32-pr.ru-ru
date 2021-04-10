---
description: '\_Перечисление типа кэйсвк определяет, применяется ли ключ к компьютеру или службе.'
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: Перечисление KEYSVC_TYPE (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999664"
---
# <a name="keysvc_type-enumeration"></a>\_Перечисление типов кэйсвк

Перечисление **\_ типа кэйсвк** определяет, применяется ли ключ к компьютеру или службе.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**кэйсвкмачине**
</dt> <dd>

Ключ для компьютера.

</dd> <dt>

<span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**кэйсвксервице**
</dt> <dd>

Ключ для службы.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ркэйсвкк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ркэйопенкэйсервице**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




