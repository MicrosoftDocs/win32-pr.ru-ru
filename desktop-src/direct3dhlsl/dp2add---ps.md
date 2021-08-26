---
title: dp2add-PS
description: Выполняет продукт с двухмерной точкой и скалярным добавлением.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39a7cd640de57f2f69c8ee3b46ee6be6e52cbb16f9db39ef902725241d77b9c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068364"
---
# <a name="dp2add---ps"></a>dp2add-PS

Выполняет продукт с двухмерной точкой и скалярным добавлением.

## <a name="syntax"></a>Синтаксис


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Где:

-   DST — это регистр назначения.
-   src0, src1 и src2 являются тремя исходными регистрами.
-   {x \| y \| z \| w} является обязательным параметром replicate свиззле on src2.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

Скалярное значение для Add выбирается параметром replicate свиззле on src2.

В следующем фрагменте кода показаны выполняемые операции.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




