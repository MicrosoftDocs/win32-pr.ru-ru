---
description: '\_Структура байтов с меткой Определяет битовую пару с меткой. Метка БИТОВой пары с метками отображается при обнаружении определенного значения свойства Byte.'
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Структура LABELED_BYTE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 05aa29942768c0c40816eafce112f12a95cd0a713bebe612d2e5ad32776a33a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494984"
---
# <a name="labeled_byte-structure"></a>\_Структура БАЙТОВ с меткой

Структура **\_ байтов с МЕТКОЙ** Определяет битовую пару с меткой. **Метка** битовой пары с метками отображается при обнаружении определенного значения свойства Byte.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a>Члены

<dl> <dt>

**Значение**
</dt> <dd>

БАЙТОВое значение свойства, которое необходимо обнаружить.

</dd> <dt>

**Label**
</dt> <dd>

Текстовое описание или метка, отображаемая при обнаружении значения, указанного в элементе **value** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Элемент **лплабеледбитетабле** структуры [Set](set.md) указывает на массив структур **набора** , определяющих один или несколько элементов **Label** в парах «байтовые значения». Эти пары используются, если требуется отобразить метку вместо определенного БАЙТового значения, найденного в пакете протокола.

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

 

 




