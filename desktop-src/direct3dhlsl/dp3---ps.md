---
title: DP3-PS
description: Выполняет вычисление 3-компонентного произведения исходных регистров. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986364"
---
# <a name="dp3---ps"></a>DP3-PS

Выполняет вычисление 3-компонентного произведения исходных регистров.

## <a name="syntax"></a>Синтаксис



| DP3 DST, src0, src1 |
|---------------------|



 

где

-   DST — это регистр назначения.
-   src0 является исходным регистром.
-   src1 является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

В следующем фрагменте кода показаны выполняемые операции.


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Эта инструкция выполняется в векторном конвейере и всегда записывается в цветовые каналы. Для версии 1 \_ 4 Эта инструкция по-прежнему использует Векторный конвейер, но может выполнять запись в любой канал.

Инструкция с конечной точкой Register. RGB (. XYZ) может быть выпущена совместно с DP3, как показано ниже.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



Инструкцию DP3 можно изменить с помощью модификатора входного аргумента " [Регистрация регистра](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) " ( \_ bx2), применяемого к входным аргументам, если они еще не развернуты в динамическом диапазоне со знаком. Для шейдера освещения часто используется модификатор инструкции «насыщенность» ( \_ Кот) для фиксации отрицательных значений до черного, как показано в следующем примере.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




