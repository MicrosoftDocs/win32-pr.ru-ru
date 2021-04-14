---
description: Задает значение албедо для каждого шаг текселя, перезаписывая предыдущие значения албедо.
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'Метод ID3DXPRTEngine:: Сетпертекселалбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424434"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a>Метод ID3DXPRTEngine:: Сетпертекселалбедо

Задает значение албедо для каждого шаг текселя, перезаписывая предыдущие значения албедо.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*палбедотекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на объект текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , в котором хранятся значения албедо.

</dd> <dt>

*Нумчаннелс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число устанавливаемых цветовых каналов. Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.

</dd> <dt>

*ПГХ* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Необязательный указатель на объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) . Если не указано, вспомогательный объект переплета текстуры создается и уничтожается внутренним образом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLED3DERR \_ аутофвидеомемори, D3DERR \_ васстиллдравинг, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
