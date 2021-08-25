---
title: ASIN
description: Интерпретирует битовый шаблон x как целое число.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- ASIN HLSL
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 492e0b5e400adc4e5c847f12880a668fb5e3b98f683a0f64dbe32ec98f28a93c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789864"
---
# <a name="asint"></a>ASIN

Интерпретирует битовый шаблон *x* как целое число.



| RET-ASIN (*x*) |
|----------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[во \] входном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Входные данные, интерпретируемые как целое число.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md)                  | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *обратно* | то же, что входные данные *x*                                                                                              | [**INT**](/windows/desktop/WinProg/windows-data-types)                                           | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров | Да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Нет        |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

