---
description: Завершает сцену.
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'Метод ID3DXRenderToSurface:: Ендсцене (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821013"
---
# <a name="id3dxrendertosurfaceendscene-method"></a>Метод ID3DXRenderToSurface:: Ендсцене

Завершает сцену.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Мипфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметры фильтра, перечисленные в [ \_ фильтре D3DX](d3dx-filter.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface:: Бегинсцене**](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
