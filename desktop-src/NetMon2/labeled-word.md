---
description: Структура слова с МЕТКАми \_ определяет метку, которая отображается при обнаружении определенного значения свойства Word.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Структура LABELED_WORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674085"
---
# <a name="labeled_word-structure"></a>Структура слова с МЕТКАми \_

Структура **\_ слова с метками** определяет метку, которая отображается при обнаружении определенного значения свойства Word.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a>Члены

<dl> <dt>

**Значение**
</dt> <dd>

Значение слова для свойства, которое необходимо обнаружить.

</dd> <dt>

**Label**
</dt> <dd>

Текстовое описание или метка, отображаемая при обнаружении значения слова, указанного в элементе **value** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Элемент **лплабеледвордтабле** структуры [Set](set.md) указывает на массив наборов структур, определяющих одну или несколько пар значений меток. Эти пары используются, если требуется отобразить метку вместо определенного значения слова, которое найдено в пакете протокола.

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

 

 




