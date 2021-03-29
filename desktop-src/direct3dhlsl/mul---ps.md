---
title: mul-PS
description: Умножает источники на место назначения. | mul-PS
ms.assetid: 03823c10-9631-4468-8488-4bd17224d16c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fefe89d4fdbe5f75965f2707a5ceb2c1673e1326
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998231"
---
# <a name="mul---ps"></a>mul-PS

Умножает источники на место назначения.

## <a name="syntax"></a>Синтаксис



| mul DST, src0, src1 |
|---------------------|



 

где

-   DST — это регистр назначения.
-   src0 является исходным регистром.
-   src1 является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| mul                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

В следующем фрагменте кода показаны выполняемые операции.


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




