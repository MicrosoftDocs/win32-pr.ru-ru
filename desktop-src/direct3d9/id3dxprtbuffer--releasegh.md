---
description: Отменяет связь присоединенного объекта ID3DXTextureGutterHelper с объектом ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'Метод ID3DXPRTBuffer:: Релеасегх (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424526"
---
# <a name="id3dxprtbufferreleasegh-method"></a>Метод ID3DXPRTBuffer:: Релеасегх

Отменяет связь присоединенного объекта [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) с объектом [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод освобождает указатель на интерфейс [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .

Необходимо убедиться, что число вызовов [**ID3DXPRTBuffer:: аттачгх**](id3dxprtbuffer--attachgh.md) соответствует числу вызовов **ID3DXPRTBuffer:: релеасегх** . После вызова **ID3DXPRTBuffer:: релеасегх** указатель ПГХ, возвращенный **ID3DXPRTBuffer:: аттачгх** , больше не должен использоваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer:: Аттачгх**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




