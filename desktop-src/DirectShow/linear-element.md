---
description: Линейный элемент определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего элемент param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: линейный элемент (Камерауиконтрол. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910092"
---
# <a name="linear-element"></a>линейный элемент

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Линейный элемент определяет значение элемента [**param**](param-element.md) в определенное время относительно начала перехода или действия, содержащего элемент **param** . `linear`Элемент заставляет параметр выполнить плавный переход из предыдущего значения к новому значению. Для мгновенного перехода к новому значению используйте элемент [**at**](at-element.md) .

## <a name="attributes"></a>Атрибуты

[**время**](time-attribute.md), [ **значение**](value-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



| Метка | Значение |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Дети | None                           |



 

## <a name="examples"></a>Примеры


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Камерауиконтрол. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 




