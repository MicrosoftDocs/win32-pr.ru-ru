---
description: Вычисление точки в плоскости и вектора 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Функция D3DXPlaneDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4895a94ad50171682a8bd5247694c3b35a56d174b5477f5bbb2a621c1e74fa96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564634"
---
# <a name="d3dxplanedot-function"></a>Функция D3DXPlaneDot

Вычисление точки в плоскости и вектора 4D.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PP* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXPLANE**](d3dxplane.md) \***

Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Скалярное произведение плоскости и вектора 4D.

## <a name="remarks"></a>Remarks

В плоскости (a, b, c, d) и 4D Vector (x, y, z, w) возвращаемое значение этой функции равно \* x + b \* y + c \* z + d \* w. Функция **D3DXPlaneDot** полезна для определения связи плоскости с однородным координатами. Например, эта функция может использоваться для определения того, находится ли определенная Координата на определенной плоскости или на какой стороне определенной плоскости лежит определенная координата.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
