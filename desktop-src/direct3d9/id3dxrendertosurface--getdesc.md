---
description: Извлекает параметры поверхности рендеринга.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'Метод ID3DXRenderToSurface:: desc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7dd6787ad8a81491e92af2a5ec1a16253af4cd0a0f8cb075dde01461b0010d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790484"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>Метод ID3DXRenderToSurface:: DESC

Извлекает параметры поверхности рендеринга.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппараметерс* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***

Указатель на структуру [**\_ DESC D3DXRTS**](d3dxrts-desc.md) , описывающую параметры поверхности рендеринга.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 




