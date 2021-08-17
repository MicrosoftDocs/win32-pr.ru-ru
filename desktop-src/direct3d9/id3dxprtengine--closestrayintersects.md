---
description: Использует эффективную трассировку лучей в предварительно вычисленном моделировании радианце (PRT), чтобы определить, пересекаются ли луч с сеткой.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'Метод ID3DXPRTEngine:: Клосестрайинтерсектс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2620140337807891efa739da4540e3895394f63bcc494396c13e7c15d0c1b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729790"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a>Метод ID3DXPRTEngine:: Клосестрайинтерсектс

Использует эффективную трассировку лучей в предварительно вычисленном моделировании радианце (PRT), чтобы определить, пересекаются ли луч с сеткой. Если пересечение обнаружено, метод возвращает индекс ближайшей грани сетки, которая достигнута лучом, и координатами барицентрик точки пересечения.

## <a name="syntax"></a>Синтаксис


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прайпос* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , указывающий точку, с которой начинается луч.

</dd> <dt>

*прайдир* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается нормализованное направление луча.

</dd> <dt>

*пфацеиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на индекс текущей грани сетки, который первым помещается на данный луч, на основе стека всех граней в сетке, расположенных перед текущей сеткой.

</dd> <dt>

*PU* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на барицентрик координату, U, для вершины 0 треугольника.

</dd> <dt>

*ПС* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на барицентрик координату, V, для вершины 1 треугольника.

</dd> <dt>

*пдист* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на расстояние точки пересечения вдоль луча.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращает **значение true** , если луч пересекает текущую сетку; в противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

Используйте [**ID3DXPRTEngine:: сетминмаксинтерсектион**](id3dxprtengine--setminmaxintersection.md) , чтобы задать минимальное и максимальное расстояние пересечения с лучом.

Координата барицентрик третьей вершины (вершина 2) треугольника — 1 (U + V).

Этот метод выполняется медленнее, чем [**ID3DXPRTEngine:: шадоврайинтерсектс**](id3dxprtengine--shadowrayintersects.md). Используйте **ID3DXPRTEngine:: шадоврайинтерсектс** , если расположение точки пересечения не требуется.

Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника. Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Шадоврайинтерсектс**](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine:: Сетминмаксинтерсектион**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
