---
title: освещенность — VS
description: Обеспечивает частичную поддержку освещения путем вычисления коэффициентов освещения из двух изделий с точками и экспоненты.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983857"
---
# <a name="lit---vs"></a>освещенность — VS

Обеспечивает частичную поддержку освещения путем вычисления коэффициентов освещения из двух изделий с точками и экспоненты.

## <a name="syntax"></a>Синтаксис



| освещенный DST, src |
|--------------|



 

где

-   DST — это регистр назначения.
-   src является исходным регистром.

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| индикатор                    | x    | x    | x    | x     | x    | x     |



 

Предполагается, что исходный вектор содержит значения, показанные в следующем псевдокоде.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



В следующем фрагменте кода показаны выполняемые операции.


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



Арифметическая точность с ограниченной точностью приемлема при оценке целевого компонента y (dest. y). Реализация должна поддерживать по крайней мере восемь дробных разрядов в аргументе питания. Продукты с точками вычисляются с помощью нормализованных векторов, а пределы для срезов — от-128 до 128.

Ошибка должна соответствовать сочетанию [логп-VS](logp---vs.md) и [exp-VS](exp---vs.md) или не более приблизительно одного значащих бит для 8-разрядного компонента цвета.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




