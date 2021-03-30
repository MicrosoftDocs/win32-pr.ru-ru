---
description: Инициация отрисовки сферической схемы среды.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'Метод ID3DXRenderToEnvMap:: Бегинсфере (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354570"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a>Метод ID3DXRenderToEnvMap:: Бегинсфере

Инициация отрисовки сферической схемы среды.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекс* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру, для которой необходимо выполнить рендеринг.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл. \_Ошибка E

## <a name="remarks"></a>Комментарии

Чтобы нарисовать грань, см. раздел [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: end**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
