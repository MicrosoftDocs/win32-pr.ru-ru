---
title: Структура DDS_HEADER_DXT10 (DDS. h)
description: Расширение заголовков DDS для обработки массивов ресурсов, форматов пикселей DXGI, которые не соответствуют устаревшим структурам формата пикселей Microsoft DirectDraw, и дополнительным метаданным.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS структуры DDS_HEADER_DXT10
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713531"
---
# <a name="dds_header_dxt10-structure"></a><span data-ttu-id="78770-104">\_Структура DXT10 заголовков DDS \_</span><span class="sxs-lookup"><span data-stu-id="78770-104">DDS\_HEADER\_DXT10 structure</span></span>

<span data-ttu-id="78770-105">Расширение заголовков DDS для обработки массивов ресурсов, форматов пикселей DXGI, которые не соответствуют устаревшим структурам формата пикселей Microsoft DirectDraw, и дополнительным метаданным.</span><span class="sxs-lookup"><span data-stu-id="78770-105">DDS header extension to handle resource arrays, DXGI pixel formats that don't map to the legacy Microsoft DirectDraw pixel format structures, and additional metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="78770-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78770-106">Syntax</span></span>


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a><span data-ttu-id="78770-107">Члены</span><span class="sxs-lookup"><span data-stu-id="78770-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="78770-108">**дксгиформат**</span><span class="sxs-lookup"><span data-stu-id="78770-108">**dxgiFormat**</span></span>
</dt> <dd>

<span data-ttu-id="78770-109">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="78770-109">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

</dd> <dd>

<span data-ttu-id="78770-110">Формат пиксельной области (см [**. \_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="78770-110">The surface pixel format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span>

</dd> <dt>

<span data-ttu-id="78770-111">**ресаурцедименсион**</span><span class="sxs-lookup"><span data-stu-id="78770-111">**resourceDimension**</span></span>
</dt> <dd>

<span data-ttu-id="78770-112">Тип: **[ **D3D10 \_ ресурс \_ измерение**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span><span class="sxs-lookup"><span data-stu-id="78770-112">Type: **[**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**</span></span>

</dd> <dd>

<span data-ttu-id="78770-113">Определяет тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="78770-113">Identifies the type of resource.</span></span> <span data-ttu-id="78770-114">Следующие значения для этого элемента являются подмножеством значений в перечислении [**измерений \_ ресурсов \_ D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) или [**D3D11 \_ \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) .</span><span class="sxs-lookup"><span data-stu-id="78770-114">The following values for this member are a subset of the values in the [**D3D10\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) or [**D3D11\_RESOURCE\_DIMENSION**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) enumeration:</span></span>



| <span data-ttu-id="78770-115">Тип</span><span class="sxs-lookup"><span data-stu-id="78770-115">Type</span></span>                                                              | <span data-ttu-id="78770-116">Описание</span><span class="sxs-lookup"><span data-stu-id="78770-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="78770-117">Значение</span><span class="sxs-lookup"><span data-stu-id="78770-117">Value</span></span> |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="78770-118">\_TEXTURE1D измерения DDS \_ (D3D10 \_ ресурсов \_ измерения \_ TEXTURE1D)</span><span class="sxs-lookup"><span data-stu-id="78770-118">DDS\_DIMENSION\_TEXTURE1D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE1D)</span></span> | <span data-ttu-id="78770-119">Ресурс является [одномерной текстурой](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span><span class="sxs-lookup"><span data-stu-id="78770-119">Resource is a [1D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types).</span></span> <span data-ttu-id="78770-120">Элемент **дввидс** в [**\_ заголовке DDS**](dds-header.md) определяет размер текстуры.</span><span class="sxs-lookup"><span data-stu-id="78770-120">The **dwWidth** member of [**DDS\_HEADER**](dds-header.md) specifies the size of the texture.</span></span> <span data-ttu-id="78770-121">Как правило, для элемента **двхеигхт** в **\_ заголовке DDS** устанавливается значение 1. Кроме того, необходимо задать \_ флаг высоты ддсд  в элементе dwFlags **\_ заголовка DDS**.</span><span class="sxs-lookup"><span data-stu-id="78770-121">Typically, you set the **dwHeight** member of **DDS\_HEADER** to 1; you also must set the DDSD\_HEIGHT flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                      | <span data-ttu-id="78770-122">2</span><span class="sxs-lookup"><span data-stu-id="78770-122">2</span></span>     |
| <span data-ttu-id="78770-123">\_TEXTURE2D измерения DDS \_ (D3D10 \_ ресурсов \_ измерения \_ TEXTURE2D)</span><span class="sxs-lookup"><span data-stu-id="78770-123">DDS\_DIMENSION\_TEXTURE2D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE2D)</span></span> | <span data-ttu-id="78770-124">Ресурс — это [двухмерная текстура](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) с областью, заданной членами **дввидс** и **Двхеигхт** в [**\_ заголовке DDS**](dds-header.md).</span><span class="sxs-lookup"><span data-stu-id="78770-124">Resource is a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with an area specified by the **dwWidth** and **dwHeight** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="78770-125">Этот тип также можно использовать для распознавания текстуры на карте Куба.</span><span class="sxs-lookup"><span data-stu-id="78770-125">You can also use this type to identify a cube-map texture.</span></span> <span data-ttu-id="78770-126">Дополнительные сведения о том, как определить текстуру схемы куба, см. в разделе **мискфлаг** and **размера массива** Members.</span><span class="sxs-lookup"><span data-stu-id="78770-126">For more information about how to identify a cube-map texture, see **miscFlag** and **arraySize** members.</span></span> | <span data-ttu-id="78770-127">3</span><span class="sxs-lookup"><span data-stu-id="78770-127">3</span></span>     |
| <span data-ttu-id="78770-128">\_TEXTURE3D измерения DDS \_ (D3D10 \_ ресурсов \_ измерения \_ TEXTURE3D)</span><span class="sxs-lookup"><span data-stu-id="78770-128">DDS\_DIMENSION\_TEXTURE3D (D3D10\_RESOURCE\_DIMENSION\_TEXTURE3D)</span></span> | <span data-ttu-id="78770-129">Ресурс — это [трехмерная текстура](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) с томом, указанным в [**\_ заголовке DDS**](dds-header.md) **дввидс**, **двхеигхт** и **двдепс** .</span><span class="sxs-lookup"><span data-stu-id="78770-129">Resource is a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) with a volume specified by the **dwWidth**, **dwHeight**, and **dwDepth** members of [**DDS\_HEADER**](dds-header.md).</span></span> <span data-ttu-id="78770-130">Также необходимо задать \_ флаг глубины ддсд в элементе **DwFlags** **\_ заголовка DDS**.</span><span class="sxs-lookup"><span data-stu-id="78770-130">You also must set the DDSD\_DEPTH flag in the **dwFlags** member of **DDS\_HEADER**.</span></span>                                                                   | <span data-ttu-id="78770-131">4</span><span class="sxs-lookup"><span data-stu-id="78770-131">4</span></span>     |



 

</dd> <dt>

<span data-ttu-id="78770-132">**мискфлаг**</span><span class="sxs-lookup"><span data-stu-id="78770-132">**miscFlag**</span></span>
</dt> <dd>

<span data-ttu-id="78770-133">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="78770-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="78770-134">Определяет другие, менее распространенные параметры для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78770-134">Identifies other, less common options for resources.</span></span> <span data-ttu-id="78770-135">Следующее значение для этого элемента является подмножеством значений в перечислении [**\_ \_ \_ флагов**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) [**\_ ресурсов \_ \_ D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) или D3D11 ресурса.</span><span class="sxs-lookup"><span data-stu-id="78770-135">The following value for this member is a subset of the values in the [**D3D10\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) or [**D3D11\_RESOURCE\_MISC\_FLAG**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration:</span></span>



| <span data-ttu-id="78770-136">Тип</span><span class="sxs-lookup"><span data-stu-id="78770-136">Type</span></span>                             | <span data-ttu-id="78770-137">Описание</span><span class="sxs-lookup"><span data-stu-id="78770-137">Description</span></span>                                                                                                  | <span data-ttu-id="78770-138">Значение</span><span class="sxs-lookup"><span data-stu-id="78770-138">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="78770-139">\_ресурс DDS \_ \_ текстурекубе</span><span class="sxs-lookup"><span data-stu-id="78770-139">DDS\_RESOURCE\_MISC\_TEXTURECUBE</span></span> | <span data-ttu-id="78770-140">Указывает, что [двухмерная текстура](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) является текстурой схемы куба.</span><span class="sxs-lookup"><span data-stu-id="78770-140">Indicates a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) is a cube-map texture.</span></span> | <span data-ttu-id="78770-141">0x4</span><span class="sxs-lookup"><span data-stu-id="78770-141">0x4</span></span>   |



 

</dd> <dt>

<span data-ttu-id="78770-142">**Размера массива**</span><span class="sxs-lookup"><span data-stu-id="78770-142">**arraySize**</span></span>
</dt> <dd>

<span data-ttu-id="78770-143">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="78770-143">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="78770-144">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="78770-144">The number of elements in the array.</span></span>

<span data-ttu-id="78770-145">Для [двухмерной текстуры](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) , которая также является текстурой схемы куба, это число представляет число кубов.</span><span class="sxs-lookup"><span data-stu-id="78770-145">For a [2D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) that is also a cube-map texture, this number represents the number of cubes.</span></span> <span data-ttu-id="78770-146">Это число совпадает с числом в **нумкубес** члене [**D3D10 \_ Текскубе \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) или [**D3D11 \_ текскубе \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span><span class="sxs-lookup"><span data-stu-id="78770-146">This number is the same as the number in the **NumCubes** member of [**D3D10\_TEXCUBE\_ARRAY\_SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) or [**D3D11\_TEXCUBE\_ARRAY\_SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)).</span></span> <span data-ttu-id="78770-147">В этом случае файл DDS содержит двумерные текстуры **размера массива** \* 6.</span><span class="sxs-lookup"><span data-stu-id="78770-147">In this case, the DDS file contains **arraySize**\*6 2D textures.</span></span> <span data-ttu-id="78770-148">Дополнительные сведения об этом случае см. в описании **мискфлаг** .</span><span class="sxs-lookup"><span data-stu-id="78770-148">For more information about this case, see the **miscFlag** description.</span></span>

<span data-ttu-id="78770-149">Для [трехмерной текстуры](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)это число необходимо задать равным 1.</span><span class="sxs-lookup"><span data-stu-id="78770-149">For a [3D texture](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), you must set this number to 1.</span></span>

</dd> <dt>

<span data-ttu-id="78770-150">**miscFlags2**</span><span class="sxs-lookup"><span data-stu-id="78770-150">**miscFlags2**</span></span>
</dt> <dd>

<span data-ttu-id="78770-151">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="78770-151">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="78770-152">Содержит дополнительные метаданные (ранее зарезервированные).</span><span class="sxs-lookup"><span data-stu-id="78770-152">Contains additional metadata (formerly was reserved).</span></span> <span data-ttu-id="78770-153">Младшие 3 бита указывают режим альфа связанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="78770-153">The lower 3 bits indicate the alpha mode of the associated resource.</span></span> <span data-ttu-id="78770-154">Верхние 29 битов зарезервированы и обычно равны 0.</span><span class="sxs-lookup"><span data-stu-id="78770-154">The upper 29 bits are reserved and are typically 0.</span></span>



| <span data-ttu-id="78770-155">Тип</span><span class="sxs-lookup"><span data-stu-id="78770-155">Type</span></span>                            | <span data-ttu-id="78770-156">Описание</span><span class="sxs-lookup"><span data-stu-id="78770-156">Description</span></span>                                                                                                                              | <span data-ttu-id="78770-157">Значение</span><span class="sxs-lookup"><span data-stu-id="78770-157">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="78770-158">\_режим альфа-канала DDS \_ \_ неизвестен</span><span class="sxs-lookup"><span data-stu-id="78770-158">DDS\_ALPHA\_MODE\_UNKNOWN</span></span>       | <span data-ttu-id="78770-159">Неизвестное содержимое альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="78770-159">Alpha channel content is unknown.</span></span> <span data-ttu-id="78770-160">Это значение для устаревших файлов, которое обычно предполагается "прямым" альфа-каналом.</span><span class="sxs-lookup"><span data-stu-id="78770-160">This is the value for legacy files, which typically is assumed to be 'straight' alpha.</span></span>                 | <span data-ttu-id="78770-161">0x0</span><span class="sxs-lookup"><span data-stu-id="78770-161">0x0</span></span>   |
| <span data-ttu-id="78770-162">\_режим альфа-канала DDS \_ \_</span><span class="sxs-lookup"><span data-stu-id="78770-162">DDS\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="78770-163">Предполагается, что любое содержимое альфа-канала использует прямую альфа.</span><span class="sxs-lookup"><span data-stu-id="78770-163">Any alpha channel content is presumed to use straight alpha.</span></span>                                                                             | <span data-ttu-id="78770-164">0x1</span><span class="sxs-lookup"><span data-stu-id="78770-164">0x1</span></span>   |
| <span data-ttu-id="78770-165">предварительно \_ \_ умноженный режим альфа-канала DDS \_</span><span class="sxs-lookup"><span data-stu-id="78770-165">DDS\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="78770-166">Любое содержимое альфа-канала использует предварительно умноженное альфа.</span><span class="sxs-lookup"><span data-stu-id="78770-166">Any alpha channel content is using premultiplied alpha.</span></span> <span data-ttu-id="78770-167">Единственными форматами файлов прежних версий, которые указывают на эти данные, являются "DX2" и "DX4".</span><span class="sxs-lookup"><span data-stu-id="78770-167">The only legacy file formats that indicate this information are 'DX2' and 'DX4'.</span></span> | <span data-ttu-id="78770-168">0x2</span><span class="sxs-lookup"><span data-stu-id="78770-168">0x2</span></span>   |
| <span data-ttu-id="78770-169">\_непрозрачный режим альфа-канала DDS \_ \_</span><span class="sxs-lookup"><span data-stu-id="78770-169">DDS\_ALPHA\_MODE\_OPAQUE</span></span>        | <span data-ttu-id="78770-170">Все содержимое альфа-канала имеет значение полностью непрозрачно.</span><span class="sxs-lookup"><span data-stu-id="78770-170">Any alpha channel content is all set to fully opaque.</span></span>                                                                                    | <span data-ttu-id="78770-171">0x3</span><span class="sxs-lookup"><span data-stu-id="78770-171">0x3</span></span>   |
| <span data-ttu-id="78770-172">\_ \_ Пользовательский режим набора DDS Alpha \_</span><span class="sxs-lookup"><span data-stu-id="78770-172">DDS\_ALPHA\_MODE\_CUSTOM</span></span>        | <span data-ttu-id="78770-173">Любое содержимое альфа-канала используется в качестве 4-го канала и не предназначено для представления прозрачности (с прямым или предварительным умножением).</span><span class="sxs-lookup"><span data-stu-id="78770-173">Any alpha channel content is being used as a 4th channel and is not intended to represent transparency (straight or premultiplied).</span></span>      | <span data-ttu-id="78770-174">0x4</span><span class="sxs-lookup"><span data-stu-id="78770-174">0x4</span></span>   |



 

> [!Note]  
> <span data-ttu-id="78770-175">Устаревшие библиотеки служебной программы D3DX 10 и [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) не смогут загрузить какие бы то ни было. Файл DDS с **miscFlags2** не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="78770-175">The legacy D3DX 10 and [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) utility libraries will fail to load any .DDS file with **miscFlags2** not equal to zero.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78770-176">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78770-176">Remarks</span></span>

<span data-ttu-id="78770-177">Используйте эту структуру вместе с [**\_ заголовком DDS**](dds-header.md) для хранения массива ресурсов в файле DDS.</span><span class="sxs-lookup"><span data-stu-id="78770-177">Use this structure together with a [**DDS\_HEADER**](dds-header.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="78770-178">Дополнительные сведения см. в разделе [массивы текстур](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="78770-178">For more info, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="78770-179">Этот заголовок отображается, если элемент **двфауркк** структуры [**DDS \_ PIXELFORMAT**](dds-pixelformat.md) имеет значение "содержимым DX10".</span><span class="sxs-lookup"><span data-stu-id="78770-179">This header is present if the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](dds-pixelformat.md) structure is set to 'DX10'.</span></span>

## <a name="requirements"></a><span data-ttu-id="78770-180">Требования</span><span class="sxs-lookup"><span data-stu-id="78770-180">Requirements</span></span>



| <span data-ttu-id="78770-181">Требование</span><span class="sxs-lookup"><span data-stu-id="78770-181">Requirement</span></span> | <span data-ttu-id="78770-182">Значение</span><span class="sxs-lookup"><span data-stu-id="78770-182">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78770-183">Header</span><span class="sxs-lookup"><span data-stu-id="78770-183">Header</span></span><br/> | <dl> <span data-ttu-id="78770-184"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="78770-184"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78770-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78770-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78770-186">Справочник по DDS</span><span class="sxs-lookup"><span data-stu-id="78770-186">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

