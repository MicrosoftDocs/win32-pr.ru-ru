---
title: Структура D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. | Структура D3DX11_IMAGE_LOAD_INFO (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO структура Direct3D 11
- Указатель структуры LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987206"
---
# <a name="d3dx11_image_load_info-structure"></a><span data-ttu-id="a8014-107">\_ \_ \_ Структура сведений о загрузке образа D3DX11</span><span class="sxs-lookup"><span data-stu-id="a8014-107">D3DX11\_IMAGE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="a8014-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="a8014-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="a8014-109">При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур.</span><span class="sxs-lookup"><span data-stu-id="a8014-109">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="a8014-110">Значение D3DX11 \_ по умолчанию для любого из этих параметров приведет к тому, что D3DX будет автоматически использовать значение из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="a8014-110">A value of D3DX11\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8014-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8014-111">Syntax</span></span>


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="a8014-112">Участники</span><span class="sxs-lookup"><span data-stu-id="a8014-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8014-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="a8014-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-115">Целевая Ширина текстуры.</span><span class="sxs-lookup"><span data-stu-id="a8014-115">The target width of the texture.</span></span> <span data-ttu-id="a8014-116">Если фактическая ширина текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую ширину.</span><span class="sxs-lookup"><span data-stu-id="a8014-116">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="a8014-117">**Height**</span><span class="sxs-lookup"><span data-stu-id="a8014-117">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-119">Целевая Высота текстуры.</span><span class="sxs-lookup"><span data-stu-id="a8014-119">The target height of the texture.</span></span> <span data-ttu-id="a8014-120">Если фактическая высота текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую высоту.</span><span class="sxs-lookup"><span data-stu-id="a8014-120">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="a8014-121">**Depth**</span><span class="sxs-lookup"><span data-stu-id="a8014-121">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-122">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-123">Глубина текстуры.</span><span class="sxs-lookup"><span data-stu-id="a8014-123">The depth of the texture.</span></span> <span data-ttu-id="a8014-124">Это относится только к текстурам томов.</span><span class="sxs-lookup"><span data-stu-id="a8014-124">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="a8014-125">**фирстмиплевел**</span><span class="sxs-lookup"><span data-stu-id="a8014-125">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-126">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-127">Уровень mipmap наивысшего разрешения текстуры.</span><span class="sxs-lookup"><span data-stu-id="a8014-127">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="a8014-128">Если это значение больше 0, после загрузки текстуры Фирстмиплевел будет сопоставлен с mipmap уровнем 0.</span><span class="sxs-lookup"><span data-stu-id="a8014-128">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="a8014-129">**миплевелс**</span><span class="sxs-lookup"><span data-stu-id="a8014-129">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-130">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-131">Максимальное число уровней mipmap в текстуре.</span><span class="sxs-lookup"><span data-stu-id="a8014-131">The maximum number of mipmap levels in the texture.</span></span> <span data-ttu-id="a8014-132">См. примечания в разделе [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span><span class="sxs-lookup"><span data-stu-id="a8014-132">See the remarks in [**D3D11\_TEX1D\_SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv).</span></span> <span data-ttu-id="a8014-133">Использование значения 0 или D3DX11 \_ по умолчанию приведет к созданию всей цепочки mipmap.</span><span class="sxs-lookup"><span data-stu-id="a8014-133">Using 0 or D3DX11\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="a8014-134">**Использование**</span><span class="sxs-lookup"><span data-stu-id="a8014-134">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-135">Тип: **[ **\_ Использование D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span><span class="sxs-lookup"><span data-stu-id="a8014-135">Type: **[**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-136">Способ использования ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="a8014-136">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="a8014-137">См. раздел [**\_ Использование D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="a8014-137">See [**D3D11\_USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span>

</dd> <dt>

<span data-ttu-id="a8014-138">**биндфлагс**</span><span class="sxs-lookup"><span data-stu-id="a8014-138">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-139">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-139">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-140">Этапы конвейера, к которым может быть привязана текстура.</span><span class="sxs-lookup"><span data-stu-id="a8014-140">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="a8014-141">См. раздел [**\_ \_ флаг привязки D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="a8014-141">See [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="a8014-142">**кпуакцессфлагс**</span><span class="sxs-lookup"><span data-stu-id="a8014-142">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-143">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-144">Разрешения на доступ, которые будут иметь ЦП для ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="a8014-144">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="a8014-145">См. раздел [**\_ \_ \_ флаг доступа к ЦП D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="a8014-145">See [**D3D11\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="a8014-146">**мискфлагс**</span><span class="sxs-lookup"><span data-stu-id="a8014-146">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-147">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-147">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-148">Прочие свойства ресурсов (см. раздел [**D3D11 \_ Resource, \_ \_ флаг**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="a8014-148">Miscellaneous resource properties (see [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="a8014-149">**Формат**</span><span class="sxs-lookup"><span data-stu-id="a8014-149">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-150">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a8014-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-151">Перечисление [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , указывающее формат, в котором будет располагаться текстура после ее загрузки.</span><span class="sxs-lookup"><span data-stu-id="a8014-151">A [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration indicating the format the texture will be in after it is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a8014-152">**Фильтр**</span><span class="sxs-lookup"><span data-stu-id="a8014-152">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-153">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-153">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-154">Отфильтровать текстуру с помощью указанного фильтра (только при интерполяции).</span><span class="sxs-lookup"><span data-stu-id="a8014-154">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="a8014-155">См [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="a8014-155">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8014-156">**мипфилтер**</span><span class="sxs-lookup"><span data-stu-id="a8014-156">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-157">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8014-157">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8014-158">Фильтрация уровней MIP текстуры с помощью указанного фильтра (только при создании MIP-карты).</span><span class="sxs-lookup"><span data-stu-id="a8014-158">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="a8014-159">Допустимые значения: D3DX11 \_ Filter \_ None, D3DX11 Filter \_ \_ , D3DX11 \_ \_ линейный фильтр или \_ треугольник фильтра D3DX11 \_ .</span><span class="sxs-lookup"><span data-stu-id="a8014-159">Valid values are D3DX11\_FILTER\_NONE, D3DX11\_FILTER\_POINT, D3DX11\_FILTER\_LINEAR, or D3DX11\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="a8014-160">См [**. \_ \_ флаг фильтра D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="a8014-160">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8014-161">**псрЦинфо**</span><span class="sxs-lookup"><span data-stu-id="a8014-161">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="a8014-162">Тип: **[ **\_ \_ сведения об образе D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8014-162">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="a8014-163">Сведения о исходном образе.</span><span class="sxs-lookup"><span data-stu-id="a8014-163">Information about the original image.</span></span> <span data-ttu-id="a8014-164">См [**. \_ \_ сведения об образе D3DX11**](d3dx11-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="a8014-164">See [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md).</span></span> <span data-ttu-id="a8014-165">Можно получить с помощью [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)или [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="a8014-165">Can be obtained with [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md), or [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8014-166">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8014-166">Remarks</span></span>

<span data-ttu-id="a8014-167">При инициализации структуры можно задать любой элемент D3DX11 \_ Default, и D3DX будет инициализировать его со значением по умолчанию из текстуры источника при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="a8014-167">When initializing the structure, you may set any member to D3DX11\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="a8014-168">Эта структура может использоваться интерфейсами API, которые:</span><span class="sxs-lookup"><span data-stu-id="a8014-168">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="a8014-169">Создайте ресурсы, такие как [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) и [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="a8014-169">Create resources, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="a8014-170">Создание обработчиков данных, таких как [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) или [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="a8014-170">Create data processors, such as [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) or [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).</span></span>

<span data-ttu-id="a8014-171">Значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="a8014-171">The default values are:</span></span>


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



<span data-ttu-id="a8014-172">Ниже приведен краткий пример, в котором эта структура используется для предоставления формата пикселей при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="a8014-172">Here is a brief example that uses this structure to supply the pixel format when loading a texture.</span></span> <span data-ttu-id="a8014-173">Полный код см. в разделе HDRFormats10. cpp в [примере HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="a8014-173">For the complete code, see HDRFormats10.cpp in [HDRToneMappingCS11 Sample](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).</span></span>


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a><span data-ttu-id="a8014-174">Требования</span><span class="sxs-lookup"><span data-stu-id="a8014-174">Requirements</span></span>



| <span data-ttu-id="a8014-175">Требование</span><span class="sxs-lookup"><span data-stu-id="a8014-175">Requirement</span></span> | <span data-ttu-id="a8014-176">Значение</span><span class="sxs-lookup"><span data-stu-id="a8014-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8014-177">Header</span><span class="sxs-lookup"><span data-stu-id="a8014-177">Header</span></span><br/> | <dl> <span data-ttu-id="a8014-178"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8014-178"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8014-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8014-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8014-180">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="a8014-180">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

