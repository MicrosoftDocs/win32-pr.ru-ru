---
description: Функция D3DXVec2Transform (D3dx9math. h) — преобразует 2D-вектор по заданной матрице.
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: Функция D3DXVec2Transform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b9b0f5ae0e3fda05cd8bdd92ee73b826f81b970
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097952"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a>Функция D3DXVec2Transform (D3dx9math. h)

Преобразует двумерный вектор по заданной матрице.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является преобразованным вектором.

## <a name="remarks"></a>Remarks

Эта функция преобразует вектор *ПС* (x, y, 0, 1) на матрицу *PM*.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXVec2Transform** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2TransformCoord**](d3dxvec2transformcoord.md)
</dt> <dt>

[**D3DXVec2TransformNormal**](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




