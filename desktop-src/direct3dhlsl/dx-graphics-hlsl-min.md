---
title: мин
description: Выбирает меньшее из значений x и y.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- min HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488212"
---
# <a name="min"></a>мин

Выбирает меньшее из значений x и y.



| RET-min (x, y) |
|---------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] входном значении x.<br/> |
| <span id="y"></span><span id="Y"></span>*&*<br/> | \[во \] входном значении y.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Параметр *x* или *y* , в зависимости от наименьшего значения.


## <a name="remarks"></a>Примечания

Нормали обрабатываются следующим образом:

| src0 src1 — > | -inf | C             | +inf | Не число  |
|-------------|------|---------------|------|------|
| -inf        | -inf | -inf          | -inf | -inf |
| C           | -inf | src0 или src1  | src0 | src0 |
| +inf        | -inf | src1          | +inf | +inf |
| не число         | -inf | src1          | +inf | не число  |

F означает ограничение по настоящему вещественному числу.


## <a name="type-description"></a>Описание типа

| Имя | В/Из      | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md)                 | Размер                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| да    | in          | то же, что входные данные x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | те же измерения, что и входные x |
| обратно  | тип возвращаемого значения; | то же, что входные данные x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | те же измерения, что и входные x |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | да                         |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да (VS \_ 1 \_ 1 и PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**Функциональная спецификация DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)