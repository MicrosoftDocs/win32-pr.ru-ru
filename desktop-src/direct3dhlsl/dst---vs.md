---
title: летнее время и
description: Вычисляет вектор расстояний. | летнее время и
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914344"
---
# <a name="dst---vs"></a>летнее время и

Вычисляет вектор расстояний.

## <a name="syntax"></a>Синтаксис



| конечный DST, src0, src1 |
|----------------------|



 

где

-   dest — это регистр назначения.
-   src0 является исходным регистром.
-   src1 является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| кон                    | x    | x    | x    | x     | x    | x     |



 

В следующем фрагменте кода показаны выполняемые операции.


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



Предполагается, что первый исходный операнд (src0) является вектором (пропускается, d \* d, d \* d, игнорируется), а второй исходный операнд (src1) — вектором (игнорируется, 1/d, игнорируется, 1/d). Назначение (dest) является вектором результата (1, d, d \* d, 1/d).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




