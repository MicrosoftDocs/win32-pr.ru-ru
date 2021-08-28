---
description: Элемент TRANSITION определяет объект перехода. Переход — это преобразование с двумя входными данными, которое приводит к переходу из одного потока (например, составного или отслеживающего) в другой.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Элемент TRANSITION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725c5c6282a35f027cad87fd0b8693dbf4885ce7d4c1d5948abc2caa9014301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951483"
---
# <a name="transition-element"></a>Элемент TRANSITION

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`transition`Элемент определяет объект перехода. Переход — это преобразование с двумя входными данными, которое приводит к переходу из одного потока (например, составного или отслеживающего) в другой.

## <a name="attributes"></a>Атрибуты

[**CLSID**](clsid-attribute.md), [**кутпоинт**](cutpoint-attribute.md), [**кутсонли**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**выкл**](mute-attribute.md)., [**Start**](start-attribute.md), [**останавливаться**](stop-attribute.md), [**свапинпутс**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



| Метка | Значение |
|----------|------------------------------------------------------------------------|
| Parent   | [**составной**](composite-element.md), [ **Track**](track-element.md) |
| Дети | [**param**](param-element.md)                                         |



 

## <a name="remarks"></a>Remarks

Атрибут **CLSID** задает подобъект, который создает переход.

## <a name="examples"></a>Примеры


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 



