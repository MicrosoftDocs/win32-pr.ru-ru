---
title: f32tof16 (SM5-ASM)
description: Float16 на уровне компонентов для преобразования float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986705"
---
# <a name="f32tof16-sm5---asm"></a>f32tof16 (SM5-ASM)

Float16 на уровне компонентов для преобразования float32.



| f32tof16 dest \[ . Mask \] , \[ - \] src \[ . свиззле\] |
|----------------------------------------------|



 



| Элемент                                                            | Описание                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] адресе результата float16.<br/> |
| <span id="src"></span><span id="SRC"></span>*src*<br/>    | \[в \] преобразуемом значении float32.<br/>  |



 

## <a name="remarks"></a>Примечания

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

 

 





