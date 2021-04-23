---
description: При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур. Значение D3DX10 \_ по умолчанию для любого из этих параметров приведет к тому, что D3DX будет автоматически использовать значение из исходного файла.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: Структура D3DX10_IMAGE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713913"
---
# <a name="d3dx10_image_load_info-structure"></a><span data-ttu-id="97605-104">\_ \_ \_ Структура сведений о загрузке образа D3DX10</span><span class="sxs-lookup"><span data-stu-id="97605-104">D3DX10\_IMAGE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="97605-105">При необходимости предоставьте сведения для интерфейсов API загрузчика текстур, чтобы управлять загрузкой текстур.</span><span class="sxs-lookup"><span data-stu-id="97605-105">Optionally provide information to texture loader APIs to control how textures get loaded.</span></span> <span data-ttu-id="97605-106">Значение D3DX10 \_ по умолчанию для любого из этих параметров приведет к тому, что D3DX будет автоматически использовать значение из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="97605-106">A value of D3DX10\_DEFAULT for any of these parameters will cause D3DX to automatically use the value from the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="97605-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97605-107">Syntax</span></span>


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="97605-108">Члены</span><span class="sxs-lookup"><span data-stu-id="97605-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="97605-109">**Width**</span><span class="sxs-lookup"><span data-stu-id="97605-109">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="97605-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-111">Целевая Ширина текстуры.</span><span class="sxs-lookup"><span data-stu-id="97605-111">The target width of the texture.</span></span> <span data-ttu-id="97605-112">Если фактическая ширина текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую ширину.</span><span class="sxs-lookup"><span data-stu-id="97605-112">If the actual width of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target width.</span></span>

</dd> <dt>

<span data-ttu-id="97605-113">**Height**</span><span class="sxs-lookup"><span data-stu-id="97605-113">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="97605-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-115">Целевая Высота текстуры.</span><span class="sxs-lookup"><span data-stu-id="97605-115">The target height of the texture.</span></span> <span data-ttu-id="97605-116">Если фактическая высота текстуры больше или меньше, чем это значение, то текстура будет масштабироваться вверх или вниз, чтобы вместить эту целевую высоту.</span><span class="sxs-lookup"><span data-stu-id="97605-116">If the actual height of the texture is larger or smaller than this value then the texture will be scaled up or down to fit this target height.</span></span>

</dd> <dt>

<span data-ttu-id="97605-117">**Depth**</span><span class="sxs-lookup"><span data-stu-id="97605-117">**Depth**</span></span>
</dt> <dd>

<span data-ttu-id="97605-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-119">Глубина текстуры.</span><span class="sxs-lookup"><span data-stu-id="97605-119">The depth of the texture.</span></span> <span data-ttu-id="97605-120">Это относится только к текстурам томов.</span><span class="sxs-lookup"><span data-stu-id="97605-120">This only applies to volume textures.</span></span>

</dd> <dt>

<span data-ttu-id="97605-121">**фирстмиплевел**</span><span class="sxs-lookup"><span data-stu-id="97605-121">**FirstMipLevel**</span></span>
</dt> <dd>

<span data-ttu-id="97605-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-123">Уровень mipmap наивысшего разрешения текстуры.</span><span class="sxs-lookup"><span data-stu-id="97605-123">The highest resolution mipmap level of the texture.</span></span> <span data-ttu-id="97605-124">Если это значение больше 0, после загрузки текстуры Фирстмиплевел будет сопоставлен с mipmap уровнем 0.</span><span class="sxs-lookup"><span data-stu-id="97605-124">If this is greater than 0, then after the texture is loaded FirstMipLevel will be mapped to mipmap level 0.</span></span>

</dd> <dt>

<span data-ttu-id="97605-125">**миплевелс**</span><span class="sxs-lookup"><span data-stu-id="97605-125">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="97605-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-127">Максимальное число уровней mipmap, которое будет иметь текстура.</span><span class="sxs-lookup"><span data-stu-id="97605-127">The maximum number of mipmap levels that the texture will have.</span></span> <span data-ttu-id="97605-128">Использование значения 0 или D3DX10 \_ по умолчанию приведет к созданию всей цепочки mipmap.</span><span class="sxs-lookup"><span data-stu-id="97605-128">Using 0 or D3DX10\_DEFAULT will cause a full mipmap chain to be created.</span></span>

</dd> <dt>

<span data-ttu-id="97605-129">**Использование**</span><span class="sxs-lookup"><span data-stu-id="97605-129">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="97605-130">Тип: **[ **\_ Использование D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span><span class="sxs-lookup"><span data-stu-id="97605-130">Type: **[**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-131">Способ использования ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="97605-131">The way the texture resource is intended to be used.</span></span> <span data-ttu-id="97605-132">См. раздел [**\_ Использование D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span><span class="sxs-lookup"><span data-stu-id="97605-132">See [**D3D10\_USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

</dd> <dt>

<span data-ttu-id="97605-133">**биндфлагс**</span><span class="sxs-lookup"><span data-stu-id="97605-133">**BindFlags**</span></span>
</dt> <dd>

<span data-ttu-id="97605-134">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-135">Этапы конвейера, к которым может быть привязана текстура.</span><span class="sxs-lookup"><span data-stu-id="97605-135">The pipeline stages that the texture will be allowed to bind to.</span></span> <span data-ttu-id="97605-136">См. раздел [**\_ \_ флаг привязки D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span><span class="sxs-lookup"><span data-stu-id="97605-136">See [**D3D10\_BIND\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).</span></span>

</dd> <dt>

<span data-ttu-id="97605-137">**кпуакцессфлагс**</span><span class="sxs-lookup"><span data-stu-id="97605-137">**CpuAccessFlags**</span></span>
</dt> <dd>

<span data-ttu-id="97605-138">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-138">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-139">Разрешения на доступ, которые будут иметь ЦП для ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="97605-139">The access permissions the cpu will have for the texture resource.</span></span> <span data-ttu-id="97605-140">См. раздел [**\_ \_ \_ флаг доступа к ЦП D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="97605-140">See [**D3D10\_CPU\_ACCESS\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).</span></span>

</dd> <dt>

<span data-ttu-id="97605-141">**мискфлагс**</span><span class="sxs-lookup"><span data-stu-id="97605-141">**MiscFlags**</span></span>
</dt> <dd>

<span data-ttu-id="97605-142">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-143">Прочие свойства ресурсов (см. раздел [**D3D10 \_ Resource, \_ \_ флаг**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span><span class="sxs-lookup"><span data-stu-id="97605-143">Miscellaneous resource properties (see [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).</span></span>

</dd> <dt>

<span data-ttu-id="97605-144">**Формат**</span><span class="sxs-lookup"><span data-stu-id="97605-144">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="97605-145">Тип: **[ **\_ Формат DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="97605-145">Type: **[**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-146">Формат текстуры будет находиться после загрузки.</span><span class="sxs-lookup"><span data-stu-id="97605-146">The format the texture will be in after it is loaded.</span></span> <span data-ttu-id="97605-147">См. раздел [**\_ Формат DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="97605-147">See [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="97605-148">**Фильтр**</span><span class="sxs-lookup"><span data-stu-id="97605-148">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="97605-149">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-149">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-150">Отфильтровать текстуру с помощью указанного фильтра (только при интерполяции).</span><span class="sxs-lookup"><span data-stu-id="97605-150">Filter the texture using the specified filter (only when resampling).</span></span> <span data-ttu-id="97605-151">См [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="97605-151">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="97605-152">**мипфилтер**</span><span class="sxs-lookup"><span data-stu-id="97605-152">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="97605-153">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97605-153">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="97605-154">Фильтрация уровней MIP текстуры с помощью указанного фильтра (только при создании MIP-карты).</span><span class="sxs-lookup"><span data-stu-id="97605-154">Filter the texture mip levels using the specified filter (only if generating mipmaps).</span></span> <span data-ttu-id="97605-155">Допустимые значения: D3DX10 \_ Filter \_ None, D3DX10 Filter \_ \_ , D3DX10 \_ \_ линейный фильтр или \_ треугольник фильтра D3DX10 \_ .</span><span class="sxs-lookup"><span data-stu-id="97605-155">Valid values are D3DX10\_FILTER\_NONE, D3DX10\_FILTER\_POINT, D3DX10\_FILTER\_LINEAR, or D3DX10\_FILTER\_TRIANGLE.</span></span> <span data-ttu-id="97605-156">См [**. \_ \_ флаг фильтра D3DX10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="97605-156">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="97605-157">**псрЦинфо**</span><span class="sxs-lookup"><span data-stu-id="97605-157">**pSrcInfo**</span></span>
</dt> <dd>

<span data-ttu-id="97605-158">Тип: **[ **\_ \_ сведения об образе D3DX10**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="97605-158">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="97605-159">Сведения о исходном образе.</span><span class="sxs-lookup"><span data-stu-id="97605-159">Information about the original image.</span></span> <span data-ttu-id="97605-160">См [**. \_ \_ сведения об образе D3DX10**](d3dx10-image-info.md).</span><span class="sxs-lookup"><span data-stu-id="97605-160">See [**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md).</span></span> <span data-ttu-id="97605-161">Можно получить с помощью [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)или [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span><span class="sxs-lookup"><span data-stu-id="97605-161">Can be obtained with [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md), or [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97605-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97605-162">Remarks</span></span>

<span data-ttu-id="97605-163">При инициализации структуры можно задать любой элемент D3DX10 \_ Default, и D3DX будет инициализировать его со значением по умолчанию из текстуры источника при загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="97605-163">When initializing the structure, you may set any member to D3DX10\_DEFAULT and D3DX will initialize it with a default value from the source texture when the texture is loaded.</span></span>

<span data-ttu-id="97605-164">Эта структура может использоваться интерфейсами API, которые:</span><span class="sxs-lookup"><span data-stu-id="97605-164">This structure can be used by APIs that:</span></span>

-   <span data-ttu-id="97605-165">Создайте ресурсы, такие как [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) и [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span><span class="sxs-lookup"><span data-stu-id="97605-165">Create resources, such as [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).</span></span>
-   <span data-ttu-id="97605-166">Создание обработчиков данных, таких как [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) или [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="97605-166">Create data processors, such as [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) or [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97605-167">Требования</span><span class="sxs-lookup"><span data-stu-id="97605-167">Requirements</span></span>



| <span data-ttu-id="97605-168">Требование</span><span class="sxs-lookup"><span data-stu-id="97605-168">Requirement</span></span> | <span data-ttu-id="97605-169">Значение</span><span class="sxs-lookup"><span data-stu-id="97605-169">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97605-170">Header</span><span class="sxs-lookup"><span data-stu-id="97605-170">Header</span></span><br/> | <dl> <span data-ttu-id="97605-171"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="97605-171"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97605-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97605-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97605-173">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="97605-173">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
