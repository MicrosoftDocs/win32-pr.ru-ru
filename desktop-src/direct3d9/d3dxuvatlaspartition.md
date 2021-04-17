---
description: Создайте UV Atlas для сетки.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Функция D3DXUVAtlasPartition (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707a503832a4fd66ab2e8d9346587d11544a885c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703768"
---
# <a name="d3dxuvatlaspartition-function"></a>Функция D3DXUVAtlasPartition

Создайте UV Atlas для сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), содержащую объект Geometry для вычисления Atlas. Как минимум, сетка должна содержать данные позиции и координаты двухмерной текстуры.

</dd> <dt>

*двмаксчартнумбер* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальное число диаграмм, в которых нужно секционировать сетку. См. раздел Примечания о режимах секционирования. Используйте значение 0, чтобы сообщить D3DX, что Atlas следует заменять на основе растяжения.

</dd> <dt>

*фмаксстретч* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Допустимый объем растяжения. 0 означает, что растяжение не разрешено, 1 означает, что можно использовать любой уровень растяжения.

</dd> <dt>

*двтекстуреиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.

</dd> <dt>

*пдваджаценци* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из соседей данных с 3 DWORD на грань, указывающий, какие треугольники являются смежными друг с другом (см. [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*пдвфалсиджес* 
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Массив с 3 DWORD на грань. Каждая Сторона указывает, имеет ли граница значение false. Неложное ребро обозначается параметром-1, а значение false — с любым другим значением. Это обеспечивает параметризацию сетки из четырех, в которых края, расположенные в середине каждого из четырех, не будут вырезаны.

</dd> <dt>

*пфимтаррай* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на массив встроенных десятков метрик, описывающих растяжение треугольника (см. [интегратедметриктенсор](using-uvatlas.md)).

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

Указатель на определяемое пользователем значение, которое передается функции обратного вызова; обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.

</dd> <dt>

*двоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Укажите качество диаграмм, созданных путем объединения одного или нескольких флагов [**D3DXUVATLAS**](./d3dxuvatlas.md) .

</dd> <dt>

*ппмешаут* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Указатель на созданную сетку с помощью Atlas (см. [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*пфацепартитионинг* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Указатель на массив окончательных данных секционирования для граней. Каждый элемент содержит один DWORD для каждого лица (см. [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ппвертексремапаррай* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на массив повторно сопоставленных вершин. Каждый элемент массива определяет исходную вершину каждой конечной вершины (Если вершина была разделена во время повторного сопоставления). Каждый элемент массива содержит один DWORD на вершину.

</dd> <dt>

*пппартитионресултаджаценци* 
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) . Этот буфер будет содержать массив из трех DWORD на лицо, задающих три соседи для каждой грани в выходной сетке. Этот параметр не должен иметь **значение NULL**, поскольку он требуется для последующего вызова D3DXUVAtlasPack ().

</dd> <dt>

*пфмаксстретчаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на максимальное значение растяжения, созданное алгоритмом Atlas. Диапазон составляет от 0,0 до 1,0.

</dd> <dt>

*пдвнумчартсаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на число диаграмм, созданных алгоритмом Atlas. Если Двмаксчартнумбер имеет слишком малое значение, этот параметр возвратит минимальное число диаграмм, необходимых для создания Atlas.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

D3DXUVAtlasPartition похож на [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), за исключением того, что D3DXUVAtlasPartition не выполняет окончательный шаг упаковки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Инструмент Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
