---
description: Проверяет сетку исправлений, возвращая число вырожденных вершин и исправлений.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Функция D3DXValidPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c3b7b28c763691af83dbb1ed0fe406fa6d370c82f9d8ffa702afa69566f2597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523819"
---
# <a name="d3dxvalidpatchmesh-function"></a>Функция D3DXValidPatchMesh

Проверяет сетку исправлений, возвращая число вырожденных вершин и исправлений.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмешин* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

Указатель на интерфейс [**ID3DXPatchMesh**](id3dxpatchmesh.md) , представляющий проверяемую сетку исправлений.

</dd> <dt>

*пнумдеженератевертицес* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Возвращает число вырожденных вершин в сетке исправлений.

</dd> <dt>

*пнумдеженератепатчес* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Возвращает число вырожденных исправлений в сетке исправлений.

</dd> <dt>

*пперрорсандварнингс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Возвращает указатель на буфер, содержащий строку ошибок и предупреждений, объясняющих проблемы, обнаруженные в сетке исправлений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Этот метод проверяет сетку, проверяя наличие недопустимых индексов. Сведения об ошибках доступны в выходных данных отладчика.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
