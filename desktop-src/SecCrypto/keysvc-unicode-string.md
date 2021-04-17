---
description: '\_ \_ Структура строки Юникода кэйсвк определяет строку в Юникоде и максимальную длину строки. Эта структура используется функцией Ркэйпфксинсталл.'
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: Структура KEYSVC_UNICODE_STRING (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684578"
---
# <a name="keysvc_unicode_string-structure"></a>КЭЙСВК \_ \_ строковая структура Юникода

Структура **\_ \_ строки Юникода кэйсвк** определяет строку в [*Юникоде*](../secgloss/u-gly.md) и максимальную длину строки. Эта структура используется функцией [**ркэйпфксинсталл**](rkeypfxinstall.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a>Члены

<dl> <dt>

**Длина**
</dt> <dd>

Значение **UShort** , указывающее длину в байтах, используемую для **buffer**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Значение **UShort** , указывающее максимальную длину в байтах, допустимую для **buffer**.

</dd> <dt>

**Буфер**
</dt> <dd>

Указатель на **UShort** , представляющий строку в Юникоде.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ркэйсвкк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ркэйпфксинсталл**](rkeypfxinstall.md)
</dt> <dt>

[**\_большой двоичный объект кэйсвк**](keysvc-blob.md)
</dt> </dl>

 

 
