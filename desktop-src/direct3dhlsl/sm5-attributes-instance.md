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
ms.openlocfilehash: 77c19b26107228bb04007d1c2c69ac34b464c7c361966ac9858d9bcdb09b4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986164"
---
# <a name="instance"></a>экземпляр

Используйте этот атрибут для экземпляра шейдера Geometry.


```
instance(X)   
```



## <a name="remarks"></a>Remarks

X — это целочисленный индекс, указывающий количество экземпляров, которые должны быть выполнены для каждого рисуемого элемента (например, для каждого треугольника). При использовании этого атрибута используйте [SV \_ гсинстанцеид](sv-gsinstanceid.md) , чтобы указать, какой экземпляр шейдера Geometry выполняется.

Этот атрибут поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Атрибуты модели шейдеров 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




