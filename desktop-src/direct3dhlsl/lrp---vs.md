---
title: ЛРП — VS
description: Выполняет линейную интерполяцию между вторым и третьим регистрами источника по пропорциям, заданным в первом регистре источника. | ЛРП — VS
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d154f78b3e8ae5d3b7b8e553435d962ad3dbea9fe86f8dd772bf165c5eb542be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119188"
---
# <a name="lrp---vs"></a>ЛРП — VS

Выполняет линейную интерполяцию между вторым и третьим регистрами источника по пропорциям, заданным в первом регистре источника.

## <a name="syntax"></a>Синтаксис



| ЛРП DST, src0, src1, src2 |
|---------------------------|



 

where

-   DST — это регистр назначения.
-   src0 является исходным регистром.
-   src1 является исходным регистром.
-   src2 является исходным регистром.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| лрп                    |      | x    | x    | x     | x    | x     |



 

Эта инструкция выполняет линейную интерполяцию на основе следующей формулы.


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




