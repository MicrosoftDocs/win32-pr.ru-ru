---
description: '\_Структура SYSTEMTIME с меткой не определяет метку, которая отображается при обнаружении определенного значения свойства SYSTEMTIME.'
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Структура LABELED_SYSTEMTIME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913444"
---
# <a name="labeled_systemtime-structure"></a>\_Структура SYSTEMTIME с меткой

Структура **\_ SYSTEMTIME с меткой** не определяет метку, которая отображается при обнаружении определенного значения свойства SYSTEMTIME.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a>Члены

<dl> <dt>

**Значение**
</dt> <dd>

Значение SYSTEMTIME для свойства, которое необходимо обнаружить.

</dd> <dt>

**Label**
</dt> <dd>

Текстовое описание или метка, отображаемая при обнаружении значения SYSTEMTIME, указанного в элементе **value** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Элемент **лплабеледсистемтиметабле** структуры [Set](set.md) указывает на массив структур **набора** , определяющих одну или несколько пар значений меток. Эти пары используются, если требуется отобразить метку вместо определенного значения ЛАРЖЕИНТ, найденного в пакете протокола.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




