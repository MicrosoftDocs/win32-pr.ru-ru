---
title: тексбемл-PS
description: Применение имитации предельного преобразования схемы окружения с коррекцией светимости. Это достигается путем изменения данных адреса текстуры в регистре назначения с использованием данных адреса пертурбатион (du, DV), матрицы среды 2D-выпуклости и освещенности.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c549e93829c3165d4921342d4e74a8dc15bc1518f7c88aa205f8afc889fae95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788068"
---
# <a name="texbeml---ps"></a>тексбемл-PS

Применение имитации предельного преобразования схемы окружения с коррекцией светимости. Это достигается путем изменения данных адреса текстуры в регистре назначения с использованием данных адреса пертурбатион (du, DV), матрицы среды 2D-выпуклости и освещенности.

## <a name="syntax"></a>Синтаксис



| тексбемл DST, src |
|------------------|



 

where

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| тексбемл               | x    | x    | x    |      |      |      |       |      |       |



 

Красный и зеленый цветовые данные в регистре src интерпретируется как данные пертурбатион (du, DV). Синий цвет данных в регистре src интерпретируется как данные светимости.

Эта инструкция преобразует красные и зеленые компоненты в исходном регистре с помощью матрицы сопоставления среды 2D-выпуклости. Результат добавляется в набор координат текстуры, соответствующий номеру регистра назначения. Корректировка светимости применяется с использованием значений светимости и этапа текстуры смещения. Результат используется для выборки текущей стадии текстуры.

Это можно использовать для различных методов, основанных на пертурбатионах адресов, таких как имитация сопоставления среды на пиксель.

Эта операция всегда интерпретирует du и DV как количество со знаком. Для версий 1 \_ 0 и 1 \_ 1 в входном аргументе не разрешается использовать модификатор input для [масштабирования со знаком "Source Register](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) " ( \_ bx2).

Эта инструкция формирует определенные результаты, когда текстуры ввода содержат данные в смешанном формате. Дополнительные сведения о форматах поверхностей см. в разделе [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



В этом примере показаны вычисления, выполненные в рамках инструкции.


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



u "= TextureCoordinates (этап m)<sub>u</sub> +

D3DTSS \_ BUMPENVMAT00 (этап m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT10 (этап m) \* t (n)<sub>G</sub>

v ' = TextureCoordinates (этап m)<sub>v</sub> +

D3DTSS \_ BUMPENVMAT01 (этап m) \* t (n)<sub>R</sub> +

D3DTSS \_ BUMPENVMAT11 (этап m) \* t (n)<sub>G</sub>

t (m)<sub>RGBA</sub> = текстуресампле (этап m) использование (u ", v") в качестве координат

t (m)<sub>RGBA</sub> = t (m)<sub>RGBA</sub>\*

\[(t (n)<sub>б</sub> \* D3DTSS \_ бумпенвлскале (этап m)) +

D3DTSS \_ бумпенвлоффсет (этап m)\]

Данные регистрации, считанные инструкцией [тексбем](texbem---ps.md) или тексбемл, не могут быть считаны позже, за исключением других тексбем или тексбемл.


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a>Примеры

Ниже приведен пример шейдера с идентифицированными картами текстур и идентифицированными стадиями текстуры.


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



Для этого примера требуются следующие текстуры на следующих стадиях текстуры.

-   Этапу 0 назначается схема выпуклости с данными (du, DV) пертурбатион.
-   Этап 1 назначает текстурную карту с данными цвета.
-   тексбемл задает данные матрицы на стадии текстуры, которая является выборкой. Это отличается от функций конвейера с фиксированной функцией, где данные пертурбатион и матрицы занимают одну и ту же стадию текстуры.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 