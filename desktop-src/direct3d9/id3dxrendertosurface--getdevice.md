---
description: Извлекает устройство Direct3D, связанное с областью прорисовки.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: Метод ID3DXRenderToSurface::-Device (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac01744887412349c71daa34194fc3a0b03b19a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355833"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a>Метод ID3DXRenderToSurface:: of Device

Извлекает устройство Direct3D, связанное с областью прорисовки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдевице* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с областью прорисовки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл. Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Не забудьте вызвать [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , когда вы завершите работу с этим интерфейсом **IDirect3DDevice9** , или у вас будет утечка памяти.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
