---
description: Этот метод используется для повторного получения ресурсов и сохранения начального состояния.
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'Метод ID3DXEffect:: Онресетдевице (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d419ad456fcefbf0d6e4a201d4949556d6694e46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703702"
---
# <a name="id3dxeffectonresetdevice-method"></a>Метод ID3DXEffect:: Онресетдевице

Этот метод используется для повторного получения ресурсов и сохранения начального состояния.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

**ID3DXEffect:: онресетдевице** должен вызываться каждый раз при сбросе устройства (с помощью [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) перед вызовом других методов. Это удобное место для повторного получения ресурсов видеопамяти и блоков состояния захвата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
