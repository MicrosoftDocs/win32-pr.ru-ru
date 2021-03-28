---
title: else (SM4-ASM)
description: Запускает блок else.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e283a2621c916ac254daab9f055be0ffe1ba67d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983889"
---
# <a name="else-sm4---asm"></a>else (SM4-ASM)

Запускает блок **else** .



| else |
|------|



 

## <a name="remarks"></a>Примечания

Формат токена содержит смещение соответствующей инструкции [endif](endif--sm4---asm-.md) в шейдере для удобства.

В следующем примере показано, как использовать инструкцию **else** .

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

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

 

 




