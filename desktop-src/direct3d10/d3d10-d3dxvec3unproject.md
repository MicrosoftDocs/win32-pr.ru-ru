---
description: Функция D3DXVec3Unproject (D3DX10Math. h) — Проецирует вектор из пространства экрана в объектное пространство.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: Функция D3DXVec3Unproject (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 08d38691d0e780e49293149bdb7a08b1ea0ef1fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103032"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a>Функция D3DXVec3Unproject (D3DX10Math. h)

Проецирует вектор из пространства экрана в объектное пространство.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
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

*пвиевпорт* \[ окне\]
</dt> <dd>

Тип: **const [**D3D10 \_ окно просмотра**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***

Указатель на [**\_ окно просмотра D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), представляющее окно просмотра.

</dd> <dt>

*ппрожектион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , представляющую матрицу проекции.

</dd> <dt>

*pView* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на структуру D3DXMATRIX, представляющую матрицу представления.

</dd> <dt>

*пворлд* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на структуру D3DXMATRIX, представляющую матрицу мира.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на структуру D3DXVECTOR3, которая представляет собой вектор, проецируемый из пространства экрана в объектное пространство.

## <a name="remarks"></a>Remarks

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXVec3Unproject может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
