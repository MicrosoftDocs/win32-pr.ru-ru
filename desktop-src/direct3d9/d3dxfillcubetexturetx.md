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
ms.openlocfilehash: 95c6d054900f3f4c4710e22c54759161800137c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107672"
---
# <a name="d3dxfillcubetexturetx-function"></a><span data-ttu-id="8d1f1-103">Функция D3DXFillCubeTextureTX</span><span class="sxs-lookup"><span data-stu-id="8d1f1-103">D3DXFillCubeTextureTX function</span></span>

<span data-ttu-id="8d1f1-104">Использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d1f1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d1f1-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="8d1f1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d1f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d1f1-107">*птекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d1f1-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d1f1-108">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="8d1f1-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="8d1f1-109">Указатель на объект [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий заполняемую текстуру.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="8d1f1-110">*птекстурешадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d1f1-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d1f1-111">Тип: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="8d1f1-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="8d1f1-112">Указатель на объект шейдера текстуры [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="8d1f1-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d1f1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d1f1-113">Return value</span></span>

<span data-ttu-id="8d1f1-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d1f1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d1f1-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d1f1-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d1f1-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="8d1f1-117">Remarks</span></span>

<span data-ttu-id="8d1f1-118">Цель текстуры должна быть HLSL функцией, которая имеет следующую семантику:</span><span class="sxs-lookup"><span data-stu-id="8d1f1-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="8d1f1-119">Один входной параметр должен использовать семантику расположения.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="8d1f1-120">Один входной параметр должен использовать семантику ПСИЗЕ.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="8d1f1-121">Функция должна возвращать параметр, который использует семантику цвета.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="8d1f1-122">Входные параметры могут быть в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="8d1f1-122">The input parameters can be in any order.</span></span> <span data-ttu-id="8d1f1-123">Пример см. в разделе [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="8d1f1-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="8d1f1-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8d1f1-124">Requirements</span></span>



| <span data-ttu-id="8d1f1-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8d1f1-125">Requirement</span></span> | <span data-ttu-id="8d1f1-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8d1f1-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1f1-127">Header</span><span class="sxs-lookup"><span data-stu-id="8d1f1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8d1f1-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d1f1-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8d1f1-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d1f1-129">Library</span></span><br/> | <dl> <span data-ttu-id="8d1f1-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d1f1-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8d1f1-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8d1f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d1f1-132">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8d1f1-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="8d1f1-133">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="8d1f1-133">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
