---
description: Элемент at определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего параметр.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Элемент at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d67a5e3c3ca2bd47381084ad0e0090d7aa208db87f35e5efe3a7d805a73d097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824395"
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

 

 



