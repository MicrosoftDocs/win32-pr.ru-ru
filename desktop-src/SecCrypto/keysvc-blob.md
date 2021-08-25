---
description: '\_Структура больших двоичных объектов кэйсвк определяет большой двоичный объект службы Key. Эта структура используется функцией Ркэйпфксинсталл.'
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: Структура KEYSVC_BLOB (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 7e71a090558b31444c550146a2cb99f062080db9b80e7d69561ff891b93262b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992974"
---
# <a name="keysvc_blob-structure"></a>\_Структура больших двоичных объектов кэйсвк

Структура **\_ больших двоичных объектов кэйсвк** определяет большой двоичный объект службы Key. Эта структура используется функцией [**ркэйпфксинсталл**](rkeypfxinstall.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Члены

<dl> <dt>

**CB**
</dt> <dd>

Значение типа **ulong** , указывающее размер в байтах, который равен **Pb**.

</dd> <dt>

**ПБ**
</dt> <dd>

Указатель на **байт** , содержащий большой двоичный объект, в формате [*PKCS \# 12*](../secgloss/p-gly.md) .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Ркэйсвкк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ркэйпфксинсталл**](rkeypfxinstall.md)
</dt> <dt>

[**\_строка Юникода \_ кэйсвк**](keysvc-unicode-string.md)
</dt> </dl>

 

 
