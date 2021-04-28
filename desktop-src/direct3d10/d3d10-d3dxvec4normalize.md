---
description: Функция D3DXVec4Normalize (D3DX10Math. h) — Возвращает нормализованную версию вектора 4D.
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: Функция D3DXVec4Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1577ff3109c2cc3ca547f68f7841ecebb2f03569
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102912"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a>Функция D3DXVec4Normalize (D3DX10Math. h)

Возвращает нормализованную версию вектора 4D.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
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

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Указатель на структуру D3DXVECTOR4, которая является нормализованной версией вектора.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXVec4Normalize может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
