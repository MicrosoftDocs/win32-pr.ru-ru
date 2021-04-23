---
description: Загрузка текстуры из текстуры.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Функция D3DX10LoadTextureFromTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354433"
---
# <a name="d3dx10loadtexturefromtexture-function"></a><span data-ttu-id="ab81b-103">Функция D3DX10LoadTextureFromTexture</span><span class="sxs-lookup"><span data-stu-id="ab81b-103">D3DX10LoadTextureFromTexture function</span></span>

<span data-ttu-id="ab81b-104">Загрузка текстуры из текстуры.</span><span class="sxs-lookup"><span data-stu-id="ab81b-104">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab81b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab81b-105">Syntax</span></span>


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ab81b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab81b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab81b-107">*псрктекстуре*</span><span class="sxs-lookup"><span data-stu-id="ab81b-107">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="ab81b-108">Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="ab81b-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="ab81b-109">Указатель на исходную текстуру.</span><span class="sxs-lookup"><span data-stu-id="ab81b-109">Pointer to the source texture.</span></span> <span data-ttu-id="ab81b-110">См. [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="ab81b-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="ab81b-111">*плоадинфо*</span><span class="sxs-lookup"><span data-stu-id="ab81b-111">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ab81b-112">Тип: **[ **\_ \_ \_ сведения о загрузке текстуры D3DX10**](d3dx10-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab81b-112">Type: **[**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md)\***</span></span>

<span data-ttu-id="ab81b-113">Указатель на параметры загрузки текстуры.</span><span class="sxs-lookup"><span data-stu-id="ab81b-113">Pointer to texture loading parameters.</span></span> <span data-ttu-id="ab81b-114">См [**. \_ \_ \_ сведения о загрузке текстур D3DX10**](d3dx10-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="ab81b-114">See [**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab81b-115">*пдсттекстуре*</span><span class="sxs-lookup"><span data-stu-id="ab81b-115">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="ab81b-116">Тип: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="ab81b-116">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="ab81b-117">Указатель на текстуру назначения.</span><span class="sxs-lookup"><span data-stu-id="ab81b-117">Pointer to the destination texture.</span></span> <span data-ttu-id="ab81b-118">См. раздел [**интерфейс ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="ab81b-118">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab81b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab81b-119">Return value</span></span>

<span data-ttu-id="ab81b-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab81b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab81b-121">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ab81b-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab81b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ab81b-122">Requirements</span></span>



| <span data-ttu-id="ab81b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ab81b-123">Requirement</span></span> | <span data-ttu-id="ab81b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ab81b-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab81b-125">Header</span><span class="sxs-lookup"><span data-stu-id="ab81b-125">Header</span></span><br/> | <dl> <span data-ttu-id="ab81b-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab81b-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab81b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab81b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab81b-128">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="ab81b-128">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




