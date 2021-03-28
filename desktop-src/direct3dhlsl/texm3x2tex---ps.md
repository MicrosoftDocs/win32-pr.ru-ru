---
title: texm3x2tex-PS
description: Выполняет заполнение последней строки матрицы 3x2 и использует результат для поиска текстур. texm3x2tex необходимо использовать в сочетании с инструкцией texm3x2pad-PS.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996914"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex-PS

Выполняет заполнение последней строки матрицы 3x2 и использует результат для поиска текстур. texm3x2tex необходимо использовать в сочетании с инструкцией [texm3x2pad-PS](texm3x2pad---ps.md) .

## <a name="syntax"></a>Синтаксис



| texm3x2tex DST, src |
|---------------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

Инструкция используется как одна из двух инструкций, представляющих операцию умножения матрицы 3x2. Эта инструкция должна использоваться с инструкцией [texm3x2pad-PS](texm3x2pad---ps.md) .

При использовании этих двух инструкций регистры текстур должны использовать следующую последовательность.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



Ниже приведены более подробные сведения о том, как выполняется умножение 3x2.

Инструкция texm3x2pad выполняет первую строку умножения<sup>, чтобы найти u.</sup>

u<sup>"</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (этап m)<sub>УВВ</sub>

Инструкция texm3x2tex выполняет вторую строку умножения, чтобы<sup>найти v.</sup>

v<sup>'</sup> = t (n) TextureCoordinates<sub>RGB</sub> \* (этап m + 1)<sub>УВВ</sub>

Инструкция texm3x2tex выбирает текстуру на этапе (m + 1) с (u<sup>"</sup>, v<sup>"</sup>) и сохраняет результат в t (m + 1).

t (m + 1)<sub>RGB</sub> = текстуресампле (этап m + 1)<sub>RGB</sub> using (u<sup>"</sup>, v<sup>"</sup> ) в качестве координат

## <a name="examples"></a>Примеры

Ниже приведен пример шейдера с текстурными картами и идентифицированными стадиями текстуры.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



Для этого примера требуются следующие текстуры на следующих стадиях текстуры.

-   Этап 0 принимает карту с данными (x, y, z) пертурбатион.
-   Этап 1 содержит координаты текстуры. На стадии текстуры текстура не требуется.
-   Этап 2 содержит как координаты текстуры, так и набор 2D-текстур на этой стадии текстуры.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




