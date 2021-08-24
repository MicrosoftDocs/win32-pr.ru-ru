---
description: 'Метод ID3DXRenderToEnvMap:: Онлостдевице. Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.'
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: 'Метод ID3DXRenderToEnvMap:: Онлостдевице (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65aee3724cf4596f4ab54a1a27fcbb4ba482070c0aa3eb0ba68262fa94d24145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747694"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a>Метод ID3DXRenderToEnvMap:: Онлостдевице

Используйте этот метод, чтобы освободить все ссылки на ресурсы видеопамяти и удалить все статеблоккс. Этот метод должен вызываться при каждом потере устройства или перед сбросом устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Этот метод должен вызываться при каждом потере устройства или до того, как пользователь вызывает [**IDirect3DDevice9:: Reset**](/windows/desktop/api). Даже если устройство не было потеряно, **ID3DXRenderToEnvMap:: онлостдевице** отвечает за освобождение статеблоккс и других ресурсов, которые, возможно, потребуется освободить перед сбросом устройства. В результате объект Font не может быть использован повторно перед вызовом **IDirect3DDevice9:: Reset** , а затем [**ID3DXRenderToEnvMap:: онресетдевице**](id3dxrendertoenvmap--onresetdevice.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




