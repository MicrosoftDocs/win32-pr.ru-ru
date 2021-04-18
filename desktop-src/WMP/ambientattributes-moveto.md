---
title: Амбиентаттрибутес. moveTo
description: Метод moveTo перемещает элемент управления в новое расположение с линейной скоростью.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. moveTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694917"
---
# <a name="ambientattributesmoveto"></a>Амбиентаттрибутес. moveTo

Метод **MoveTo** перемещает элемент управления в новое расположение с линейной скоростью.

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*невлефт*
</dt> <dd>

**Число** (**длинное**), определяющее новое значение **левого** атрибута элемента управления.

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*невтоп*
</dt> <dd>

**Число** (**длинное**), указывающее новое значение для **верхнего** атрибута элемента управления.

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*Таймаут*
</dt> <dd>

**Число** (**длинное**), указывающее время в миллисекундах, которое требуется для перехода элемента управления в новое место.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод полезен для анимированных элементов вложенного **представления** (например, если пользователь щелкает табло и элементы управления просматриваются вниз).

Этот метод создает линейное движение при перемещении элемента управления. Это отличается от **слидето**, который создает нелинейное движение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Атрибуты окружения**](ambient-attributes.md)
</dt> <dt>

[**Амбиентаттрибутес. Left**](ambientattributes-left.md)
</dt> <dt>

[**Амбиентаттрибутес. Слидето**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





