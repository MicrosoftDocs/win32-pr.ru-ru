---
description: Структура диапазона определяет диапазон допустимых значений свойств.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Структура диапазона (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662895"
---
# <a name="range-structure"></a>Структура диапазона

Структура **диапазона** определяет диапазон допустимых значений свойств.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Члены

<dl> <dt>

**MinValue**
</dt> <dd>

Наименьшее возможное значение в диапазоне.

</dd> <dt>

**MaxValue**
</dt> <dd>

Наибольшее возможное значение в диапазоне.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Структура **диапазона** используется для указания допустимого диапазона чисел для свойства протокола. Если элементу **квалификатора** класса **PropertyInfo** задано значение **prop \_ куал \_ Range**, то элемент **лпранже** структуры [PropertyInfo](propertyinfo.md) должен предоставить указатель на структуру **диапазона** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




