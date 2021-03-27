---
title: frexp (Корекрт \_ Math. h)
description: Возвращает мантисса и экспоненту указанного значения с плавающей точкой.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000356"
---
# <a name="frexp"></a>frexp

Возвращает мантисса и экспоненту указанного значения с плавающей точкой.



| *RET* frexp (*x*, *exp*) |
|-------------------------|



 

Возвращаемое значение — мантисса, а значение, возвращаемое параметром *exp* , — показатель степени.

## <a name="parameters"></a>Параметры



| Элемент                                                         | Описание                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[в \] указанном значении с плавающей запятой. Если параметр *x* равен 0, эта функция возвращает 0 для мантиссаа и экспоненты.<br/> |
| <span id="exp"></span><span id="EXP"></span>*расширением*<br/> | \[\]возвращаемый экспонента параметра *x* .<br/>                                                                                   |



 

## <a name="return-value"></a>Возвращаемое значение

Мантисса параметра *x* .

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *exp* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| *обратно* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) и более высокие модели шейдеров | да                 |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Да ( \_ только PS 2 \_ x) |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Нет                  |



 

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Корекрт \_ Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

