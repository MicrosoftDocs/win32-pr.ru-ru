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
ms.openlocfilehash: 10b6d327b665b30418478d06d21433614587824eeb481202a9bef202b8727001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847444"
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
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




