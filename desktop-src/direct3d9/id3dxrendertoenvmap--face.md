---
description: Инициирует рисование каждой грани схемы среды.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'Метод ID3DXRenderToEnvMap:: Face (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821484"
---
# <a name="id3dxrendertoenvmapface-method"></a>Метод ID3DXRenderToEnvMap:: Face

Инициирует рисование каждой грани схемы среды.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Лицо* \[ окне\]
</dt> <dd>

Тип: **[ **D3DCUBEMAP \_ лиц**](./d3dcubemap-faces.md)**

Первое лицо из схемы куба среды. См [**. \_ раздел D3DCUBEMAP**](./d3dcubemap-faces.md)Face.

</dd> <dt>

*Мипфилтер* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Допустимое сочетание одного или нескольких флагов [ \_ фильтра D3DX](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Этот метод должен вызываться один раз для каждого типа схемы среды. Единственным исключением является схема среды кубического типа, которая требует, чтобы этот метод вызывался шесть раз, один раз для каждого из граней в D3DCUBEMAP Face \_ . Дополнительные сведения см. в разделе [сопоставление среды (Direct3D 9)](environment-mapping.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
