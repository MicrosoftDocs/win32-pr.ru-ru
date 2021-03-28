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
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104412273"
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
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | да       |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Модификаторы инструкций](instruction-modifiers.md)
</dt> </dl>

 

 




