---
description: Извлекает устройство Direct3D, связанное с объектом Font.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: Метод ID3DXFont::-Device (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e0f89594f77044db20bade062b245ccabe072a0ccae1fb5fa76f23bb18a8db0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121151"
---
# <a name="id3dxfontgetdevice-method"></a>Метод ID3DXFont:: of Device

Извлекает устройство Direct3D, связанное с объектом Font.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдевице* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с объектом Font.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

> [!Note]  
> Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Не забудьте вызвать [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , когда вы завершите работу с этим интерфейсом **IDirect3DDevice9** , или у вас будет утечка памяти.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
