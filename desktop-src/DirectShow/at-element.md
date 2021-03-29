---
description: Элемент at определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего параметр.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Элемент at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806598"
---
# <a name="at-element"></a>Элемент at

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`at`Элемент определяет значение элемента [**param**](param-element.md) в определенное время относительно начала перехода или действия, содержащего параметр. `at`Элемент приводит к резкому переходу параметра к новому значению в заданный момент времени. Для плавного продвижения нового значения используйте [**линейный**](linear-element.md) элемент.

## <a name="attributes"></a>Атрибуты

[**время**](time-attribute.md), [ **значение**](value-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



|          |                                |
|----------|--------------------------------|
| Parent   | [**байт**](param-element.md) |
| Дети | None                           |



 

## <a name="examples"></a>Примеры


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 



