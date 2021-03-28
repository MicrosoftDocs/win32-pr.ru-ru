---
title: texm3x3vspec-PS
description: Выполняет умножение матрицы 3x3 и использует результат для выполнения поиска текстур.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987085"
---
# <a name="texm3x3vspec---ps"></a>texm3x3vspec-PS

Выполняет умножение матрицы 3x3 и использует результат для выполнения поиска текстур. Его можно использовать для отражения отражений и для сопоставления среды, если вектор-Ray не является константой. texm3x3vspec необходимо использовать в сочетании с двумя инструкциями [texm3x3pad-PS](texm3x3pad---ps.md) . Если для глаза-Ray используется константа, инструкция [texm3x3spec-PS](texm3x3spec---ps.md) выполняет ту же матрицу умножения и поиск текстур.

## <a name="syntax"></a>Синтаксис



| texm3x3vspec DST, src |
|-----------------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3vspec          | x    | x    | x    |      |      |      |       |      |       |



 

Эта инструкция выполняет последнюю строку операции умножения матрицы 3x3, интерпретирует полученный вектор в качестве обычного вектора для отражения вектора с глазами-Ray, а затем использует отраженный вектор в качестве адреса текстуры для поиска текстуры. Он работает так же, как [texm3x3spec-PS](texm3x3spec---ps.md), за исключением того, что вектор глаза-Ray взят из четвертого компонента координат текстуры. Матрица 3x3, как правило, полезна для ориентации обычного вектора на правильное пространство тангенса для отрисовки поверхности.

Матрица 3x3 состоит из координат текстуры третьего этапа текстуры и двух предшествующих стадий текстуры. Полученный вектор после отражения (УВВ) используется для выборки текстуры на этапе 3. Любая текстура, назначенная предшествующим двум стадиям текстуры, игнорируется.

Эта инструкция должна использоваться с инструкцией texm3x3pad. Регистры текстур должны использовать следующую последовательность.


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



Первая инструкция texm3x3pad выполняет первую строку умножения<sup>, чтобы найти u.</sup>

u<sup>"</sup> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n) <sub>RGB</sub>

Вторая инструкция texm3x3pad выполняет вторую строку умножения, чтобы<sup>найти v.</sup>

v<sup>'</sup> = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Инструкция texm3x3spec выполняет третью строку умножения, чтобы<sup>найти w.</sup>

w<sup>"</sup> = TextureCoordinates (этап m + 2)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Инструкция texm3x3vspec также выполняет вычисление отражения.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E

где значение обычного N задается

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

и глаз. вектор E передается

E = (TextureCoordinates (этап m)<sub>Q</sub> ,

TextureCoordinates (этап m + 1)<sub>Q</sub> ,

TextureCoordinates (этап m + 2)<sub>Q</sub> )

Наконец, примеры инструкций texm3x3vspec t (m + 2) с (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) и сохраняют результат в t (m + 2).

t (m + 2)<sub>RGBA</sub> = текстуресампле (этап m + 2)<sub>RGBA</sub> с использованием (<sup>u, v, w</sup> )<sup>в</sup> качестве координат<sup></sup>

## <a name="examples"></a>Примеры

Ниже приведен пример шейдера с идентифицированными картами текстур и идентифицированными стадиями текстуры.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



Для этого примера требуется следующая Настройка этапа текстуры.

-   Этапу 0 назначается Текстурная схема с обычными данными. Часто это называется картой выпуклости. Для каждого шаг текселя данные имеют (XYZ) нормали. Координаты текстуры на этапе n определяют способ выборки этой обычной схемы.
-   Набор координат текстуры m назначается строке 1 матрицы 3X3. Любая текстура, назначенная этапу m, игнорируется.
-   Набор координат текстуры m + 1 назначается строке 2 матрицы 3X3. Любая текстура, назначенная этапу m + 1, игнорируется.
-   Набор координат текстуры m + 2 назначается строке 3 матрицы 3X3. Этапу m + 2 назначается том или текстура текстуры Куба. Текстура предоставляет данные цвета (RGBA).
-   В инструкции четвертого компонента (q) данных координат текстуры на этапах m, m + 1 и m + 2 передается элемент «глаз» вектора E.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




