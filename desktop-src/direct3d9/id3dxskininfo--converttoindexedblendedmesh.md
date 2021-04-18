---
description: Принимает сетку и возвращает новую сетку с весовыми коэффициентами перехода на вершину, индексами и комбинацией костей. В таблице описывается, какие палитры костей влияют на подмножества сетки.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'Метод ID3DXSkinInfo:: Конверттоиндекседблендедмеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703948"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>Метод ID3DXSkinInfo:: Конверттоиндекседблендедмеш

Принимает сетку и возвращает новую сетку с весовыми коэффициентами перехода на вершину, индексами и комбинацией костей. В таблице описывается, какие палитры костей влияют на подмножества сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Входная сетка. См. [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

В настоящее время не используется.

</dd> <dt>

*палеттесизе* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число матриц костей, доступных для обложки палитры матрицы.

</dd> <dt>

*паджаценциин* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Сведения о смежности входной сетки.

</dd> <dt>

*паджаценциаут* \[ окне\]
</dt> <dd>

Тип: **[ **лпдворд**](../winprog/windows-data-types.md)**

Сведения о смежной сетке выходных данных.

</dd> <dt>

*пфацеремап* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Массив DWORD, по одному на каждое лицо, который определяет исходную сетку, соответствующую каждой грани в смешанной сетке. Если значение, заданное для этого аргумента, равно **null**, данные сопоставления лиц не возвращаются.

</dd> <dt>

*ппвертексремап* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами. Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин. Этот параметр является необязательным. Может использоваться **значение NULL** .

</dd> <dt>

*пмаксвертексинфл* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на DWORD, который будет содержать максимальное количество влияния на кость, необходимых для каждого из этих методов.

</dd> <dt>

*пнумбонекомбинатионс* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на число костей в таблице сочетаний костей.

</dd> <dt>

*ппбонекомбинатионтабле* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на таблицу сочетаний костей. Данные организованы в виде структуры [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .

</dd> <dt>

*ппмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Указатель на новую сетку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Каждый элемент в массивах сопоставления указывает предыдущий индекс для этой позиции. Например, если вершина находится в положении 3, но была повторно сопоставлена с позицией 5, то Пятый элемент Пвертексремап будет содержать значение 3.

Этот метод не выполняется на оборудовании, не поддерживающем смешение вершин с фиксированной функцией.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
