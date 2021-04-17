---
description: Подготавливает устройство для рисования линий.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'Метод ID3DXLine:: Begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694285"
---
# <a name="id3dxlinebegin-method"></a>Метод ID3DXLine:: Begin

Подготавливает устройство для рисования линий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Комментарии

Вызов **ID3DXLine:: Begin** является необязательным. Если вызывается за пределами последовательности ID3DXLine:: Begin/ID3DXLine:: end, функции рисования будут внутренним вызовом ID3DXLine:: Begin и ID3DXLine:: end. Чтобы избежать дополнительных издержек, следует использовать этот метод, если несколько функций рисования будут вызываться последовательно.

Этот метод должен вызываться из последовательности [**IDirect3DDevice9:: бегинсцене**](/windows/desktop/api) и [**IDirect3DDevice9:: ендсцене**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .

ID3DXLine:: Begin не может использоваться в качестве замены для [**IDirect3DDevice9:: бегинсцене**](/windows/desktop/api) или [**ID3DXRenderToSurface:: бегинсцене**](id3dxrendertosurface--beginscene.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
