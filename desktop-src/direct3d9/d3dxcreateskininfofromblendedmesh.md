---
description: Создает сетку обложки из другой сетки.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Функция D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547927"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a>Функция D3DXCreateSkinInfoFromBlendedMesh

Создает сетку обложки из другой сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Указатель на объект [**ID3DXBaseMesh**](id3dxbasemesh.md) — сетку, из которой создается сетка обложки.

</dd> <dt>

*Нумбонес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Длина массива, присоединенного к Бонеид. См. [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*пбонекомбинатионтабле* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***

Указатель на массив сочетаний костей. См. [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*ппскининфо* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Адрес указателя на интерфейс [**ID3DXSkinInfo**](id3dxskininfo.md) , представляющий созданный объект сетки обложки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
