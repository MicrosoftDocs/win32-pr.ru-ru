---
title: Функция D3DX11SaveTextureToFile (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать библиотеку Директкстекс, Каптуретекстуре затем Саветоксксксфиле (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр). Для упрощенного сценария создания снимка экрана из текстуры цели рендеринга рекомендуется использовать библиотеку Директкстк, Саведдстекстуретофиле или Савевиктекстуретофиле. Сохранение текстуры в файл.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- D3DX11SaveTextureToFile функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986990"
---
# <a name="d3dx11savetexturetofile-function"></a><span data-ttu-id="01aef-107">Функция D3DX11SaveTextureToFile</span><span class="sxs-lookup"><span data-stu-id="01aef-107">D3DX11SaveTextureToFile function</span></span>

> [!Note]  
> <span data-ttu-id="01aef-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="01aef-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="01aef-109">Вместо использования этой функции рекомендуется использовать библиотеку [директкстекс](https://github.com/Microsoft/DirectXTex) , **каптуретекстуре** затем **саветоксксксфиле** (где XXX — это WIC, DDS или TGA; WIC не поддерживает DDS и TGA; D3DX 9 поддерживается TGA как общий формат исходного кода для игр).</span><span class="sxs-lookup"><span data-stu-id="01aef-109">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="01aef-110">Для упрощенного сценария создания снимка экрана из текстуры цели рендеринга рекомендуется использовать библиотеку [директкстк](https://github.com/Microsoft/DirectXTK) , **саведдстекстуретофиле** или **савевиктекстуретофиле**.</span><span class="sxs-lookup"><span data-stu-id="01aef-110">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SaveDDSTextureToFile** or **SaveWICTextureToFile**.</span></span>

 

<span data-ttu-id="01aef-111">Сохранение текстуры в файл.</span><span class="sxs-lookup"><span data-stu-id="01aef-111">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="01aef-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01aef-112">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="01aef-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="01aef-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01aef-114">*pContext*</span><span class="sxs-lookup"><span data-stu-id="01aef-114">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="01aef-115">Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="01aef-115">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="01aef-116">Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="01aef-116">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="01aef-117">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01aef-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01aef-118">Тип: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="01aef-118">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="01aef-119">Указатель на текстуру, которую необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="01aef-119">Pointer to the texture to be saved.</span></span> <span data-ttu-id="01aef-120">См. [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="01aef-120">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="01aef-121">*Дестформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01aef-121">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01aef-122">Тип: **[ **D3DX11 \_ image \_ File \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="01aef-122">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="01aef-123">Формат текстуры будет сохранен как (см. раздел [**\_ \_ \_ Формат файла изображения D3DX11**](d3dx11-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="01aef-123">The format the texture will be saved as (see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)).</span></span> <span data-ttu-id="01aef-124">D3DX11 \_ одиночная \_ DDS — это предпочтительный формат, так как это единственный вариант, поддерживающий все форматы [**в \_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="01aef-124">D3DX11\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="01aef-125">*пдестфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01aef-125">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01aef-126">Тип: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="01aef-126">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="01aef-127">Имя целевого выходного файла, в котором будет сохранена текстура.</span><span class="sxs-lookup"><span data-stu-id="01aef-127">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="01aef-128">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="01aef-128">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="01aef-129">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="01aef-129">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01aef-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01aef-130">Return value</span></span>

<span data-ttu-id="01aef-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01aef-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01aef-132">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md). Используйте возвращаемое значение, чтобы узнать, поддерживается ли *дестформат* .</span><span class="sxs-lookup"><span data-stu-id="01aef-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="01aef-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="01aef-133">Remarks</span></span>

<span data-ttu-id="01aef-134">**D3DX11SaveTextureToFile** записывает дополнительную [**\_ \_ DXT10 структуру заголовков DDS**](/windows/desktop/direct3ddds/dds-header-dxt10) для текстуры ввода, только если это необходимо (например, поскольку текстура ввода имеет стандартный RGB-формат (sRGB)).</span><span class="sxs-lookup"><span data-stu-id="01aef-134">**D3DX11SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="01aef-135">Если **D3DX11SaveTextureToFile** записывает **\_ \_ DXT10 структуру заголовков DDS** , он устанавливает для текстуры **двфауркк** член в структуре [**\_ PIXELFORMAT DDS**](/windows/desktop/direct3ddds/dds-pixelformat) **, чтобы указать** содержимым DX10 в заголовке **DDS \_ \_ пресценсе** расширенный заголовок.</span><span class="sxs-lookup"><span data-stu-id="01aef-135">If **D3DX11SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="01aef-136">Требования</span><span class="sxs-lookup"><span data-stu-id="01aef-136">Requirements</span></span>



| <span data-ttu-id="01aef-137">Требование</span><span class="sxs-lookup"><span data-stu-id="01aef-137">Requirement</span></span> | <span data-ttu-id="01aef-138">Значение</span><span class="sxs-lookup"><span data-stu-id="01aef-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01aef-139">Header</span><span class="sxs-lookup"><span data-stu-id="01aef-139">Header</span></span><br/>  | <dl> <span data-ttu-id="01aef-140"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="01aef-140"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="01aef-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="01aef-141">Library</span></span><br/> | <dl> <span data-ttu-id="01aef-142"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01aef-142"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="01aef-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01aef-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01aef-144">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="01aef-144">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

