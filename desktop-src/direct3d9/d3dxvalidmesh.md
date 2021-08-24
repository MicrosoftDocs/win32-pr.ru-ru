---
description: Проверяет сетку.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: Функция D3DXValidMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 299092700b015840376f3e4b297d7825366b6083e1458155f5963e1b5b1f4d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749674"
---
# <a name="d3dxvalidmesh-function"></a>Функция D3DXValidMesh

Проверяет сетку.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмешин* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий проверяемую сеть.

</dd> <dt>

*паджаценци* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждого лица в проверяемой сети.

</dd> <dt>

*пперрорсандварнингс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Возвращает буфер, содержащий строку ошибок и предупреждений, в которых объясняются проблемы, обнаруженные в сетке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DXERR \_ инвалидмеш, D3DERR \_ Инвалидкалл, E \_ OUTOFMEMORY.

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

 

 
