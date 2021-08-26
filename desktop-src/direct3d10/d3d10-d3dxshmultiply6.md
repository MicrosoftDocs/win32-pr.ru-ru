---
description: Выполняет вычисление произведения двух сферовых гармонических функций (f и g). Обе функции имеют порядок N = 6.
ms.assetid: 3b68b238-c1ae-4ab8-89ed-bdf815463143
title: Функция D3DXSHMultiply6 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply6
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b442d6d8c64d7c1ef0b202bd2cfa5d6d625280eb7320609a11ea89420c2bc215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990004"
---
# <a name="d3dxshmultiply6-function"></a>Функция D3DXSHMultiply6

Выполняет вычисление произведения двух сферовых гармонических функций (f и g). Обе функции имеют порядок N = 6.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT* D3DXSHMultiply6(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на выводимые коэффициенты SH — функция *Y* LM хранится в l ² + *m* + l. Порядок *n* определяет длину массива, где всегда должно быть коэффициентов *n*².

</dd> <dt>

*Общая папка* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Входные коэффициенты SH для первой функции.

</dd> <dt>

*PG* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Второй набор коэффициентов входных данных SH.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на коэффициенты вывода SH.

## <a name="remarks"></a>Remarks

Произведение двух функций SH в заказе N = 6 создает функцию SH в заказе 2 × *N* -1 = 11, но результаты усекаются. Это означает, что продукт работает ( *f* × *g*  =  *g* x *f* ), но не связан ( *f* × ( *g* x *h* ) ≠ ( *f* × *g* ) × *h* ).

Эта функция использует следующее уравнение:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



где y \_ i (s) — это функция-i sh, где f (s) и g (s) используют следующую функцию SH:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
