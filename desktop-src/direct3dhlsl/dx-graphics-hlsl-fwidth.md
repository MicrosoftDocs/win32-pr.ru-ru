---
title: фвидс
description: Возвращает абсолютное значение частичного производного указанного значения.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- фвидс HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: feee9a017664e71c9c96f19fda5106870c04b947dc2b668e67f376626f7ea38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120178"
---
# <a name="fwidth"></a>фвидс

Возвращает абсолютное значение частичного производного указанного значения.



| *RET* фвидс (*x*) |
|-------------------|



 

Эта функция вычислит следующее: [**ABS**](dx-graphics-hlsl-abs.md)([**DDX**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**ДДИ**](dx-graphics-hlsl-ddy.md)(*x*)).

Эта функция поддерживается только в шейдерах пикселей.

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] указанном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Абсолютное значение частичного производного параметра *x* .

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *обратно* | то же, что входные данные *x*                                                                                              | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) и более высокие модели шейдеров | Да                 |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Да ( \_ только PS 2 \_ x) |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Нет                  |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

