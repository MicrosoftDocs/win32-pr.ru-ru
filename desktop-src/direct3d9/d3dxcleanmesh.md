---
description: Очищает сетку, подготавливая ее к упрощению.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Функция D3DXCleanMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647857"
---
# <a name="d3dxcleanmesh-function"></a>Функция D3DXCleanMesh

Очищает сетку, подготавливая ее к упрощению.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Клеантипе* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

Операции вершин, выполняемые при подготовке к очистке сетки. См. [**D3DXCLEANTYPE**](./d3dxcleantype.md).

</dd> <dt>

*пмешин* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий удаляемую сеть.

</dd> <dt>

*паджаценциин* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, указывающий три соседа для каждого лица в удаляемой сети.

</dd> <dt>

*ппмешаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий возвращенную очищенную сетку. Возвращается та же сетка, которая была передана, если очистка не была выполнена.

</dd> <dt>

*паджаценциаут* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сетке выходных данных.

</dd> <dt>

*пперрорсандварнингс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Возвращает буфер, содержащий строку ошибок и предупреждений, в которых объясняются проблемы, обнаруженные в сетке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Эта функция очищает сетку с помощью метода очистки и параметров, указанных в параметре Клеантипе. Описание доступных параметров см. в описании перечисления [**D3DXCLEANTYPE**](./d3dxcleantype.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
