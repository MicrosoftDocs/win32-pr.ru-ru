---
title: Амбиентаттрибутес. Слидето
description: Метод Слидето перемещает элемент управления в новое расположение. Элемент управления перемещается нелинейным способом за указанный период времени.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- амбиентаттрибутес. слидето проигрыватель Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f199a2786adbd63313c3f500d589f9f51e2b8ca2fa8120a8fdf75021041115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469914"
---
# <a name="ambientattributesslideto"></a>Амбиентаттрибутес. Слидето

Метод **слидето** перемещает элемент управления в новое расположение. Элемент управления перемещается нелинейным способом за указанный период времени.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*невкс*
</dt> <dd>

**Число** (**длинное**), определяющее новое значение **левого** атрибута элемента управления.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*неви*
</dt> <dd>

**Число** (**длинное**), указывающее новое значение для **верхнего** атрибута элемента управления.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*моветиме*
</dt> <dd>

**Число** (**длинное**), указывающее время в миллисекундах, которое требуется для перехода элемента управления в новое место.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод отличается от **MoveTo**, который создает линейное движение при перемещении элемента управления. Нелинейное движение, созданное этим методом, является скользящим движением, которое ускоряется от нуля в начале движения и замедляется до нуля в конце, что достигается плавной остановкой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Атрибуты окружения**](ambient-attributes.md)
</dt> <dt>

[**Амбиентаттрибутес. Left**](ambientattributes-left.md)
</dt> <dt>

[**Амбиентаттрибутес. moveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





