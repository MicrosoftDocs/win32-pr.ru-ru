---
description: Функция D3DXMatrixScaling (D3DX10Math. h) — строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: Функция D3DXMatrixScaling (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bf11b2196953775fb41412ad484a77ab00ae578e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108932"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a>Функция D3DXMatrixScaling (D3DX10Math. h)

Строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.

</dd> <dt>

*SX* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент масштабирования, применяемый вдоль оси x.

</dd> <dt>

*SY* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент масштабирования, применяемый вдоль оси y.

</dd> <dt>

*SZ* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент масштабирования, применяемый вдоль оси z.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на D3DXMATRIX преобразования масштабирования.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXMatrixScaling может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
