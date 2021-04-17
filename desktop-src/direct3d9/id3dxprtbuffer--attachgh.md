---
description: Связывает объект ID3DXTextureGutterHelper с объектом ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'Метод ID3DXPRTBuffer:: Аттачгх (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703870"
---
# <a name="id3dxprtbufferattachgh-method"></a>Метод ID3DXPRTBuffer:: Аттачгх

Связывает объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) с объектом [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПГХ* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Указатель на интерфейс [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) объекта, который содержит данные для переплета текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК.

## <a name="remarks"></a>Комментарии

Число ссылок объекта [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) будет автоматически увеличиваться на единицу. Все существующие указатели **ID3DXTextureGutterHelper** будут освобождены.

Необходимо убедиться, что число вызовов **ID3DXPRTBuffer:: аттачгх** соответствует числу вызовов [**ID3DXPRTBuffer:: релеасегх**](id3dxprtbuffer--releasegh.md) . После вызова **ID3DXPRTBuffer:: релеасегх** указатель ПГХ, возвращенный **ID3DXPRTBuffer:: аттачгх** , больше не должен использоваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer:: Релеасегх**](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




