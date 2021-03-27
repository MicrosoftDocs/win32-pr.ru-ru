---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Объявите образец построителя текстуры.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069381"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>дкл \_ самплертипе (SM2, SM3-PS ASM)

Объявите образец построителя текстуры.

## <a name="syntax"></a>Синтаксис



|                      |
|----------------------|
| дкл \_ самплертипе s\# |



 

где:

-   \_Самплертипе определяет тип данных образца. Определяет, сколько координат требуется для каждой координаты текстуры при выборки. Определены следующие измерения координат текстуры.
    -   \_двухмерном
    -   \_Куба
    -   \_тома
-   s \# определяет образец, где s — это аббревиатура для образца, а \# — номер образца. Пробы являются псевдо-регистром, так как вы не можете напрямую считывать их или записывать.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| дкл \_ самплертипе      |      |      |      |      | x    | x    | x     | x    | x     |



 

Все \_ инструкции самплертипе дкл должны располагаться перед первой исполняемой инструкцией.

## <a name="example"></a>Например, .


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




