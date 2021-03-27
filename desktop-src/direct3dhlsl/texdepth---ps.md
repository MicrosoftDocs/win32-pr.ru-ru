---
title: тексдепс-PS
description: Вычислите значения глубины, которые будут использоваться в тесте сравнения буферов глубины для этого пикселя.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103889988"
---
# <a name="texdepth---ps"></a>тексдепс-PS

Вычислите значения глубины, которые будут использоваться в тесте сравнения буферов глубины для этого пикселя.

## <a name="syntax"></a>Синтаксис



| тексдепс DST |
|--------------|



 

где

-   DST — это регистр назначения.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| тексдепс              |      |      |      | x    |      |      |       |      |       |



 

Эта инструкция использует R5. r/R5. g в тесте сравнения буферов глубины для этого пикселя. Данные в синих и альфа-каналах игнорируются. Если R5. g = 0, результат R5. r/R5. g = 1,0.

Временная регистрация R5 — единственный регистр, который может использовать эта инструкция.

После выполнения этой инструкции временная регистрация R5 недоступна для дополнительного использования в шейдере.

При использовании множественной выборки использование этой инструкции исключает большую часть преимуществ буфера глубины более высокого разрешения. Поскольку шейдер пикселей выполняется один раз для каждого пикселя, для каждого из сравниваемых тестов глубины должно использоваться одно значение глубины, полученное [texm3x2depth-PS](texm3x2depth---ps.md) или тексдепс.

## <a name="examples"></a>Примеры

Ниже приведен пример использования тексдепс.


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




