---
description: Выполняет вычисление произведения двух сферовых гармонических функций (f и g). Обе функции имеют порядок N = 2.
ms.assetid: 9e0942ce-e39d-4147-9472-cda8a97fd390
title: Функция D3DXSHMultiply2 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a72cdf7eb28b06e11b4901ebd048af143dfbdb5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703905"
---
# <a name="d3dxshmultiply2-function-d3dx10mathh"></a>Функция D3DXSHMultiply2 (D3DX10Math. h)

Выполняет вычисление произведения двух сферовых гармонических функций (*f* и *g*). Обе функции имеют порядок N = 2.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT* D3DXSHMultiply2(
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

## <a name="remarks"></a>Комментарии

Произведение двух функций SH в заказе N = 2 создает функцию SH в заказе 2 × *N* -1 = 3, но результаты усекаются. Это означает, что продукт работает ( *f* × *g*  =  *g* x *f* ), но не связан ( *f* × (*g* x *h*) ≠ ( *f* × *g*) × *h* ).

Эта функция использует следующее уравнение:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



где y \_ i (s) — это функция-i sh, где f (s) и g (s) используют следующую функцию SH:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
