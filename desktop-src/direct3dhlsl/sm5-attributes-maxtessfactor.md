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
ms.openlocfilehash: b2cb3e946e152d6f79329be01961f6865ccc26f12e3485e05d952b8e39e41a8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023484"
---
# <a name="maxtessfactor"></a>макстессфактор

Указывает максимальное значение, которое будет возвращаться шейдером поверхности для любого фактора тесселяции.


```
maxtessfactor(X)   
```



## <a name="remarks"></a>Remarks

Этот атрибут помещает верхнюю границу объема запрошенной тесселяции, чтобы помочь драйверу определить максимальный объем ресурсов, необходимых для тесселяции.

Этот атрибут поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Атрибуты модели шейдеров 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




