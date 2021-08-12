---
title: каунтбитс (SM5-ASM)
description: Подсчитывает количество битов, заданных в числе.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b13be61d470f5a8504c893f85bea4b7f500591d35118aec2bf6576b897a4b5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286956"
---
# <a name="countbits-sm5---asm"></a>каунтбитс (SM5-ASM)

Подсчитывает количество битов, заданных в числе.



| каунтбитс dest \[ . Mask \] , src0 \[ . свиззле\] |
|-------------------------------------------|



 



| Элемент                                                            | Описание                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] адресе результатов.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[во \] входном 32-разрядном номере.<br/>    |



 

## <a name="remarks"></a>Remarks

Эту инструкцию можно использовать для расчета процентного покрытия заполнения шейдером.

Эта инструкция применяется к следующим этапам шейдера:



| Вершина | Поверхности | Домен | Geometry | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сборка Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





