---
description: Определяет, пересекает ли луч объем ограничивающего прямоугольника сферы.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: Функция D3DXSphereBoundProbe (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbab8a49165a87f73037ae25230d67b02222fc15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674695"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>Функция D3DXSphereBoundProbe (D3DX9Mesh. h)

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

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , задавая центральную координату сферы.

</dd> <dt>

*Радиус* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Радиус сферы.

</dd> <dt>

*прайпоситион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , задавая координату начала луча.

</dd> <dt>

*прайдиректион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается направление луча. Этот вектор не должен быть (0, 0, 0), но не требует нормализации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращает **значение true** , если луч пересекает объем ограничивающего прямоугольника сферы. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Комментарии

**D3DXSphereBoundProbe** определяет, пересекает ли луч объем ограничивающего прямоугольника сферы, а не только поверхность сферы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
