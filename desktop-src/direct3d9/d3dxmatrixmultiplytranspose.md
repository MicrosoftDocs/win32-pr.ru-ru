---
description: Функция D3DXMatrixMultiplyTranspose (D3dx9math. h) — вычисляет транспроизведенное произведение двух матриц.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: Функция D3DXMatrixMultiplyTranspose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87aaa45e7a7a16884d17ab340f0bf1efeccd93bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107542"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a>Функция D3DXMatrixMultiplyTranspose (D3dx9math. h)

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

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.

</dd> <dt>

*pM1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .

</dd> <dt>

*pM2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является произведением двух матриц.

## <a name="remarks"></a>Remarks

Результатом является преобразование произведения двух матриц преобразования, out = T (M1 \* m2).

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* . Таким образом, функция **D3DXMatrixMultiplyTranspose** может использоваться в качестве параметра для другой функции.

Эта функция полезна для установки матриц в качестве констант для шейдеров вершин и пикселей.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> <dt>

[**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




