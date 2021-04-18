---
description: 'Восстанавливает состояние устройства в том виде, в котором оно было при вызове ID3DXLine:: Begin.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'Метод ID3DXLine:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694282"
---
# <a name="id3dxlineend-method"></a>Метод ID3DXLine:: end

Восстанавливает состояние устройства в том виде, в котором оно было при вызове [**ID3DXLine:: Begin**](id3dxline--begin.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT End();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Комментарии

**ID3DXLine:: end** нельзя использовать в качестве замены для [**IDirect3DDevice9:: ендсцене**](/windows/desktop/api) или [**ID3DXRenderToSurface:: ендсцене**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine:: Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




