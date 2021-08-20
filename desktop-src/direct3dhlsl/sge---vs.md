---
title: СЖЕ — VS
description: Выдает знак, если первый источник больше или равен второму источнику.
ms.assetid: 88e8eb68-8189-40c3-b20e-f395576f5f6a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1478a6e53889ed9b1aed725653f18791af7e6eda1fd4c888f87e0e938d850cff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671764"
---
# <a name="sge---vs"></a>СЖЕ — VS

Выдает знак, если первый источник больше или равен второму источнику.

## <a name="syntax"></a>Синтаксис



| СЖЕ DST, src0, src1 |
|---------------------|



 

where

-   DST — это регистр назначения.
-   src0 является исходным регистром.
-   src1 является исходным регистром.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| сже                    | x    | x    | x    | x     | x    | x     |



 

В следующем фрагменте кода показаны выполняемые операции.


```
 
dest.x = (src0.x >= src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y >= src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z >= src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w >= src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




