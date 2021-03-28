---
title: макстессфактор
description: Указывает максимальное значение, которое будет возвращаться шейдером поверхности для любого фактора тесселяции.
ms.assetid: 2c12ed56-cd64-4143-8dda-6998aa212356
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ab17bd40c24c19b4b929f2e8307ccc6bb9b56
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890027"
---
# <a name="maxtessfactor"></a>макстессфактор

Указывает максимальное значение, которое будет возвращаться шейдером поверхности для любого фактора тесселяции.


```
maxtessfactor(X)   
```



## <a name="remarks"></a>Примечания

Этот атрибут помещает верхнюю границу объема запрошенной тесселяции, чтобы помочь драйверу определить максимальный объем ресурсов, необходимых для тесселяции.

Этот атрибут поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Атрибуты модели шейдеров 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




