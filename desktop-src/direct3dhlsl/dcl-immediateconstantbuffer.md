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
ms.openlocfilehash: 781a792257b23a3d89cfa432ccc1ead9e5d756159beb428defc3404ba32df47c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024804"
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

### <a name="remarks"></a>Remarks

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
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | Да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Да       |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сборка Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




