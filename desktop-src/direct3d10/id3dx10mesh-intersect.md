---
description: Определяет, пересекается ли луч с этой сеткой.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: Метод ID3DX10Mesh::Intersect (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1693db027baad13d69c43e394407ed8eb037d2dbb95eb217ccca473d1f91d08a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634554"
---
# <a name="id3dx10meshintersect-method"></a>Метод ID3DX10Mesh:: Intersect

Определяет, пересекается ли луч с этой сеткой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прайпос* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , указывающий точку, с которой начинается луч.

</dd> <dt>

*прайдир* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , в которой указывается направление луча.

</dd> <dt>

*фиткаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Количество раз, когда луч пересекается с сеткой.

</dd> <dt>

*пфацеиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на значение индекса стороны, ближайшее к началу луча, если Фит имеет **значение true**.

</dd> <dt>

*PU* \[ окне\]
</dt> <dd>

Тип: **float \***

Указатель на барицентрик координату нажатия, U.

</dd> <dt>

*ПС* \[ окне\]
</dt> <dd>

Тип: **float \***

Указатель на барицентрик координату, V.

</dd> <dt>

*пдист* \[ окне\]
</dt> <dd>

Тип: **float \***

Указатель на расстояние с параметром пересечения лучей.

</dd> <dt>

*ппаллхитс* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), содержащий массив структур [**\_ \_ сведений о пересечении D3DX10**](d3dx10-intersect-info.md) . Это список всех попаданий, произошедших в тесте пересечения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Этот API позволяет понять точки в и вокруг треугольника независимо от того, где фактически находится треугольник. Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + U (V2-v1) + V (v3-v1).

Любая точка в плоскости V1V2V3 может быть представлена координатой барицентрик (U, V). Параметр U управляет тем, сколько v2 имеет взвешенное значение в результате, а параметр V определяет, сколько будет иметь взвешенное значение v3 в результате. Наконец, значение \[ 1 (U + V) \] определяет, сколько единиц измерения v1 будет взвешено по результату.

Координаты барицентрик — это форма общих координат. В этом контексте использование координат барицентрик представляет собой изменение в системах координат. Что содержит значение true для декартовых координат, имеет значение true для координат барицентрик.

Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника. Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
