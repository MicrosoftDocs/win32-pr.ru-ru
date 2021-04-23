---
description: Использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.
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
ms.openlocfilehash: 3605011f7967edec68d13405b4cabbd9c90d4c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081862"
---
# <a name="d3dxfilltexturetx-function"></a><span data-ttu-id="f7d94-103">Функция D3DXFillTextureTX</span><span class="sxs-lookup"><span data-stu-id="f7d94-103">D3DXFillTextureTX function</span></span>

<span data-ttu-id="f7d94-104">Использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.</span><span class="sxs-lookup"><span data-stu-id="f7d94-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7d94-105">Syntax</span></span>


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="f7d94-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7d94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d94-107">*птекстуре* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f7d94-107">*pTexture* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d94-108">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="f7d94-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="f7d94-109">Указатель на объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий заполняемую текстуру.</span><span class="sxs-lookup"><span data-stu-id="f7d94-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="f7d94-110">*птекстурешадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7d94-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d94-111">Тип: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="f7d94-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="f7d94-112">Указатель на объект шейдера текстуры [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="f7d94-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d94-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7d94-113">Return value</span></span>

<span data-ttu-id="f7d94-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7d94-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7d94-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f7d94-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f7d94-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f7d94-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d94-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7d94-117">Remarks</span></span>

<span data-ttu-id="f7d94-118">Цель текстуры должна быть HLSL функцией, которая имеет следующую семантику:</span><span class="sxs-lookup"><span data-stu-id="f7d94-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="f7d94-119">Один входной параметр должен использовать семантику расположения.</span><span class="sxs-lookup"><span data-stu-id="f7d94-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="f7d94-120">Один входной параметр должен использовать семантику ПСИЗЕ.</span><span class="sxs-lookup"><span data-stu-id="f7d94-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="f7d94-121">Функция должна возвращать параметр, который использует семантику цвета.</span><span class="sxs-lookup"><span data-stu-id="f7d94-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="f7d94-122">Ниже приведен пример такой функции HLSL:</span><span class="sxs-lookup"><span data-stu-id="f7d94-122">The following is an example of such an HLSL function:</span></span>


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



<span data-ttu-id="f7d94-123">Обратите внимание, что входные параметры могут быть в любом порядке, но должны быть представлены обе семантики ввода.</span><span class="sxs-lookup"><span data-stu-id="f7d94-123">Note that the input parameters can be in any order, but both input semantics must be represented.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d94-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f7d94-124">Requirements</span></span>



| <span data-ttu-id="f7d94-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f7d94-125">Requirement</span></span> | <span data-ttu-id="f7d94-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f7d94-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d94-127">Header</span><span class="sxs-lookup"><span data-stu-id="f7d94-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f7d94-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d94-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f7d94-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f7d94-129">Library</span></span><br/> | <dl> <span data-ttu-id="f7d94-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7d94-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f7d94-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7d94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d94-132">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f7d94-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="f7d94-133">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="f7d94-133">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="f7d94-134">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="f7d94-134">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
