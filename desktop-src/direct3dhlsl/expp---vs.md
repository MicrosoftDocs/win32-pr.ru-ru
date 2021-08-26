---
title: експп — VS
description: Обеспечивает частичную точность 2 экспоненциального представления.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8717edc045f50cc572d675dbec405b01fda49503349e9716210dfcae23fb277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982454"
---
# <a name="expp---vs"></a>експп — VS

Предоставляет экспоненциальное 2<sup>x</sup>частичной точности.

## <a name="syntax"></a>Синтаксис



| експп DST, src. x|&|гармошкой|Белая |
|----------------------------|



 

Где:

-   DST — это регистр назначения.
-   src является исходным регистром. Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.
-   {x \| y \| z \| w} — это обязательная репликация свиззле для исходного регистра.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| експп                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>VS \_ 1 \_ 1

Инструкция [exp-VS](exp---vs.md) работает по-разному в зависимости от версий шейдера вершин.

В VS \_ 1 \_ 1 Инструкция експп дает следующие результаты.


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



В VS \_ 2 \_ 0 и выше инструкция експп дает следующие результаты.


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>VS \_ 2 \_ 0

В VS \_ 2 \_ 0 и выше инструкция работает следующим образом:


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



Инструкция предоставляет не менее 10 разрядов точности.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




