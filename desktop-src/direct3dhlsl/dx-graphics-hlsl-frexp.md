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
ms.openlocfilehash: 0f77ab30f525c37fcb2243bb6f634722420836f3893a4550edbb6604c8769773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276624"
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
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *exp* | то же, что входные данные *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| *обратно* | то же, что входные данные *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) и более высокие модели шейдеров | Да                 |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Да ( \_ только PS 2 \_ x) |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Нет                  |



 

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Корекрт \_ Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

