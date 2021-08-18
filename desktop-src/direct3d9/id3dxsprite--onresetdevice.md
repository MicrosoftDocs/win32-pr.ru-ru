---
description: 'Метод ID3DXSprite:: Онресетдевице. Используйте этот метод для повторного получения ресурсов и сохранения начального состояния.'
ms.assetid: 74f8616e-c3ed-4231-b701-009213ea48c0
title: 'Метод ID3DXSprite:: Онресетдевице (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16086aca86e0df8c2c75e6a055be9fa95f7cc97259f37401aa932af962409811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800582"
---
# <a name="id3dxspriteonresetdevice-method"></a>Метод ID3DXSprite:: Онресетдевице

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

## <a name="remarks"></a>Remarks

**ID3DXSprite:: онресетдевице** должен вызываться каждый раз при сбросе устройства (с помощью [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) перед вызовом других методов. Это удобное место для повторного получения ресурсов видеопамяти и блоков состояния захвата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 
