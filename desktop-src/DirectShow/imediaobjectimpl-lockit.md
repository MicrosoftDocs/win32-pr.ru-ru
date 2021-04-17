---
description: Класс Локкит является внутренним классом, который блокирует и разблокирует DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Класс Имедиаобжектимпл:: Локкит (Дмоимпл. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675178"
---
# <a name="imediaobjectimpllockit-class"></a>Класс Имедиаобжектимпл:: Локкит

`LockIt`Класс является внутренним классом, который блокирует и разблокирует DMO.

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="p"></span><span id="P"></span>*ш*
</dt> <dd>

Указатель на производный объект.

</dd> </dl>

## <a name="remarks"></a>Комментарии

`LockIt`Конструктор БЛОКИРУЕТ DMO, а деструктор разблокирует DMO. Чтобы заблокировать объект внутри производного класса, Объявите локальную переменную типа `LockIt` . Объекты DMO блокируются, пока `LockIt` объект остается в области:


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



Методы в **имедиаобжектимпл** автоматически блокируют DMO.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дмоимпл. h</dt> </dl>                                                                     |
| Библиотека<br/> | <dl> <dt>Дмогуидс. lib; </dt> <dt>Мсдмо. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Шаблон класса Имедиаобжектимпл**](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




