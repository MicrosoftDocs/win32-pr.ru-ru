---
description: Инициация отрисовки схемы кубической среды.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'Метод ID3DXRenderToEnvMap:: Бегинкубе (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 081e96425a7928cb1cd4a5a3ee48479d562c5c30a2f9017665acd32ffb539244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293278"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a>Метод ID3DXRenderToEnvMap:: Бегинкубе

Инициация отрисовки схемы кубической среды.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкубетекс* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Указатель на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий текстуру Куба, для которой необходимо выполнить рендеринг.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Рисование каждого из шести Сторон см. в разделе [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: end**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
