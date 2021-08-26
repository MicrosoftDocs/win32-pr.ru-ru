---
title: Емитсенкут (SM4-ASM)
description: Эквивалентно команде Emit, за которой следует команда Cut. | Емитсенкут (SM4-ASM)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab83fa3eca853a75dca74ef32116e3d13da2dbe76f34fa407f9b0d5f2459d66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023864"
---
# <a name="emitthencut-sm4---asm"></a>Емитсенкут (SM4-ASM)

Эквивалентно команде [Emit](emit--sm4---asm-.md) , за которой следует команда [Cut](cut--sm4---asm-.md) .



| емитсенкут |
|-------------|



 

## <a name="remarks"></a>Remarks

Эта команда полезна, когда вы узнаете о размещении последней вершины в топологии.

Если были объявлены потоки, необходимо использовать [ \_ поток емитсенкут](emitthencut-stream--sm5---asm-.md).

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



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

[Сборка Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




