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
ms.openlocfilehash: 371463bfc24cbdba63ac51c9b729c267b9d020dd260d6d1b6c6a378bb38c3524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987234"
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

## <a name="remarks"></a>Remarks

**ID3DXLine:: end** нельзя использовать в качестве замены для [**IDirect3DDevice9:: ендсцене**](/windows/desktop/api) или [**ID3DXRenderToSurface:: ендсцене**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine:: Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




