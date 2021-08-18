---
description: Упаковка данных секционирования сетки в Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Функция D3DXUVAtlasPack (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6990d6fbc114c874b31d0035a2415d48161d3065718efce3783a041a2097e96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749664"
---
# <a name="d3dxuvatlaspack-function"></a>Функция D3DXUVAtlasPack

Упаковка данных секционирования сетки в Atlas.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления Atlas. Как минимум, сетка должна содержать данные позиции и координаты двухмерной текстуры.

</dd> <dt>

*дввидс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ширина текстуры.

</dd> <dt>

*двхеигхт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Высота текстуры.

</dd> <dt>

*фгуттер* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Минимальное расстояние в пикселей текстуры между двумя диаграммами в Atlas. Переплет всегда масштабируется по ширине; Таким образом, если для текстуры 512 x 512 используется переплет 2,5, то минимальное расстояние между двумя диаграммами — 2,5/512,0 пикселей текстуры.

</dd> <dt>

*двтекстуреиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.

</dd> <dt>

*пдвпартитионресултаджаценци* 
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети. Он должен быть производным от Пппартитионресултаджаценци, возвращенного из [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md). Это значение не может быть **равно NULL**, поскольку пакету необходимо узнать, где были вырезаны диаграммы на шаге секционирования, чтобы найти края каждой диаграммы.

</dd> <dt>

*пкаллбакк* \[ окне\]
</dt> <dd>

Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Указатель на функцию обратного вызова (см. [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), который полезен для мониторинга хода выполнения.

</dd> <dt>

*фкаллбаккфрекуенци* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Укажите, как часто D3DX будет вызывать обратный вызов. разумное значение по умолчанию — 0,0001 f.

</dd> <dt>

*пусерконтент* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель типа void, который должен быть передан обратно функции обратного вызова.

</dd> <dt>

*двоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Этот параметр параметров в настоящее время зарезервирован.

</dd> <dt>

*пфацепартитионинг* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Указатель на объект [**ID3DXBuffer**](id3dxbuffer.md) , содержащий массив конечного секционирования. Каждый элемент содержит один DWORD для каждого лица.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
