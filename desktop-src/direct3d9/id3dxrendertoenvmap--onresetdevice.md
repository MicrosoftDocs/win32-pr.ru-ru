---
description: Этот метод используется для повторного получения ресурсов и сохранения начального состояния.
ms.assetid: 3e231ad6-858e-4b6a-bbea-0839794bbac7
title: 'Метод ID3DXRenderToEnvMap:: Онресетдевице (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d429c08d8bad23652a080998b6a4735132522ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354520"
---
# <a name="id3dxrendertoenvmaponresetdevice-method"></a>Метод ID3DXRenderToEnvMap:: Онресетдевице

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

**ID3DXRenderToEnvMap:: онресетдевице** должен вызываться каждый раз при сбросе устройства (с помощью [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) перед вызовом других методов. Это удобное место для повторного получения ресурсов видеопамяти и блоков состояния захвата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
