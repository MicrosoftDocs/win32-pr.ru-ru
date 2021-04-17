---
description: Конструирует плоскость с точки и обычного.
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: Функция D3DXPlaneFromPointNormal (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9900a9f6838e253bd195374d00f90ee31fae07a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720954"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a>Функция D3DXPlaneFromPointNormal (D3DX10Math. h)

Конструирует плоскость с точки и обычного.

## <a name="syntax"></a>Синтаксис


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Указатель на [**D3DXPLANE**](d3d10-d3dxplane.md) , который является результатом операции.

</dd> <dt>

*ппоинт* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), определяющий точку, используемую для создания плоскости.

</dd> <dt>

*пнормал* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру D3DXVECTOR3, определяющую нормальную, используемую для создания плоскости.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Указатель на структуру D3DXPLANE, созданную из точки и обычного.

## <a name="remarks"></a>Комментарии

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция D3DXPlaneFromPointNormal может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
