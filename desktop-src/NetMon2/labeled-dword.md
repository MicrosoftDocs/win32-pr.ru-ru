---
description: '\_Структура DWORD с меткой определяет метку, которая отображается при обнаружении определенного значения свойства DWORD.'
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Структура LABELED_DWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 10f3e0dd09b37821a00f2c10f99c0ea6d509ff388e9d7394a8b2c4958438f979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364849"
---
# <a name="labeled_dword-structure"></a>\_Структура DWORD с меткой

Структура **\_ DWORD с меткой** определяет метку, которая отображается при обнаружении определенного значения свойства DWORD.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a>Члены

<dl> <dt>

**Значение**
</dt> <dd>

Значение DWORD свойства, которое необходимо обнаружить.

</dd> <dt>

**Label**
</dt> <dd>

Текстовое описание или метка, отображаемая при обнаружении значения DWORD, указанного в элементе **value** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Элемент **лплабеледдвордтабле** структуры [Set](set.md) указывает на массив структур **набора** , определяющих один или несколько элементов **Label** в парах значений DWORD. Эти пары используются, если требуется отобразить метку вместо определенного значения DWORD, найденного в пакете протокола.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




