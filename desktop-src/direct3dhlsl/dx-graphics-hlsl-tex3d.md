---
title: tex3D (Справочник по HLSL)
description: Выберет трехмерную текстуру.
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f5f5ea1db13e2c7aea9ee27cb4035bc59b7ac2672e7cb7527f5bd749c8833e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744804"
---
# <a name="tex3d-hlsl-reference"></a>tex3D (Справочник по HLSL)

Выберет трехмерную текстуру.



| RET tex3D (s, t) |
|-----------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*#d0*<br/> | \[в \] состоянии выборки.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[в \] координатах текстуры.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Значение данных текстуры.

## <a name="type-description"></a>Описание типа



| Имя | В/Из | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**объектами**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| обратно  | out    | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Да (только для шейдера Pixel), но при компиляции необходимо использовать [устаревший параметр Compile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) . |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Да (только для шейдера Pixel)                                                                                                           |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Да (только для шейдера Pixel)                                                                                                           |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Да (только для шейдера Pixel)                                                                                                           |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

