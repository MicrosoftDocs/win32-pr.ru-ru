---
description: Ресамплинг входного буфера ID3DXPRTBuffer и сохранение его в выходной буфер. Этот метод можно использовать для преобразования буфера вершин в буфер текстуры и наоборот. Он также может использоваться для преобразования одноканальных буферов в 3-канальные буферы и наоборот.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'Метод ID3DXPRTEngine:: Ресамплебуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa945be7b01c928a5dc8f5e44a6a31e8cb6d879be102145d25e03e7bef73f3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729618"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>Метод ID3DXPRTEngine:: Ресамплебуффер

Ресамплинг входного буфера [**ID3DXPRTBuffer**](id3dxprtbuffer.md) и сохранение его в выходной буфер. Этот метод можно использовать для преобразования буфера вершин в буфер текстуры и наоборот. Он также может использоваться для преобразования одноканальных буферов в 3-канальные буферы и наоборот.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбуфферин* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на входной буфер [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

</dd> <dt>

*пбуффераут* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на выходной буфер [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




