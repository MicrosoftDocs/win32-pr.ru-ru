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
ms.openlocfilehash: 9daa65558c58849d406056ce3358c26fdf2ce1c604342f993babe6af553d130f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629654"
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

## <a name="remarks"></a>Remarks

Вызов **ID3DXLine:: Begin** является необязательным. Если вызывается за пределами последовательности ID3DXLine:: Begin/ID3DXLine:: end, функции рисования будут внутренним вызовом ID3DXLine:: Begin и ID3DXLine:: end. Чтобы избежать дополнительных издержек, следует использовать этот метод, если несколько функций рисования будут вызываться последовательно.

Этот метод должен вызываться из последовательности [**IDirect3DDevice9:: бегинсцене**](/windows/desktop/api) и [**IDirect3DDevice9:: ендсцене**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .

ID3DXLine:: Begin не может использоваться в качестве замены для [**IDirect3DDevice9:: бегинсцене**](/windows/desktop/api) или [**ID3DXRenderToSurface:: бегинсцене**](id3dxrendertosurface--beginscene.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
