---
description: Функция D3DXSphereBoundProbe (D3DX10math. h). определяет, пересекает ли луч объем ограничивающего прямоугольника сферы.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Функция D3DXSphereBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108472"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a>Функция D3DXSphereBoundProbe (D3DX10math. h)

Определяет, пересекает ли луч объем ограничивающего прямоугольника сферы.

## <a name="syntax"></a>Синтаксис


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пцентер* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , задавая центральную координату сферы.

</dd> <dt>

*Радиус* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Радиус сферы.

</dd> <dt>

*прайпоситион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , задавая координату начала луча.

</dd> <dt>

*прайдиректион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , в которой указывается направление луча. Этот вектор не должен быть (0, 0, 0), но не требует нормализации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращает **значение true** , если луч пересекает объем ограничивающего прямоугольника сферы. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

**D3DXSphereBoundProbe** определяет, пересекает ли луч объем ограничивающего прямоугольника сферы, а не только поверхность сферы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
