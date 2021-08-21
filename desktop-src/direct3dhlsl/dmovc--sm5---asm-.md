---
title: дмовк (SM5-ASM)
description: Условное перемещение на уровне компонентов. | дмовк (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0ed15d81a91d8a93ce99eda3fa17b91900e0045301f1c5b5d1f56e4448954a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792385"
---
# <a name="dmovc-sm5---asm"></a>дмовк (SM5-ASM)

Условное перемещение на уровне компонентов.



| дмовк \[ \_ \] \[ . Mask \] , src0 \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src2 \[ \_ ABS \] \[ . свиззле \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Элемент                                                            | Описание                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] месте назначения перемещения.<br/> Если *src0*, то укажите *dest*  =  *src1* else   =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в \] компонентах для проверки условия.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[в \] компонентах для перемещения, если условие истинно.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[в \] компонентах для перемещения, если условие имеет значение false.<br/>                                      |



 

## <a name="remarks"></a>Remarks

В следующем примере показано, как использовать эту инструкцию.

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

Допустимыми масками для dest являются. XY,. ZW,. ксизв.

Допустимыми свиззлес для *src0* являются все. Первые два компонента, выполняемые после свиззле, используются для определения 2 32-разрядных значений условий.

Допустимые свиззлес для *src1* и *src2* , содержащие Double, — это. ксизв,. ксикси,. звкси,. звзв. имеют вид. XY,. ZW и. ксизв.

Следующие сопоставления *src* ниже являются свиззле.

-   *dest* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).
-   *src0* — это 32-разрядный или компонентный vec2 по осям x и y (ZW игнорируется).
-   *src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).
-   *src2* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).

Модификаторы для *src1* и *src2*, кроме свиззле, предполагают, что данные являются двойными. Отсутствие модификаторов перемещает данные без изменения битов.

Эта инструкция применяется к следующим этапам шейдера:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
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

 

 





