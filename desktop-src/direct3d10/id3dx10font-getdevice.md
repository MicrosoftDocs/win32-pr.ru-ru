---
description: Получите устройство Direct3D, связанное с объектом Font.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: Метод ID3DX10Font::-Device (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703803"
---
# <a name="id3dx10fontgetdevice-method"></a>Метод ID3DX10Font:: of Device

Получите устройство Direct3D, связанное с объектом Font.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдевице* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Адрес указателя на интерфейс ID3D10Device, представляющий объект устройства Direct3D, связанный с объектом Font.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе ID3D10Device. Не забудьте вызвать IUnknown, когда вы завершите работу с этим интерфейсом ID3D10Device, или у вас будет утечка памяти.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




