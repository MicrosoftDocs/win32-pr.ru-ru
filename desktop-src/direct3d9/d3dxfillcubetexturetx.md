---
description: Функция D3DXFillCubeTextureTX — использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: Функция D3DXFillCubeTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afdf80cf1557f8b08709536ef49b08206873f5758c4b02a12008b27b4413a116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731802"
---
# <a name="d3dxfillcubetexturetx-function"></a>Функция D3DXFillCubeTextureTX

Использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Указатель на объект [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий заполняемую текстуру.

</dd> <dt>

*птекстурешадер* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

Указатель на объект шейдера текстуры [**ID3DXTextureShader**](id3dxtextureshader.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Цель текстуры должна быть HLSL функцией, которая имеет следующую семантику:

-   Один входной параметр должен использовать семантику расположения.
-   Один входной параметр должен использовать семантику ПСИЗЕ.
-   Функция должна возвращать параметр, который использует семантику цвета.

Входные параметры могут быть в любом порядке. Пример см. в разделе [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
