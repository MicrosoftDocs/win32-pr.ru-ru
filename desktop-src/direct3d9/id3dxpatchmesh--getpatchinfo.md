---
description: Возвращает атрибуты исправления.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'Метод ID3DXPatchMesh:: Жетпатчинфо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664987"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a>Метод ID3DXPatchMesh:: Жетпатчинфо

Возвращает атрибуты исправления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Патчинфо* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**

Указатель на структуры, содержащие атрибуты исправления. Дополнительные сведения об атрибутах исправления см. в разделе [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




