---
title: f32tof16 (SM5-ASM)
description: Float16 на уровне компонентов для преобразования float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7f2a5810024800c812780a8138948ec873f20d1dfe95d554718a6d63b38cb88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907748"
---
# <a name="f32tof16-sm5---asm"></a>f32tof16 (SM5-ASM)

Float16 на уровне компонентов для преобразования float32.



| f32tof16 dest \[ . Mask \] , \[ - \] src \[ . свиззле\] |
|----------------------------------------------|



 



| Элемент                                                            | Описание                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] адресе результата float16.<br/> |
| <span id="src"></span><span id="SRC"></span>*src*<br/>    | \[в \] преобразуемом значении float32.<br/>  |



 

## <a name="remarks"></a>Remarks

Эта инструкция выполняет покомпонентное преобразование значения float32 в результат float16, который помещается в ЛСБ 16 бит.

Эта инструкция соответствует правилам D3D для преобразования с плавающей запятой.

Используйте эту инструкцию для сжатия данных, основанного на шейдере.

Эта инструкция применяется к следующим этапам шейдера:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта инструкция поддерживается в следующих моделях шейдеров:



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | Да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Нет        |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Нет        |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сборка Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





