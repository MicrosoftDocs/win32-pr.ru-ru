---
title: clip
description: Отменяет текущую точку, если указанное значение меньше нуля.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- обрезать HLSL
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f12c9ea508aa960b0f3b1ec255867fc8e4f37fbee580ee5517ba40cf3ae0d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118091072"
---
# <a name="clip"></a>clip

Отменяет текущую точку, если указанное значение меньше нуля.



| клип (*x*) |
|-----------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] указанном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Нет.

## <a name="remarks"></a>Remarks

Используйте встроенную функцию **Clip** HLSL, чтобы имитировать обтравочные плоскости, если каждый компонент параметра *x* представляет расстояние от плоскости.

Кроме того, используйте функцию **Clip** для проверки поведения альфа-канала, как показано в следующем примере:


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a>Описание типа



| Имя | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*  | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any  |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается               |
|-----------------------------------------------------------|-------------------------|
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Да (только для шейдера Pixel) |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Да (только для шейдера Pixel) |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Да (только для шейдера Pixel) |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Да (только для шейдера Pixel) |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

