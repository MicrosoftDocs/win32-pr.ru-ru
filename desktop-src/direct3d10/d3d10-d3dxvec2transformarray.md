---
description: Функция D3DXVec2TransformArray (D3DX10Math. h) — преобразует массив (x, y, 0, 1) по заданной матрице.
ms.assetid: 66c8909c-6c20-4b32-9546-fcf2d0e824fa
title: Функция D3DXVec2TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a795590530503819ae66d1e17f9a4c8f8236dfb3015af512f4c6e28d084ca778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989904"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a>Функция D3DXVec2TransformArray (D3DX10Math. h)

Преобразует массив (x, y, 0, 1) по заданной матрице.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
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

Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Указатель на структуру [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , которая является результатом операции.

</dd> <dt>

*Шаг* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг между векторами в потоке выходных данных.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Указатель на источник [**D3DXVECTOR2**](d3d10-d3dxvector2.md).

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

Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Указатель на структуру D3DXVECTOR4, которая является преобразованным массивом.

## <a name="remarks"></a>Remarks

Эта функция преобразует массив ПС (x, y, 0, 1) на матрицу pM.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
