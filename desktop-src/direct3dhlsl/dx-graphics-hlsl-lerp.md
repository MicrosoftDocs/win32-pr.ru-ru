---
title: лерп
description: Выполняет линейную интерполяцию.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- лерп HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6981ef4134bbce17cbc7fa1e17de4d55de198572716ac39cbdd44b5e552e7f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791640"
---
# <a name="lerp"></a>лерп

Выполняет линейную интерполяцию.



| *RET* лерп (*x*, *y*, *s*) |
|---------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] значении первого значения с плавающей точкой.<br/>                                                     |
| <span id="y"></span><span id="Y"></span>*&*<br/> | \[во \] втором значении с плавающей запятой.<br/>                                                    |
| <span id="s"></span><span id="S"></span>*#d0*<br/> | \[в \] значении с линейной интерполяцией между параметром *x* и параметром *y* .<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Результат линейной интерполяции.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | то же, что входные данные *x*                                                                                              | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| *s*   | то же, что входные данные *x*                                                                                              | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| *обратно* | то же, что входные данные *x*                                                                                              | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

## <a name="remarks"></a>Remarks

Линейная интерполяция основана на следующей формуле: x \* (1-s) + y \* , что может быть эквивалентно записано в виде x + s (y-x).

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Да                         |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да (VS 1 1 \_ \_ и PS \_ 1 \_ 1) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

