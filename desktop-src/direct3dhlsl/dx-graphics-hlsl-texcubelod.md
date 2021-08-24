---
title: текскубелод
description: Пример текстуры Куба с MIP-карты. Лод mipmap указан в т.в.
ms.assetid: fa7b236d-2c52-42bd-9123-919541f9e675
keywords:
- Текскубелод HLSL
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9d4ccbb46dfb01cf983314c4b79ec45cbf25eb442615c6dd6965443505d4f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744814"
---
# <a name="texcubelod"></a>текскубелод

Пример текстуры Куба с MIP-карты. Лод mipmap указан в т.в.



| RET Текскубелод (s, t) |
|----------------------|



 

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
| s    | in     | [**объектами**](dx-graphics-hlsl-intrinsic-functions.md) | [самплеркубе](dx-graphics-hlsl-sampler.md)                    | 1    |
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

 

