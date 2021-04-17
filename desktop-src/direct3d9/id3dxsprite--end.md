---
description: 'Вызывает ID3DXSprite:: Flush и восстанавливает состояние устройства до вызова ID3DXSprite:: Begin.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'Метод ID3DXSprite:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424453"
---
# <a name="id3dxspriteend-method"></a>Метод ID3DXSprite:: end

Вызывает [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) и восстанавливает состояние устройства до вызова [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT End();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Комментарии

**ID3DXSprite:: end** нельзя использовать в качестве замены для [**IDirect3DDevice9:: ендсцене**](/windows/desktop/api) или [**ID3DXRenderToSurface:: ендсцене**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: Begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 




