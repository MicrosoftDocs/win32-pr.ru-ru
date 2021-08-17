---
description: Разблокируйте буфер индексов.
ms.assetid: de3d0893-1596-42df-b049-6574c58ffa8d
title: 'Метод ID3DXPatchMesh:: Унлоккиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 995a9ff69c4b1404035e323f85540f232ad01aa7dc46efaa5e42acd79429052d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120648"
---
# <a name="id3dxpatchmeshunlockindexbuffer-method"></a>Метод ID3DXPatchMesh:: Унлоккиндексбуффер

Разблокируйте буфер индексов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Буфер индексов обычно блокируется, записывается в, а затем разблокируется для чтения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




