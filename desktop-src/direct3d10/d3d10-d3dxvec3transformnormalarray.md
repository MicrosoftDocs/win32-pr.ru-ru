---
description: Преобразует массив (x, y, z, 0) в заданную матрицу.
ms.assetid: 7f0a41ce-bd3a-4e35-9a5d-8178a4e7bd44
title: Функция D3DXVec3TransformNormalArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: facb5591becd27d3fff283e8d531118ca433d5d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674682"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx10mathh"></a>Функция D3DXVec3TransformNormalArray (D3DX10Math. h)

Преобразует массив (x, y, z, 0) в заданную матрицу.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на массив [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.

</dd> <dt>

*Шаг* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг между векторами в потоке выходных данных.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на исходный массив D3DXVECTOR3.

</dd> <dt>

*Встриде* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг между векторами во входном потоке данных.

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .

</dd> <dt>

*n* \[ в\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число элементов в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на массив D3DXVECTOR3, который является преобразованным массивом.

## <a name="remarks"></a>Комментарии

Эта функция преобразует вектор (ПС->x, pV->y, pV->z, 0) матрице, на которую указывает pM.

Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция **D3DXVec3TransformNormalArray** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
