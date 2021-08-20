---
title: аутпуттопологи
description: Определяет тип выходного примитива для тесселяции.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d718b11c23fcf77f452e224a51439f7d6f422d3c81d5238167cbf87c7c3014a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725418"
---
# <a name="outputtopology"></a>аутпуттопологи

Определяет тип выходного примитива для тесселяции.


```
outputtopology(X)      
```



## <a name="remarks"></a>Remarks

X должен быть " [**точка**](dx-graphics-hlsl-geometry-shader.md)", " **линия**", " **треугольник \_**" или "треугольник" и должен быть заключен в кавычки. **\_** Ниже приведены допустимые параметры для этого атрибута.


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Этот атрибут поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Атрибуты модели шейдеров 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




