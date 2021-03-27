---
title: ЛРП-PS
description: Выполняет линейную интерполяцию между вторым и третьим регистрами источника по пропорциям, заданным в первом регистре источника. | ЛРП-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081824"
---
# <a name="lrp---ps"></a>ЛРП-PS

Выполняет линейную интерполяцию между вторым и третьим регистрами источника по пропорциям, заданным в первом регистре источника.

## <a name="syntax"></a>Синтаксис



| ЛРП DST, src0, src1, src2 |
|---------------------------|



 

где

-   DST — это регистр назначения.
-   src0 является исходным регистром.
-   src1 является исходным регистром.
-   src2 является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| лрп                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Эта инструкция выполняет линейную интерполяцию на основе следующей формулы.


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




