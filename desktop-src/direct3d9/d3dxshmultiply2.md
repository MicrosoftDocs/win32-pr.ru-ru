---
description: Выполняет вычисление произведения двух функций, представленных с помощью SH (f и g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Функция D3DXSHMultiply2 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713610"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>Функция D3DXSHMultiply2 (D3dx9math. h)

Выполняет вычисление произведения двух функций, представленных с помощью SH (f и g).

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

Указатель на выходную функцию SH илм хранится в l \* l + m + l.

</dd> <dt>

*Общая папка* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Вход SH коеффс для первой функции.

</dd> <dt>

*PG* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Второй набор входных данных SH коеффс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на коэффициенты вывода SH.

## <a name="remarks"></a>Комментарии

Порядок — это число от 2 до 6 включительно. В действительности эта страница документирует несколько функций: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.

Вычисляет произведение двух функций, представленных с помощью SH (f и g), где *тоска* \[ i \] = int (y i (s) f (s) g (s) \_ \* \* ), где y \_ i (s) — это функция i-го sh, f (s) и g (s) — функции SH (сумма \_ i (y \_ i (s) \* c \_ i)). Order O определяет длины массивов, где всегда должно быть коэффициенты O ^ 2. В целом, произведение двух функций SH для Order O создает функцию SH в порядке 2 \* o-1, но результаты усекаются. Это означает, что продукт работает (f \* g = = g \* f), но не связан (f \* (g \* h)! = (f \* g) \* h.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
