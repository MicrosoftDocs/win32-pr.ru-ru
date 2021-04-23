---
description: Использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: Функция D3DXFillVolumeTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de310ee6171924a5d2b61071d47c421739f15833
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674697"
---
# <a name="d3dxfillvolumetexturetx-function"></a><span data-ttu-id="82d79-103">Функция D3DXFillVolumeTextureTX</span><span class="sxs-lookup"><span data-stu-id="82d79-103">D3DXFillVolumeTextureTX function</span></span>

<span data-ttu-id="82d79-104">Использует скомпилированную функцию высокого уровня шейдеров (HLSL) для заполнения каждого шаг текселя каждого уровня mipmap текстуры.</span><span class="sxs-lookup"><span data-stu-id="82d79-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82d79-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="82d79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82d79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d79-107">*птекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82d79-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d79-108">Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="82d79-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="82d79-109">Указатель на объект [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий заполняемую текстуру.</span><span class="sxs-lookup"><span data-stu-id="82d79-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="82d79-110">*птекстурешадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82d79-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82d79-111">Тип: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="82d79-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="82d79-112">Указатель на объект шейдера текстуры [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="82d79-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82d79-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82d79-113">Return value</span></span>

<span data-ttu-id="82d79-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82d79-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82d79-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="82d79-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="82d79-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="82d79-116">If the function fails, the return value can be one of the following:D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="82d79-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82d79-117">Remarks</span></span>

<span data-ttu-id="82d79-118">Цель текстуры должна быть HLSL функцией, которая имеет следующую семантику:</span><span class="sxs-lookup"><span data-stu-id="82d79-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="82d79-119">Один входной параметр должен использовать семантику расположения.</span><span class="sxs-lookup"><span data-stu-id="82d79-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="82d79-120">Один входной параметр должен использовать семантику ПСИЗЕ.</span><span class="sxs-lookup"><span data-stu-id="82d79-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="82d79-121">Функция должна возвращать параметр, который использует семантику цвета.</span><span class="sxs-lookup"><span data-stu-id="82d79-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="82d79-122">Входные параметры могут быть в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="82d79-122">The input parameters can be in any order.</span></span> <span data-ttu-id="82d79-123">Пример см. в разделе [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="82d79-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="82d79-124">Требования</span><span class="sxs-lookup"><span data-stu-id="82d79-124">Requirements</span></span>



| <span data-ttu-id="82d79-125">Требование</span><span class="sxs-lookup"><span data-stu-id="82d79-125">Requirement</span></span> | <span data-ttu-id="82d79-126">Значение</span><span class="sxs-lookup"><span data-stu-id="82d79-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82d79-127">Header</span><span class="sxs-lookup"><span data-stu-id="82d79-127">Header</span></span><br/>  | <dl> <span data-ttu-id="82d79-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="82d79-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="82d79-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82d79-129">Library</span></span><br/> | <dl> <span data-ttu-id="82d79-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82d79-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="82d79-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82d79-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d79-132">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="82d79-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="82d79-133">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="82d79-133">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="82d79-134">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="82d79-134">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
