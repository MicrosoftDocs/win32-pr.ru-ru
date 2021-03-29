---
title: tex3Dlod
description: Пример трехмерной текстуры с помощью MIP-карты. Лод mipmap указан в т.в.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- tex3Dlod HLSL
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983993"
---
# <a name="tex3dlod"></a>tex3Dlod

Пример трехмерной текстуры с помощью MIP-карты. Лод mipmap указан в т.в.



| RET tex3Dlod (s, t) |
|--------------------|



 

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
| t    | in     | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| обратно  | out    | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается               |
|-----------------------------------------------------------|-------------------------|
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Да (только для шейдера Pixel) |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Да (только для шейдера Pixel) |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет                      |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет                      |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

