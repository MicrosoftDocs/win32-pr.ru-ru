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
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713464"
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

## <a name="remarks"></a>Комментарии

В плоскости (a, b, c, d) и 4D Vector (x, y, z, w) возвращаемое значение этой функции равно \* x + b \* y + c \* z + d \* w. Функция **D3DXPlaneDot** полезна для определения связи плоскости с однородным координатами. Например, эта функция может использоваться для определения того, находится ли определенная Координата на определенной плоскости или на какой стороне определенной плоскости лежит определенная координата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
