---
title: dcl_immediateConstantBuffer (SM4-ASM)
description: дкл \_ иммедиатеконстантбуффер (SM4-ASM)
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335651"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a>дкл \_ иммедиатеконстантбуффер (SM4-ASM)

Объявляет буфер немедленных констант шейдера.



| дкл \_ иммедиатеконстантбуффер *значение (s)* |
|-----------------------------------------|



 

<dl> <dt>

<span id="value_s_"></span><span id="VALUE_S_"></span>*значения (с)*
</dt> <dd>

\[в \] буфере должно содержать по крайней мере одно значение, но не более 4096 значений.

</dd> </dl>

### <a name="remarks"></a>Примечания

Шейдер может иметь один непосредственный постоянный буфер. Доступ к буферу немедленных констант осуществляется так же, как и постоянный буфер с динамической индексацией.

Эта инструкция применяется к следующим этапам шейдера:



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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сборка Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




