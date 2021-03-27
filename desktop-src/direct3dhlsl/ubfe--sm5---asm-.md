---
title: убфе (SM5-ASM)
description: При наличии диапазона битов в числе сдвигают эти биты в ЛСБ и устанавливает оставшиеся биты в 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890004"
---
# <a name="ubfe-sm5---asm"></a>убфе (SM5-ASM)

При наличии диапазона битов в числе сдвигают эти биты в ЛСБ и устанавливает оставшиеся биты в 0.



| убфе dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] , src2 \[ . свиззле\] |
|--------------------------------------------------------------------------|



 



| Элемент                                                            | Описание                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] содержит результаты выполнения инструкции.<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в \] ЛСБ 5 бит обеспечивает ширину битовых разрядов (0-31).<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[в \] ЛСБ 5 бит *src1* предоставляет смещение битового смещения (0-31).<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[\]число для сдвига.<br/>                                         |



 

## <a name="remarks"></a>Примечания

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

Используйте эту инструкцию для распаковки целых чисел без знака или флагов.

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

 

 





