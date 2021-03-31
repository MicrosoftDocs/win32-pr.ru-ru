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
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821412"
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
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




