---
title: макс.
description: Выбор большего числа x и y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- Максимальное HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e81eca4f5cabea57f36aa66b722fedb3e1176c3c189db9cdcfd610e4e26047c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791475"
---
# <a name="max"></a>макс.

Выбор большего числа x и y.



| RET-Max (x, y) |
|---------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] входном значении x.<br/> |
| <span id="y"></span><span id="Y"></span>*&*<br/> | \[во \] входном значении y.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Параметр *x* или *y* , в зависимости от самого крупного значения.


## <a name="remarks"></a>Remarks

Нормали обрабатываются следующим образом:

| src0 src1 — > | -inf | C             | +inf | Не число  |
|-------------|------|---------------|------|------|
| -inf        | -inf | src1          | +inf | -inf |
| C           | src0 | src0 или src1  | +inf | src0 |
| +inf        | +inf | +inf          | +inf | +inf |
| Не число         | -inf | src1          | +inf | Не число  |

F означает ограничение по настоящему вещественному числу.


## <a name="type-description"></a>Описание типа

| Имя | В/Из      | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md)                 | Размер                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| y    | in          | то же, что входные данные x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | те же измерения, что и входные x |
| обратно  | тип возвращаемого значения; | то же, что входные данные x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | те же измерения, что и входные x |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Да                         |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да (VS \_ 1 \_ 1 и PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**Функциональная спецификация DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
