---
title: tex2D (Справочник по HLSL) — выберите уровень MIP
description: Пример двухмерной текстуры с помощью градиента для выбора уровня MIP. | tex2D (Справочник по HLSL)
ms.assetid: 0e8c32ed-d174-4045-9cbf-6c04586ea5bb
keywords:
- tex2D HLSL
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 43e6d60505964beb47eb14bb797a60a3c78089371c9e1fd67463586ba1e5db0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513157"
---
# <a name="tex2d-hlsl-reference---select-the-mip-level"></a>tex2D (Справочник по HLSL) — выберите уровень MIP

Пример двухмерной текстуры с помощью градиента для выбора уровня MIP.



| RET tex2D (s, t, DDX, дди) |
|---------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                         | Описание                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*#d0*<br/>       | \[в \] состоянии выборки.<br/>                                         |
| <span id="t"></span><span id="T"></span>*t*<br/>       | \[в \] координатах текстуры.<br/>                                   |
| <span id="ddx"></span><span id="DDX"></span>*DDX*<br/> | \[\]интенсивность изменения геометрии поверхности в направлении x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*дди*<br/> | \[\]интенсивность изменения геометрии поверхности в направлении y.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Значение данных текстуры.

## <a name="type-description"></a>Описание типа



| Имя | В/Из | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**объектами**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| DDX  | in     | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| дди  | in     | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| обратно  | out    | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается                |
|-----------------------------------------------------------|--------------------------|
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Да (только для шейдера Pixel)  |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Да (только для шейдера Pixel) |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Да (только для шейдера Pixel) |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет                       |



 

1.  Значительный Переупорядочение кода выполняется для перемещения вычислений градиента за пределы управления потоком.
2.  Если для D3DPSHADERCAPS2 \_ 0 установлено значение D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс, компилятор сопоставляет эту функцию с текслдд.

## <a name="remarks"></a>Remarks

Когда управление потоком представлено в шейдере, результат вычисления градиента в заданном пути к ветви неоднозначен, если смежные Пиксели могут находиться в разных путях управления потоком. Поэтому считается недопустимым использование любой операции шейдера пикселей, запрашивающей вычисление градиента в расположении, находящегося внутри конструкции управления потоком, которая может меняться в пикселях для растрирования данного примитива. Если любая из сторон инструкции **If** с атрибутом Branch использует функцию градиента, может возникать ошибка компилятора. См. [инструкции if (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

