---
title: смусстеп
description: Возвращает гладкую Хермите интерполяцию между 0 и 1, если x находится в диапазоне от \ min, Max \.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- смусстеп HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983996"
---
# <a name="smoothstep"></a>смусстеп

Возвращает гладкую Хермите интерполяцию между 0 и 1, если *x* находится в диапазоне \[ *min*, *Max* \] .



| *RET* смусстеп (*min*, *Max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                         | Описание                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*минимум*<br/> | \[в \] минимальном диапазоне параметра *x* .<br/> |
| <span id="max"></span><span id="MAX"></span>*максимальной*<br/> | \[в \] максимальном диапазоне параметра *x* .<br/> |
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[в \] указанном значении для интерполяции.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0, если *x* меньше *min*; 1, если *x* больше *максимального*; в противном случае значение от 0 до 1, если *x* , находится в диапазоне \[ *min*, *Max* \] .

## <a name="remarks"></a>Примечания

Используйте встроенную функцию **смусстеп** HLSL, чтобы создать плавный переход между двумя значениями. Например, эту функцию можно использовать для плавного смешения двух цветов.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *min* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| *max* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| *обратно* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | да                 |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да ( \_ только VS 1 1 \_ ) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

