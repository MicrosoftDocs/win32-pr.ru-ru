---
description: Структура с МЕТКОЙ \_ ларжеинт определяет метку, которая отображается при обнаружении определенного значения свойства ларжеинт.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Структура LABELED_LARGEINT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fab2942a2a5188527c57663af0c6000aa2cb628eaa2499eef054854df9187784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778774"
---
# <a name="labeled_largeint-structure"></a>\_Структура ЛАРЖЕИНТ с меткой

Структура с **меткой \_ ларжеинт** определяет метку, которая отображается при обнаружении определенного значения свойства ларжеинт.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Значение**
</dt> <dd>

ЛАРЖЕИНТ значение свойства, которое необходимо обнаружить.

</dd> <dt>

**Label**
</dt> <dd>

Текстовое описание или метка, отображаемая при обнаружении значения ЛАРЖЕИНТ, указанного в элементе **value** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Элемент **лплабеледларжеинттабле** структуры [Set](set.md) указывает на массив структур **набора** , определяющих один или несколько элементов **Label** в парах значений ларжеинт. Эти пары используются, если требуется отобразить метку вместо определенного значения ЛАРЖЕИНТ, которое находится в пакете протокола.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




