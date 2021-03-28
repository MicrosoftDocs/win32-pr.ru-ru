---
title: Break (SM4-ASM)
description: Перемещает точку выполнения в инструкцию после следующей ендлуп или ендсвитч.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335512"
---
# <a name="break-sm4---asm"></a>Break (SM4-ASM)

Перемещает точку выполнения в инструкцию после следующей [ендлуп](endloop--sm4---asm-.md) или [ендсвитч](endswitch--sm4---asm-.md).



| break |
|-------|



 

## <a name="remarks"></a>Примечания

Формат маркера содержит смещение соответствующей инструкции **ендлуп** или **ендсвитч** в шейдере для удобства.

В следующем примере показана инструкция **break** .


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



Эта инструкция должна находиться в **цикле** / **ендлуп** или в **случае** в **параметре** / **ендсвитч**.

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



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

[Сборка Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




