---
title: emitThenCut_stream (SM5-ASM)
description: Эквивалентно команде Emit, за которой следует команда Cut. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986265"
---
# <a name="emitthencut_stream-sm5---asm"></a>\_поток емитсенкут (SM5-ASM)

Эквивалентно команде [Emit](emit--sm4---asm-.md) , за которой следует команда [Cut](cut--sm4---asm-.md) .



| Емитсенкут \_ Stream стреаминдекс |
|---------------------------------|



 



| Элемент                                                                                                               | Описание                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*стреаминдекс*<br/> | \[в \] индексе потока.<br/> |



 

## <a name="remarks"></a>Примечания

Эта операция полезна, когда вы узнаете о размещении последней вершины в топологии.

Если потоки не объявлены, необходимо использовать [емитсенкут](emitthencut--sm4---asm-.md) вместо **\_ потока емитсенкут**.

Эта инструкция применяется к следующим этапам шейдера:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта инструкция поддерживается в следующих моделях шейдеров:



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Нет        |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Нет        |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сборка Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





