---
title: Функция D3DX11LoadTextureFromTexture (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, изменить размер, преобразовать, сжать, распаковать и/или Копиректангле. Загрузка текстуры из текстуры.
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- D3DX11LoadTextureFromTexture функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986996"
---
# <a name="d3dx11loadtexturefromtexture-function"></a><span data-ttu-id="6b9e8-106">Функция D3DX11LoadTextureFromTexture</span><span class="sxs-lookup"><span data-stu-id="6b9e8-106">D3DX11LoadTextureFromTexture function</span></span>

> [!Note]  
> <span data-ttu-id="6b9e8-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="6b9e8-108">Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **изменить размер**, **преобразовать**, **Сжать**, **распаковать** и (или) **копиректангле**.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **Resize**, **Convert**, **Compress**, **Decompress**, and/or **CopyRectangle**.</span></span>

 

<span data-ttu-id="6b9e8-109">Загрузка текстуры из текстуры.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-109">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b9e8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b9e8-110">Syntax</span></span>


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="6b9e8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b9e8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b9e8-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="6b9e8-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9e8-113">Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="6b9e8-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="6b9e8-114">Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="6b9e8-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="6b9e8-115">*псрктекстуре*</span><span class="sxs-lookup"><span data-stu-id="6b9e8-115">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9e8-116">Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="6b9e8-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="6b9e8-117">Указатель на исходную текстуру.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-117">Pointer to the source texture.</span></span> <span data-ttu-id="6b9e8-118">См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="6b9e8-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="6b9e8-119">*плоадинфо*</span><span class="sxs-lookup"><span data-stu-id="6b9e8-119">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9e8-120">Тип: **[ **\_ \_ \_ сведения о загрузке текстуры D3DX11**](d3dx11-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b9e8-120">Type: **[**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md)\***</span></span>

<span data-ttu-id="6b9e8-121">Указатель на параметры загрузки текстуры.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-121">Pointer to texture loading parameters.</span></span> <span data-ttu-id="6b9e8-122">См [**. \_ \_ \_ сведения о загрузке текстур D3DX11**](d3dx11-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="6b9e8-122">See [**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b9e8-123">*пдсттекстуре*</span><span class="sxs-lookup"><span data-stu-id="6b9e8-123">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9e8-124">Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="6b9e8-124">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="6b9e8-125">Указатель на текстуру назначения.</span><span class="sxs-lookup"><span data-stu-id="6b9e8-125">Pointer to the destination texture.</span></span> <span data-ttu-id="6b9e8-126">См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="6b9e8-126">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b9e8-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b9e8-127">Return value</span></span>

<span data-ttu-id="6b9e8-128">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b9e8-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b9e8-129">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6b9e8-129">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b9e8-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6b9e8-130">Requirements</span></span>



| <span data-ttu-id="6b9e8-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6b9e8-131">Requirement</span></span> | <span data-ttu-id="6b9e8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6b9e8-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b9e8-133">Header</span><span class="sxs-lookup"><span data-stu-id="6b9e8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6b9e8-134"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b9e8-134"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6b9e8-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b9e8-135">Library</span></span><br/> | <dl> <span data-ttu-id="6b9e8-136"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b9e8-136"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6b9e8-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b9e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b9e8-138">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="6b9e8-138">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





