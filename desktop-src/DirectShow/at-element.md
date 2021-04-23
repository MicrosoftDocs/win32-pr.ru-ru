---
description: Элемент at определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего параметр.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Элемент at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909832"
---
# <a name="at-element"></a>Элемент at

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`at`Элемент определяет значение элемента [**param**](param-element.md) в определенное время относительно начала перехода или действия, содержащего параметр. `at`Элемент приводит к резкому переходу параметра к новому значению в заданный момент времени. Для плавного продвижения нового значения используйте [**линейный**](linear-element.md) элемент.

## <a name="attributes"></a>Атрибуты

[**время**](time-attribute.md), [ **значение**](value-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



| Метка | Значение |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Дети | None                           |



 

## <a name="examples"></a>Примеры


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>См. также

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 



