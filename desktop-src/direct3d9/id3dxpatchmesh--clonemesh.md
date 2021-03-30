---
description: Создает новую сетку исправлений с указанным объявлением вершины.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'Метод ID3DXPatchMesh:: Клонемеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354323"
---
# <a name="id3dxpatchmeshclonemesh-method"></a>Метод ID3DXPatchMesh:: Клонемеш

Создает новую сетку исправлений с указанным объявлением вершины.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) , задающих параметры создания для сетки.

</dd> <dt>

*пдекл* \[ окне\]
</dt> <dd>

Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , задающих формат вершины для вершин в выходной сетке.

</dd> <dt>

*пмеш* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Адрес указателя на интерфейс [**ID3DXPatchMesh**](id3dxpatchmesh.md) , представляющий клонированную сетку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

**Клонемеш** Преобразует буфер вершин в новое объявление вершины. Записи в объявлении вершины, которые являются новыми для исходной сетки, имеют значение 0. Если текущая сеть имеет соседства, то новая сеть также будет иметь соседства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
