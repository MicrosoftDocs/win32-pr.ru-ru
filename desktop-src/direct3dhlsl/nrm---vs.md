---
title: НРМ — VS
description: Нормализация трехмерного вектора. | НРМ — VS
ms.assetid: 735e9971-c0c3-4648-8362-58bda6fac46a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e696277136826294392149c4b7430e4c75f9d9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273520"
---
# <a name="nrm---vs"></a>НРМ — VS

Нормализация трехмерного вектора.

## <a name="syntax"></a>Синтаксис



| НРМ DST, src |
|--------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| нрм                    |      | x    | x    | x     | x    | x     |



 

Эта инструкция работает по принципу, как показано здесь.

Скуарерутофсесум = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



Регистры dest и src не могут совпадать. Регистр приемника должен быть временным регистром.

Эта инструкция выполняет линейную интерполяцию на основе следующей формулы.


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




