---
description: Извлекает устройство, связанное с объектом Sprite.
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: Метод ID3DXSprite::-Device (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf98eb932971a22232a5dbc8f0d5449f8639db97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424461"
---
# <a name="id3dxspritegetdevice-method"></a>Метод ID3DXSprite:: of Device

Извлекает устройство, связанное с объектом Sprite.

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

Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с объектом Sprite.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Комментарии

Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 
