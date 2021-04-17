---
description: Преобразует массив (x, y, 0, 0) в заданную матрицу.
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: Функция D3DXVec2TransformNormalArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4850961560ae810b9a21f58fbefa9b6b07227c77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694244"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a>Функция D3DXVec2TransformNormalArray (D3DX10Math. h)

Преобразует массив (x, y, 0, 0) в заданную матрицу.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.

</dd> <dt>

*Шаг* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг между векторами в потоке выходных данных.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на исходный массив D3DXVECTOR2.

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

Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Указатель на структуру D3DXVECTOR2, которая является преобразованным массивом.

## <a name="remarks"></a>Комментарии

Эта функция преобразует вектор (pV->x, pV->y, 0, 0) на матрицу, на которую указывает pM.

Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция **D3DXVec2TransformNormalArray** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
