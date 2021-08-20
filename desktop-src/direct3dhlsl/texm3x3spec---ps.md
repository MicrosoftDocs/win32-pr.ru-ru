---
title: texm3x3spec-PS
description: Выполняет умножение матрицы 3x3 и использует результат для выполнения поиска текстур. Это можно использовать для отражения отражений и сопоставления среды. texm3x3spec необходимо использовать в сочетании с двумя инструкциями texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b5fcef771d6d06a1691d5c5e953b76b1c445c7c8df7b2da37b8b4220bef2b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485434"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec-PS

Выполняет умножение матрицы 3x3 и использует результат для выполнения поиска текстур. Это можно использовать для отражения отражений и сопоставления среды. texm3x3spec необходимо использовать в сочетании с двумя инструкциями [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Синтаксис



| texm3x3spec DST, src0, src1 |
|-----------------------------|



 

where

-   DST — это регистр назначения.
-   src0 и src1 являются исходными регистрами.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

Эта инструкция выполняет последнюю строку матрицы 3x3, использует полученный вектор в качестве обычного вектора для отражения вектора с глазом, а затем использует отраженный вектор для выполнения поиска текстур. Шейдер считывает вектор глаза-Ray из регистра констант. Матрица 3x3, как правило, полезна для ориентации обычного вектора на правильное пространство тангенса для отрисовки поверхности.

Матрица 3x3 состоит из координат текстуры третьего этапа текстуры и двух предшествующих стадий текстуры. Полученный Вектор отражения POST (u, v, w) используется для выборки текстуры на заключительном этапе текстуры. Любая текстура, назначенная предшествующим двум стадиям текстуры, игнорируется.

Эта инструкция должна использоваться с двумя инструкциями texm3x3pad. Регистры текстур должны использовать следующую последовательность.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



Первая инструкция texm3x3pad выполняет первую строку умножения<sup>, чтобы найти u.</sup>

u<sup>"</sup> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Вторая инструкция texm3x3pad выполняет вторую строку умножения, чтобы<sup>найти v.</sup>

v<sup>'</sup> = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Инструкция texm3x3spec выполняет третью строку умножения, чтобы<sup>найти w.</sup>

w<sup>"</sup> = TextureCoordinates (этап m + 2)<sub>УВВ</sub> \* t (n)<sub>RGB</sub>

Затем инструкция texm3x3spec выполняет вычисление отражения.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E

где значение обычного N задается

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

и глаз. вектор E передается регистром констант

E = c \# (любой регистр константы — можно использовать C0, C1, C2 и т. д.).

Наконец, примеры инструкций texm3x3spec t (m + 2) с (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) и сохраняют результат в t (m + 2).

t (m + 2)<sub>RGBA</sub> = текстуресампле (этап m + 2)<sub>RGBA</sub> с использованием (<sup>u, v, w</sup> )<sup>в</sup> качестве координат<sup></sup>

## <a name="examples"></a>Примеры

Ниже приведен пример шейдера с текстурными картами и идентифицированными стадиями текстуры.


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



Для этого примера требуется следующая Настройка этапа текстуры.

-   Этапу 0 назначается Текстурная схема с обычными данными. Часто это называется картой выпуклости. Для каждого шаг текселя данные имеют (XYZ) нормали. Координаты текстуры на этапе n определяют, где следует выделать образец этой обычной схемы.
-   Набор координат текстуры m назначается строке 1 матрицы 3X3. Любая текстура, назначенная этапу m, игнорируется.
-   Набор координат текстуры m + 1 назначается строке 2 матрицы 3X3. Любая текстура, назначенная этапу m + 1, игнорируется.
-   Набор координат текстуры m + 2 назначается строке 3 матрицы 3X3. Этапу m + 2 назначается том или текстура текстуры Куба. Текстура предоставляет данные цвета (RGBA).
-   Глаз. вектор E имеет постоянный регистр E = c \# .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




