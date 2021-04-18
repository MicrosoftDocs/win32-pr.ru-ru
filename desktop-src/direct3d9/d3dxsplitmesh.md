---
description: Разделяет сетку на сетки меньше указанного размера.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Функция D3DXSplitMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713640"
---
# <a name="d3dxsplitmesh-function"></a>Функция D3DXSplitMesh

Разделяет сетку на сетки меньше указанного размера.

## <a name="syntax"></a>Синтаксис


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмешин* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий исходную сетку.

</dd> <dt>

*паджаценциин* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сетке, которую необходимо упростить.

</dd> <dt>

*MAXSIZE* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md)**

Максимальное количество вершин в результирующей сетке.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md)**

Флаги параметров для новых сеток.

</dd> <dt>

*пмешесаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Число возвращенных сеток.

</dd> <dt>

*ппмешаррайаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер, содержащий массив интерфейсов [**ID3DXMesh**](id3dxmesh.md) для новых сеток. Для исходной сетки, разделенной на n сеток, *ппмешаррайаут* является массивом из n **ID3DXMesh** указателей.

</dd> <dt>

*ппаджаценциаррайаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер, содержащий массив смежных массивов (DWORD) для новых сеток. См. [**ID3DXBuffer**](id3dxbuffer.md). Это необязательный параметр.

</dd> <dt>

*ппфацеремапаррайаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер, содержащий массив массивов для сопоставления лиц (DWORD) для новых сеток. См. [**ID3DXBuffer**](id3dxbuffer.md). Это необязательный параметр.

</dd> <dt>

*ппвертремапаррайаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер, содержащий массив массивов сопоставления вершин для новых сеток. См. [**ID3DXBuffer**](id3dxbuffer.md). Этот параметр является необязательным.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Обычно эта функция используется для разбиения сетки с 32-битовыми индексами (более 65535 вершин) в несколько сеток, каждая из которых имеет 16-разрядные индексы.

Массивы — это массивы типа DWORD, где каждый массив содержит n указателей DWORD, за которыми следуют данные типа DWORD, на которые ссылаются указатели. Например, чтобы получить сведения о сопоставлении лиц для грани 3 в сетке 2, можно использовать следующий код, предполагая, что данные о переназначении лица были возвращены в переменной с именем *ппфацеремапаррайаут*.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
