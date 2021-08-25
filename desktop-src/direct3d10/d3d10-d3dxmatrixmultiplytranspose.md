---
description: Функция D3DXMatrixMultiplyTranspose (D3DX10Math. h) — вычисляет транспроизведенное произведение двух матриц.
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Функция D3DXMatrixMultiplyTranspose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55bf8dc8eaed13c6bfdc4a8cedacd02b9c5cc5aa11ca0d3e494ed194c8cc9245
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858784"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a>Функция D3DXMatrixMultiplyTranspose (D3DX10Math. h)

Вычисляет транспроизведенное произведение двух матриц.

## <a name="syntax"></a>Синтаксис


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.

</dd> <dt>

*pM1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру D3DXMATRIX (с левой стороны).

</dd> <dt>

*pM2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на исходную структуру D3DXMATRIX (правую часть).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Указатель на структуру D3DXMATRIX, которая является произведением двух матриц.

## <a name="remarks"></a>Remarks

Результатом является преобразование произведения двух матриц преобразования, out = T (M1 \* m2).

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXMatrixMultiplyTranspose может использоваться в качестве параметра для другой функции.

Эта функция полезна для установки матриц в качестве констант для шейдеров вершин и пикселей.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
