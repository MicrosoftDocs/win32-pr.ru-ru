---
title: log2 (Корекрт \_ Math. h)
description: Возвращает логарифм по основанию 2 указанного значения.
ms.assetid: 0bc75697-92c0-4de5-89bd-2ce824baa03e
keywords:
- log2 HLSL
topic_type:
- apiref
api_name:
- log2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f606c668e20ef12ba4d1272cb7f8bd1e6060af18c78738801e4ea17ea29b6de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514105"
---
# <a name="log2"></a>log2

Возвращает логарифм по основанию 2 указанного значения.



| *RET* log2 (*x*) |
|-----------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] указанном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Логарифм по основанию 2 параметра *x* . Если параметр *x* отрицательный, эта функция возвращает неопределенное значение. Если параметр *x* равен 0, эта функция ВОЗВРАЩАЕТ + INF.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *обратно* | то же, что входные данные *x*                                                                                              | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Да                 |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да ( \_ только VS 1 1 \_ ) |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Корекрт \_ Math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

