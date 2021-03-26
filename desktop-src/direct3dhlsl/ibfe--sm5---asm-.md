---
title: ибфе (SM5-ASM)
description: При наличии диапазона битов в числе сдвигают эти биты в ЛСБ и знак, расширяя диапазон в диапазоне.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784905"
---
# <a name="ibfe-sm5---asm"></a>ибфе (SM5-ASM)

При наличии диапазона битов в числе сдвигают эти биты в ЛСБ и знак, расширяя диапазон в диапазоне.



| ибфе dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] , src2 \[ . свиззле\] |
|--------------------------------------------------------------------------|



 



| Элемент                                                            | Описание                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] адресе результатов операции.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в \] битовой ширине.<br/>                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[в \] битовом смещении.<br/>                         |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[в \] поле значение для сдвига.<br/>                          |



 

## <a name="remarks"></a>Примечания

ЛСБ 5 бит src0 (0-31) обеспечивает ширину битовых разрядов.

ЛСБ 5 бит src1 предоставляет смещение битовых разрядов (0-31).

В следующем примере показано, как использовать эту инструкцию.

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

Используйте эту инструкцию для распаковки целых чисел со знаком или флагов.

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

 

 





