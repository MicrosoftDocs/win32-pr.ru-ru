---
description: Функция D3DXUVAtlasCreate — создание UV-Atlas для сетки.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Функция D3DXUVAtlasCreate (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31ab8315370b68e2bc71e4a964440e7c7703d392cf5902e244e976080c893779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804085"
---
# <a name="d3dxuvatlascreate-function"></a>Функция D3DXUVAtlasCreate

Создайте UV Atlas для сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления Atlas. Как минимум, сетка должна содержать данные позиции и координаты двухмерной текстуры.

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

*пдваджаценци* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив соседических данных. При наличии 3 DWORD на грань, указывающих, какие треугольники являются смежными друг с другом (см. раздел [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md)).

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

Укажите качество создаваемых диаграмм. См. [**D3DXUVATLAS**](./d3dxuvatlas.md).

</dd> <dt>

*ппмешаут* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Указатель на созданную сетку с помощью Atlas (см. [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*ппфацепартитионинг* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на массив окончательных данных секционирования для граней. Каждый элемент содержит один DWORD для каждого лица (см. [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ппвертексремапаррай* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на массив повторно сопоставленных вершин. Каждый элемент массива определяет исходную вершину, из которой получена каждая конечная вершина (Если вершина была разделена во время повторного сопоставления). Каждый элемент массива содержит один DWORD на вершину.

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

## <a name="remarks"></a>Remarks

D3DXUVAtlasCreate может секционировать сетчатую геометрию двумя способами:

-   На основе числа диаграмм
-   На основе максимально допустимого растяжения. Если максимально допустимое растяжение равно 0, каждый треугольник скорее всего будет находиться в собственной диаграмме.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Инструмент Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
