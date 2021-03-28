---
title: экземпляр
description: Используйте этот атрибут для экземпляра шейдера Geometry.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069365"
---
# <a name="instance"></a>экземпляр

Используйте этот атрибут для экземпляра шейдера Geometry.


```
instance(X)   
```



## <a name="remarks"></a>Примечания

X — это целочисленный индекс, указывающий количество экземпляров, которые должны быть выполнены для каждого рисуемого элемента (например, для каждого треугольника). При использовании этого атрибута используйте [SV \_ гсинстанцеид](sv-gsinstanceid.md) , чтобы указать, какой экземпляр шейдера Geometry выполняется.

Этот атрибут поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Атрибуты модели шейдеров 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




