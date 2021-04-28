---
description: Функция D3DXFillTextureTX — использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: Функция D3DXFillTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 419dc0e7b4266a2fe32557c52ed4323b51a25843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107642"
---
# <a name="d3dxfilltexturetx-function"></a>Функция D3DXFillTextureTX

Использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* \[ в, out\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий заполняемую текстуру.

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

Ниже приведен пример такой функции HLSL:


```
float4 TextureGradientFill(
  float2 vTexCoord : POSITION, 
  float2 vTexelSize : PSIZE) : COLOR 
  {
    float r,g, b, xSq,ySq, a;
    xSq = 2.f*vTexCoord.x-1.f; xSq *= xSq;
    ySq = 2.f*vTexCoord.y-1.f; ySq *= ySq;
    a = sqrt(xSq+ySq);
    if (a > 1.0f) {
        a = 1.0f-(a-1.0f);
    }
    else if (a < 0.2f) {
        a = 0.2f;
    }
    r = 1-vTexCoord.x;
    g = 1-vTexCoord.y;
    b = vTexCoord.x;
    return float4(r, g, b, a);
    
  };
```



Обратите внимание, что входные параметры могут быть в любом порядке, но должны быть представлены обе семантики ввода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
