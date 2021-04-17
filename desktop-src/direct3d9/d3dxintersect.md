---
description: Определяет, пересекается ли луч с сеткой.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: Функция D3DXIntersect (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703785"
---
# <a name="d3dxintersect-function"></a>Функция D3DXIntersect

Определяет, пересекается ли луч с сеткой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Указатель на интерфейс [**ID3DXBaseMesh**](id3dxbasemesh.md) , представляющий проверяемую сеть.

</dd> <dt>

*прайпос* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , указывающий точку, с которой начинается луч.

</dd> <dt>

*прайдир* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается направление луча.

</dd> <dt>

*Фит* \[ заполняет\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)\***

Указатель на логическое значение. Если луч пересекает треугольную грань в сетке, это значение будет равно **true**. В противном случае это значение равно **false**.

</dd> <dt>

*пфацеиндекс* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на значение индекса стороны, ближайшее к началу луча, если Фит имеет **значение true**.

</dd> <dt>

*PU* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на барицентрик координату нажатия, U.

</dd> <dt>

*ПС* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на барицентрик координату, V.

</dd> <dt>

*пдист* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на расстояние с параметром пересечения лучей.

</dd> <dt>

*ппаллхитс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на объект [**ID3DXBuffer**](id3dxbuffer.md) , содержащий массив структур [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .

</dd> <dt>

*пкаунтофхитс* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на DWORD, содержащий количество записей в массиве Ппаллхитс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Функция **D3DXIntersect** предоставляет способ для понимания точек в треугольнике и вокруг него независимо от того, где фактически находится треугольник. Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + U (V2-v1) + V (v3-v1).

Любая точка в плоскости V1V2V3 может быть представлена координатой барицентрик (U, V). Параметр U управляет тем, сколько v2 имеет взвешенное значение в результате, а параметр V определяет, сколько будет иметь взвешенное значение v3 в результате. Наконец, значение \[ 1 (U + V) \] определяет, сколько единиц измерения v1 будет взвешено по результату.

Координаты барицентрик — это форма общих координат. В этом контексте использование координат барицентрик представляет собой изменение в системах координат. Что содержит значение true для декартовых координат, имеет значение true для координат барицентрик.

Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника. Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
