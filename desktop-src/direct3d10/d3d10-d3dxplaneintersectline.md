---
description: Функция D3DXPlaneIntersectLine (D3DX10Math. h) — Находит пересечение между плоскостью и линией.
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: Функция D3DXPlaneIntersectLine (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9d70f588c9f4ec54fd5889f8effb503c62235441fe425d38ea9dbed620fd3e8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754164"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a>Функция D3DXPlaneIntersectLine (D3DX10Math. h)

Находит пересечение между плоскостью и линией.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), определяющий пересечение между указанной плоскостью и линией.

</dd> <dt>

*PP* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Указатель на источник [**D3DXPLANE**](d3d10-d3dxplane.md).

</dd> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на исходную структуру D3DXVECTOR3, определяющую начальную точку строки.

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на исходную структуру D3DXVECTOR3, определяющую конечную точку строки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на структуру D3DXVECTOR3, которая является пересечением между указанной плоскостью и линией.

## <a name="remarks"></a>Remarks

Если линия параллельна плоскости, возвращается **значение NULL** .

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXPlaneIntersectLine может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
