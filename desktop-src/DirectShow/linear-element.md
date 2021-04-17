---
description: Линейный элемент определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего элемент param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: линейный элемент (Камерауиконтрол. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674889"
---
# <a name="linear-element"></a>линейный элемент

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Линейный элемент определяет значение элемента [**param**](param-element.md) в определенное время относительно начала перехода или действия, содержащего элемент **param** . `linear`Элемент заставляет параметр выполнить плавный переход из предыдущего значения к новому значению. Для мгновенного перехода к новому значению используйте элемент [**at**](at-element.md) .

## <a name="attributes"></a>Атрибуты

[**время**](time-attribute.md), [ **значение**](value-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



|          |                                |
|----------|--------------------------------|
| Parent   | [**байт**](param-element.md) |
| Дети | None                           |



 

## <a name="examples"></a>Примеры


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Камерауиконтрол. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 




