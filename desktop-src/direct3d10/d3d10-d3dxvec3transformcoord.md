---
description: Функция D3DXVec3TransformCoord (D3DX10Math. h) — Преобразует трехмерный вектор в заданную матрицу с проецированием результата обратно в w = 1.
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: Функция D3DXVec3TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b50c6680a52ef64e46e8dace325f124362e4efa79576e0d386c445a3766bf943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729914"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a>Функция D3DXVec3TransformCoord (D3DX10Math. h)

Преобразует трехмерный вектор в заданную матрицу с проецированием результата обратно в w = 1.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на исходную структуру D3DXVECTOR3.

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на структуру D3DXVECTOR3, которая является преобразованным вектором.

## <a name="remarks"></a>Remarks

Эта функция преобразует вектор, НЗ (x, y, z, 1) матрицу, выполнив проецирование результата обратно в w = 1.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXVec3TransformCoord может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
