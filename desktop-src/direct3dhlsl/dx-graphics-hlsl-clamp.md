---
title: фиксаци
description: Отменяет указанное значение до указанного минимального и максимального диапазона.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- HLSL среза
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793308"
---
# <a name="clamp"></a>фиксаци

Отменяет указанное значение до указанного минимального и максимального диапазона.



| *RET* -зажим (*x*, *min*, *Max*) |
|--------------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                         | Описание                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[в \] значении для среза.<br/>            |
| <span id="min"></span><span id="MIN"></span>*минимум*<br/> | \[в \] указанном минимальном диапазоне.<br/> |
| <span id="max"></span><span id="MAX"></span>*максимальной*<br/> | \[в \] указанном максимальном диапазоне.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Значение среза для параметра *x* .

## <a name="remarks"></a>Примечания

Для значений параметра-INF или INF будет вести себя так, как ожидалось. Однако для значений NaN результаты не определены.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md)                 | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *min* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | те же измерения, что и входные *x* |
| *max* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | те же измерения, что и входные *x* |
| *обратно* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается             |
|------------------------------------------------------------------------------------|-----------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | да                   |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | VS \_ 1 \_ 1 и PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

