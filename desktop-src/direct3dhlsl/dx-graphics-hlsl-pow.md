---
title: pow
description: Возвращает указанное значение, возведенное в указанную степень.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- Pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9d26e150d611df12f2e042d2e20c06ab82172bbc3d2f241ee1ce3a4725f1193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120078"
---
# <a name="pow"></a>pow

Возвращает указанное значение, возведенное в указанную степень.



| *RET* Pow (*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] указанном значении.<br/> |
| <span id="y"></span><span id="Y"></span>*&*<br/> | \[в \] заданной степени.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Параметр *x* , возведенный в степень параметра *y* .

## <a name="remarks"></a>Remarks

Встроенная функция **Pow** HLSL вычисляет *x*<sup>y</sup>.



| X      | Y      | Результат                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| < 0 | any    | Не число                                                                         |
| > 0 | = = 0   | 1                                                                           |
| = = 0   | > 0 | 0                                                                           |
| = = 0   | < 0 | файлу                                                                         |
| > 0 | < 0 | 1/X<sup>-Y</sup>                                                            |
| = = 0   | = = 0   | Зависит от конкретного графического процессора<br/> 0, 1 или NAN<br/> |



 

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | то же, что входные данные *x*                                                                                              | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| *обратно* | то же, что входные данные *x*                                                                                              | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Да                 |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да ( \_ только VS 1 1 \_ ) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

