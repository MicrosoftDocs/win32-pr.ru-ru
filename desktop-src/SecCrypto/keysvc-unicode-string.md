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
ms.openlocfilehash: ac1e82ab481b9844e8a21940112c6014a19f111cab53db2974c488dff0982027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622334"
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
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Ркэйсвкк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ркэйпфксинсталл**](rkeypfxinstall.md)
</dt> <dt>

[**\_большой двоичный объект кэйсвк**](keysvc-blob.md)
</dt> </dl>

 

 
