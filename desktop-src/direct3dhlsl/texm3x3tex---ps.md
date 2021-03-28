---
title: texm3x3tex-PS
description: Выполняет умножение матрицы 3x3 и использует результат для поиска текстур. texm3x3tex должен использоваться с двумя инструкциями texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412251"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex-PS

Выполняет умножение матрицы 3x3 и использует результат для поиска текстур. texm3x3tex должен использоваться с двумя инструкциями [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Синтаксис



| texm3x3tex DST, src |
|---------------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Эта инструкция используется в качестве завершающей из трех инструкций, представляющих операцию умножения матрицы 3x3, за которой следует Поиск текстуры. Матрица 3x3 состоит из координат текстуры третьего этапа текстуры и двух предшествующих стадий текстуры. Полученный вектор с тремя компонентами (u, v, w) используется для выборки текстуры на этапе 3. Любая текстура, назначенная предшествующим двум стадиям текстуры, игнорируется. Матрица 3x3, как правило, полезна для ориентации обычного вектора на правильное пространство тангенса для отрисовки поверхности.

Эта инструкция должна использоваться с инструкцией texm3x3pad. Регистры текстур должны использовать следующую последовательность.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



Ниже приведены более подробные сведения о том, как выполняется умножение 3X3.

Первая инструкция texm3x3pad выполняет первую строку умножения<sup>, чтобы найти u.</sup>

u<sup>"</sup> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Вторая инструкция texm3x3pad выполняет вторую строку умножения, чтобы<sup>найти v.</sup>

v<sup>'</sup> = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Инструкция texm3x3spec выполняет третью строку умножения, чтобы<sup>найти w.</sup>

w<sup>"</sup> = TextureCoordinates (этап m + 2)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Наконец, примеры инструкций texm3x3tex t (m + 2) с (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) и сохраняют результат в t (m + 2).

t (m + 2)<sub>RGBA</sub> = текстуресампле (этап m + 2)<sub>RGBA</sub> с использованием (<sup>u, v, w</sup> )<sup>в</sup> качестве координат.<sup></sup>

## <a name="examples"></a>Примеры

Ниже приведен пример шейдера с идентифицированными картами текстур и идентифицированными стадиями текстуры.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



Для этого примера требуется следующая Настройка этапа текстуры.

-   Этапу 0 назначается Текстурная схема с обычными данными. Часто это называется картой выпуклости. Для каждого шаг текселя данные имеют (XYZ) нормали. Набор координат текстуры 0 определяет способ выборки этой обычной схемы.
-   Набор координат текстуры 1 назначается строке 1 матрицы 3X3. Любая текстура, назначенная этапу 1, игнорируется.
-   Набор координат текстуры 2 назначается строке 2 матрицы 3X3. Любая текстура, назначенная этапу 2, игнорируется.
-   Набор координат текстуры 3 назначается строке 3 матрицы 3X3. Для уточняющего запроса преобразованного трехмерного вектора необходимо задать для параметра "этап 3" значение "уровень" или "текстура Куба".

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




