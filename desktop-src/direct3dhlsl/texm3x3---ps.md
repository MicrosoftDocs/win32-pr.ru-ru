---
title: texm3x3-PS
description: Выполняет умножение матрицы 3x3 при использовании в сочетании с двумя инструкциями texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983837"
---
# <a name="texm3x3---ps"></a>texm3x3-PS

Выполняет умножение матрицы 3x3 при использовании в сочетании с двумя инструкциями [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Синтаксис



| texm3x3 DST, src |
|------------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Эта инструкция аналогична инструкции [texm3x3tex-PS](texm3x3tex---ps.md) без поиска текстур.

Эта инструкция используется в качестве завершающей из трех инструкций, представляющих операцию умножения матрицы 3X3. Матрица 3x3 состоит из координат текстуры третьего этапа текстуры и двух предшествующих стадий текстуры. Любая текстура, назначенная любому из трех стадий текстуры, игнорируется.

Эта инструкция должна использоваться с двумя инструкциями texm3x3pad. Регистры текстур должны следовать следующей последовательности.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Ниже приведены более подробные сведения о том, как выполняется умножение 3X3.

Первая инструкция texm3x3pad выполняет первую строку умножения<sup>, чтобы найти u.</sup>

u<sup>"</sup> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Вторая инструкция texm3x3pad выполняет вторую строку умножения, чтобы<sup>найти v.</sup>

v<sup>'</sup> = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Инструкция texm3x3tex выполняет третью строку умножения, чтобы<sup>найти w.</sup>

w<sup>"</sup> = TextureCoordinates (этап m + 2)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Поместите результат матрицы в регистр назначения.

t (m + 2)<sub>RGBA</sub> =<sup>(u,</sup> <sup>v, w, 1</sup> )<sup></sup>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




