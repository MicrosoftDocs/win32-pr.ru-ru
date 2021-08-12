---
title: dcl_globalFlags (SM4-ASM)
description: дкл \_ глобалфлагс (SM4-ASM)
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0901482dd2c282aab98dda72a5c449df69d4551a9a7bb68d80e47c9693c54609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286378"
---
# <a name="dcl_globalflags-sm4---asm"></a>дкл \_ глобалфлагс (SM4-ASM)

Объявляет глобальные флаги шейдера.



| \_ *Флаги* глобалфлагс дкл |
|--------------------------|



 

<dl> <dt>

<span id="flags"></span><span id="FLAGS"></span>*Метки*
</dt> <dd>

\[в \] флаге глобального шейдера. В настоящий момент определен один флаг.

-   РЕФАКТОРИНГ \_ разрешен — разрешает драйверу изменять порядок арифметических операций для оптимизации, как показано здесь.

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> Изменение порядка арифметических операций может привести к различным результатам.

 

</dd> </dl>

### <a name="remarks"></a>Remarks

Эта необязательная инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.

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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сборка Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




