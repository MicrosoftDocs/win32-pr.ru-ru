---
description: Структура PF \_ фолловентри определяет протокол, который сетевой монитор добавляется в следующий набор средства синтаксического анализа.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Структура PF_FOLLOWENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8fd7452a4db6318df0d4c23ea405d2cd4afcf6575c7abac34749a66bc88c2084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063734"
---
# <a name="pf_followentry-structure"></a>\_Структура PF фолловентри

Структура **PF \_ фолловентри** определяет протокол, который сетевой монитор добавляется в следующий набор средства синтаксического анализа.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a>Члены

<dl> <dt>

**сзпротокол**
</dt> <dd>

Имя протокола.

</dd> </dl>

## <a name="remarks"></a>Remarks

В [структуре \_ следов PF](pf-followset.md) используется массив структур **PF \_ фолловентри** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[\_следующий PF](pf-followset.md)
</dt> </dl>

 

 




