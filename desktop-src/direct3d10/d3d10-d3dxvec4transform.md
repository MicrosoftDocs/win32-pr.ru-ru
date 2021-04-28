---
description: Функция D3DXVec4Transform (D3DX10Math. h) — преобразует вектор 4D по заданной матрице.
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: Функция D3DXVec4Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 737e1901a514a3940790ce83c7e9bc1f6f471371
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102922"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a>Функция D3DXVec4Transform (D3DX10Math. h)

Преобразует вектор 4D по заданной матрице.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Указатель на [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , который является результатом операции.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Указатель на исходную структуру D3DXVECTOR4.

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Указатель на структуру D3DXVECTOR4, которая является преобразованным вектором 4D.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXVec4Transform может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
