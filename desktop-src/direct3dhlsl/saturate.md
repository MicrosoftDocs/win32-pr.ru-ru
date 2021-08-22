---
title: Насыщенность (ссылка HLSL)
description: Отменяет результат арифметической операции одинарной или двойной точности с плавающей запятой до 0,0 f... 1,0 f \ диапазон.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25e771bd53dbb8a4b0d2eaf8162675cd556c071344b249562defe4a06e715f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790747"
---
# <a name="saturate-hlsl-reference"></a>Насыщенность (ссылка HLSL)

Отменяет результат арифметической операции одинарной или двойной точности с плавающей запятой до \[ 0,0 f... 1,0 f \] диапазона.



| \_Кот |
|-------|



 

Модификатор результата инструкции " **насыщенность** " выполняет следующую операцию с результирующими значениями из арифметической операции с плавающей запятой, к которой \_ применены результаты.

`min(1.0f, max(0.0f, value))`

Если min () и Max () в приведенном выше выражении ведут себя так, как [min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [DMin](dmin--sm5---asm-.md)или [DMax](dmax--sm5---asm-.md) работают.

`_sat(NaN)` Возвращает 0, по правилам для min и Max.

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Этот модификатор поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | Да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Да       |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Модификаторы инструкций](instruction-modifiers.md)
</dt> </dl>

 

 




