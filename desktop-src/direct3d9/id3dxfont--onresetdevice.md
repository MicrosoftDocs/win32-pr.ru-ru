---
description: 'Метод ID3DXFont:: Онресетдевице. Используйте этот метод для повторного получения ресурсов и сохранения начального состояния.'
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: 'Метод ID3DXFont:: Онресетдевице (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d976c29d370887362e46899c7fb2a654d6e2cc7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093742"
---
# <a name="id3dxfontonresetdevice-method"></a>Метод ID3DXFont:: Онресетдевице

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

**Онресетдевице** должен вызываться каждый раз при сбросе устройства (с помощью функции [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)) перед вызовом других методов. Это удобное место для повторного получения ресурсов видеопамяти и блоков состояния захвата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
