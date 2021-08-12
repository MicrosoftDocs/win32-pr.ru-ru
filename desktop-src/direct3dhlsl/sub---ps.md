---
title: Подсистема PS
description: Вычитает источники. | Подсистема PS
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc4faa24f95824a77e9a1e92b9a15479d2e509212c52c9309c38fcc42cf6b3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285722"
---
# <a name="sub---ps"></a>Подсистема PS

Вычитает источники.

## <a name="syntax"></a>Синтаксис



| дополнительный DST, src0, src1 |
|---------------------|



 

where

-   DST — это регистр назначения.
-   src0 является исходным регистром.
-   src1 является исходным регистром.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| sub                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Эта инструкция выполняет вычитание, показанное в этой формуле.


```
dest = src0 - src1
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




