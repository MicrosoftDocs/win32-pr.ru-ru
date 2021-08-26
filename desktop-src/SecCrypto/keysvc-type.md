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
ms.openlocfilehash: 3c23cc259029cf76fcb1590e6261623827d59b48c9a0728e21c8250ca3e858f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976099"
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
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Ркэйсвкк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ркэйопенкэйсервице**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




