---
title: Подресурсы (графика Direct3D 12)
description: Описывает разделение ресурса на подресурсы и ссылку на один, несколько или срез подресурсов.
ms.assetid: C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fa8ea0d48fea7ee8e192d9dcf1fe5e3d22423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548984"
---
# <a name="subresources-direct3d-12-graphics"></a><span data-ttu-id="887f2-103">Подресурсы (графика Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="887f2-103">Subresources (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="887f2-104">Описывает разделение ресурса на подресурсы и ссылку на один, несколько или срез подресурсов.</span><span class="sxs-lookup"><span data-stu-id="887f2-104">Describes how a resource is divided into subresources, and how to reference a single, multiple or slice of subresources.</span></span>

-   [<span data-ttu-id="887f2-105">Примеры подресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-105">Example subresources</span></span>](#example-subresources)
    -   [<span data-ttu-id="887f2-106">Индексирование подресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-106">Subresource indexing</span></span>](#subresource-indexing)
    -   [<span data-ttu-id="887f2-107">Срез MIP</span><span class="sxs-lookup"><span data-stu-id="887f2-107">Mip slice</span></span>](#mip-slice)
    -   [<span data-ttu-id="887f2-108">Срез массива</span><span class="sxs-lookup"><span data-stu-id="887f2-108">Array slice</span></span>](#array-slice)
    -   [<span data-ttu-id="887f2-109">Срез плоскости</span><span class="sxs-lookup"><span data-stu-id="887f2-109">Plane slice</span></span>](#plane-slice)
    -   [<span data-ttu-id="887f2-110">Несколько подресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-110">Multiple subresources</span></span>](#multiple-subresources)
-   [<span data-ttu-id="887f2-111">API-интерфейсы подресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-111">Subresource APIs</span></span>](#subresource-apis)
-   [<span data-ttu-id="887f2-112">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="887f2-112">Related topics</span></span>](#related-topics)

## <a name="example-subresources"></a><span data-ttu-id="887f2-113">Примеры подресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-113">Example subresources</span></span>

<span data-ttu-id="887f2-114">Если ресурс содержит буфер, то он просто содержит один подресурс с индексом 0.</span><span class="sxs-lookup"><span data-stu-id="887f2-114">If a resource contains a buffer, then it simply contains one subresource with an index of 0.</span></span> <span data-ttu-id="887f2-115">Если ресурс содержит текстуру (или массив текстуры), то ссылки на подресурсы сложнее.</span><span class="sxs-lookup"><span data-stu-id="887f2-115">If the resource contains a texture (or texture array), then referencing the subresources is more complex.</span></span>

<span data-ttu-id="887f2-116">Некоторые интерфейсы API обращаются ко всему ресурсу (например, к методу [**ID3D12GraphicsCommandList:: копиресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) ), а другие обращаются к части ресурса (например, к методу [**ID3D12Resource:: реадфромсубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) ).</span><span class="sxs-lookup"><span data-stu-id="887f2-116">Some APIs access an entire resource (such as the [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource) method), others access a portion of a resource (for example the [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) method).</span></span> <span data-ttu-id="887f2-117">Методы, обращающиеся к части ресурса, обычно используют описание представления (например, структуру [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) ) для указания подресурсов для доступа.</span><span class="sxs-lookup"><span data-stu-id="887f2-117">The methods that access a portion of a resource generally use a view description (such as the [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv) structure) to specify the subresources to access.</span></span> <span data-ttu-id="887f2-118">Полный список см. в разделе [API-интерфейсы подресурсов](#subresource-apis) .</span><span class="sxs-lookup"><span data-stu-id="887f2-118">Refer to the [Subresource APIs](#subresource-apis) section for a complete list.</span></span>

### <a name="subresource-indexing"></a><span data-ttu-id="887f2-119">Индексирование подресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-119">Subresource indexing</span></span>

<span data-ttu-id="887f2-120">Чтобы индексировать конкретный вложенный ресурс, уровни MIP индексируются Первыми при индексировании каждой записи массива.</span><span class="sxs-lookup"><span data-stu-id="887f2-120">To index a particular subresource, the mip levels are indexed first as each array entry is indexed.</span></span>

![индексирование подресурсов](images/subresource-index.png)

### <a name="mip-slice"></a><span data-ttu-id="887f2-122">Срез MIP</span><span class="sxs-lookup"><span data-stu-id="887f2-122">Mip slice</span></span>

<span data-ttu-id="887f2-123">Срез MIP содержит по одному уровню mipmap для каждой текстуры в массиве, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="887f2-123">A mip slice includes one mipmap level for every texture in an array, as shown in the following image.</span></span>

![срезы MIP подресурсов](images/subresource-mip-slice.png)

### <a name="array-slice"></a><span data-ttu-id="887f2-125">Срез массива</span><span class="sxs-lookup"><span data-stu-id="887f2-125">Array slice</span></span>

<span data-ttu-id="887f2-126">Учитывая массив текстур, каждая текстура с MIP-карты, срез массива включает одну текстуру и все ее MIP уровни, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="887f2-126">Given an array of textures, each texture with mipmaps, an array slice includes one texture and all of its mip levels, as shown in the following image.</span></span>

![срезы массива подресурсов](images/subresource-array-slices.png)

### <a name="plane-slice"></a><span data-ttu-id="887f2-128">Срез плоскости</span><span class="sxs-lookup"><span data-stu-id="887f2-128">Plane slice</span></span>

<span data-ttu-id="887f2-129">Обычно плоские форматы не используются для хранения данных RGBA, но в тех случаях, когда это (возможно, 24 RGB-данные), одна плоскость может представлять красный рисунок, один зеленый и один синий.</span><span class="sxs-lookup"><span data-stu-id="887f2-129">Typically planar formats are not used to store RGBA data, but in the cases where it is (perhaps 24bpp RGB data), one plane could represent the red image, one the green, and one the blue image.</span></span> <span data-ttu-id="887f2-130">Хотя одна плоскость не обязательно является одним цветом, два или более цвета можно объединить в одну плоскость.</span><span class="sxs-lookup"><span data-stu-id="887f2-130">One plane though is not necessarily one color, two or more colors could be combined into one plane.</span></span> <span data-ttu-id="887f2-131">Обычно плоские данные используются для подвыборки Икбкр и Depth-Stencil данных.</span><span class="sxs-lookup"><span data-stu-id="887f2-131">More typically planar data is used for sub-sampled YCbCr and Depth-Stencil data.</span></span> <span data-ttu-id="887f2-132">Depth-Stencil является единственным форматом, который полностью поддерживает MIP-карты, массивы и несколько плоскостей (часто плоскости 0 для глубины и плоскости 1 для набора элементов).</span><span class="sxs-lookup"><span data-stu-id="887f2-132">Depth-Stencil is the only format that fully supports mipmaps, arrays, and multiple planes (often plane 0 for Depth and plane 1 for Stencil).</span></span>

<span data-ttu-id="887f2-133">Ниже показано индексирование подресурсов для массива из двух Depth-Stencil изображений, каждый из которых имеет три уровня MIP.</span><span class="sxs-lookup"><span data-stu-id="887f2-133">The subresource indexing for an array of two Depth-Stencil images, each with three mip levels, is shown below.</span></span>

![индексирование трафаретов глубины](images/depth-stencil-indexing.png)

<span data-ttu-id="887f2-135">Подвыборка Икбкр поддерживает массивы и имеет плоскости, но не поддерживает MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="887f2-135">Sub-sampled YCbCr supports arrays and has planes, but does not support mipmaps.</span></span> <span data-ttu-id="887f2-136">Изображения Икбкр имеют две плоскости: один для светимости (Y), с которой важнее человеческий глаз, и один для чроминанце (как CB, так и CR), который менее чувствителен к человеческим глазу.</span><span class="sxs-lookup"><span data-stu-id="887f2-136">YCbCr images have two planes, one for the luminance (Y) that the human eye is most sensitive to, and one for the chrominance (both Cb, and Cr, interleaved) which the human eye is less sensitive to.</span></span> <span data-ttu-id="887f2-137">Этот формат обеспечивает сжатие значений чроминанце, чтобы сжать изображение, не влияя на светимость, и является распространенным форматом сжатия видео по этой причине, хотя он используется для сжатия изображений по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="887f2-137">This format enables compression of the chrominance values in order to compress an image without affecting the luminance, and is a common video compression format for that reason, although it is used to compress still images.</span></span> <span data-ttu-id="887f2-138">На рисунке ниже показан формат NV12, указывая, что чроминанце был сжат в один квартал разрешения светимости, то есть ширина каждой плоскости идентична, а плоскость чроминанце — половина высоты плоскости освещенности.</span><span class="sxs-lookup"><span data-stu-id="887f2-138">The image below shows the NV12 format, noting the chrominance has been compressed to one quarter of the resolution of the luminance, meaning the width of each plane is identical, and the chrominance plane is half the height of the luminance plane.</span></span> <span data-ttu-id="887f2-139">Плоскости будут индексироваться как подресурсы аналогичным образом Depth-Stencil примере выше.</span><span class="sxs-lookup"><span data-stu-id="887f2-139">The planes would be indexed as subresources in an identical way to the Depth-Stencil example above.</span></span>

![формат NV12](images/ycbcr.png)

<span data-ttu-id="887f2-141">Плоские форматы существовали в Direct3D 11, но отдельные плоскости не могут быть адресованы по отдельности, скажем, для операций копирования или сопоставления.</span><span class="sxs-lookup"><span data-stu-id="887f2-141">Planar formats existed in Direct3D 11, but individual planes could not be addressed individually, say for copy or mapping operations.</span></span> <span data-ttu-id="887f2-142">Это было изменено в Direct3D 12, чтобы каждая плоскость получала свой идентификатор подресурса.</span><span class="sxs-lookup"><span data-stu-id="887f2-142">This was changed in Direct3D 12 so that each plane received its own subresource ID.</span></span> <span data-ttu-id="887f2-143">Сравните два следующих метода для вычисления идентификатора подресурса.</span><span class="sxs-lookup"><span data-stu-id="887f2-143">Compare the following two methods for calculating the subresource ID.</span></span>

<span data-ttu-id="887f2-144">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="887f2-144">Direct3D 11</span></span>

``` syntax
inline UINT D3D11CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT MipLevels )
{
    return MipSlice + (ArraySlice * MipLevels); 
}
```

<span data-ttu-id="887f2-145">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="887f2-145">Direct3D 12</span></span>

``` syntax
inline UINT D3D12CalcSubresource( UINT MipSlice, UINT ArraySlice, UINT PlaneSlice, UINT MipLevels, UINT ArraySize )
{ 
    return MipSlice + (ArraySlice * MipLevels) + (PlaneSlice * MipLevels * ArraySize); 
}
```

<span data-ttu-id="887f2-146">Большинство аппаратных средств предполагает, что память для плоскости N всегда выделяется сразу после плоскости N-1.</span><span class="sxs-lookup"><span data-stu-id="887f2-146">Most hardware assumes that the memory for plane N is always immediately allocated after plane N-1.</span></span>

<span data-ttu-id="887f2-147">Альтернативой использованию подресурсов является то, что приложение может выделить полностью отдельный ресурс на плоскость.</span><span class="sxs-lookup"><span data-stu-id="887f2-147">An alternative to using subresources is that an app could allocate a completely separate resource per plane.</span></span> <span data-ttu-id="887f2-148">В этом случае приложение понимает данные как плоские и использует несколько ресурсов для их представления.</span><span class="sxs-lookup"><span data-stu-id="887f2-148">In this case, the application understands the data is planar and uses multiple resources to represent it.</span></span>

### <a name="multiple-subresources"></a><span data-ttu-id="887f2-149">Несколько подресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-149">Multiple subresources</span></span>

<span data-ttu-id="887f2-150">В представлении "шейдер — ресурс" можно выбрать любую прямоугольную область подресурсов, используя один из срезов, описанных выше, и разумное использование полей в структурах представления (например, [**D3D12 \_ TEX2D \_ array \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), как показано на рисунке.</span><span class="sxs-lookup"><span data-stu-id="887f2-150">A shader-resource view can select any rectangular region of subresources, using one of the slices described above and judicious use of fields in the view structures (such as [**D3D12\_TEX2D\_ARRAY\_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)), as shown in the image.</span></span>

![Выбор нескольких подресурсов](images/subresource-multiple.png)

<span data-ttu-id="887f2-152">Представление визуализации-целевого объекта может использовать только один подресурс или срез MIP и не может включать подресурсы из нескольких срезов MIP.</span><span class="sxs-lookup"><span data-stu-id="887f2-152">A render-target view can only use a single subresource or mip slice and cannot include subresources from more than one mip slice.</span></span> <span data-ttu-id="887f2-153">Это значит, что каждая текстура в представлении целевого объекта должна иметь одинаковый размер.</span><span class="sxs-lookup"><span data-stu-id="887f2-153">That is, every texture in a render-target view must be the same size.</span></span> <span data-ttu-id="887f2-154">В представлении "шейдер — ресурс" можно выбрать любую прямоугольную область подресурсов, как показано на изображении.</span><span class="sxs-lookup"><span data-stu-id="887f2-154">A shader-resource view can select any rectangular region of subresources, as shown in the image.</span></span>

## <a name="subresource-apis"></a><span data-ttu-id="887f2-155">API-интерфейсы подресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-155">Subresource APIs</span></span>

<span data-ttu-id="887f2-156">Следующие API ссылаются и работают с подресурсами:</span><span class="sxs-lookup"><span data-stu-id="887f2-156">The following APIs reference and work with subresources:</span></span>

<span data-ttu-id="887f2-157">Перечисления:</span><span class="sxs-lookup"><span data-stu-id="887f2-157">Enumerations:</span></span>

-   [<span data-ttu-id="887f2-158">**\_ \_ Тип копирования текстур \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="887f2-158">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)

<span data-ttu-id="887f2-159">Следующие структуры содержат индексы *планеслице* , большинство из которых содержат индексы *мипслице* .</span><span class="sxs-lookup"><span data-stu-id="887f2-159">The following structures contain *PlaneSlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="887f2-160">**D3D12 \_ TEX2D \_ РТВ**</span><span class="sxs-lookup"><span data-stu-id="887f2-160">**D3D12\_TEX2D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [<span data-ttu-id="887f2-161">**D3D12 \_ TEX2D \_ array \_ РТВ**</span><span class="sxs-lookup"><span data-stu-id="887f2-161">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="887f2-162">**D3D12 \_ TEX2D \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="887f2-162">**D3D12\_TEX2D\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [<span data-ttu-id="887f2-163">**D3D12 \_ TEX2D \_ массив \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="887f2-163">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="887f2-164">**D3D12 \_ TEX2D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="887f2-164">**D3D12\_TEX2D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [<span data-ttu-id="887f2-165">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="887f2-165">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="887f2-166">Следующие структуры содержат индексы *аррайслице* , большинство из которых содержат индексы *мипслице* .</span><span class="sxs-lookup"><span data-stu-id="887f2-166">The following structures contain *ArraySlice* indexes, most contain *MipSlice* indexes.</span></span>

-   [<span data-ttu-id="887f2-167">**Представление \_ \_ источника данных массива D3D12 TEX1D \_**</span><span class="sxs-lookup"><span data-stu-id="887f2-167">**D3D12\_TEX1D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [<span data-ttu-id="887f2-168">**Представление \_ \_ источника данных массива D3D12 TEX2D \_**</span><span class="sxs-lookup"><span data-stu-id="887f2-168">**D3D12\_TEX2D\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [<span data-ttu-id="887f2-169">**Представление \_ \_ источника данных массива D3D12 TEX2DMS \_**</span><span class="sxs-lookup"><span data-stu-id="887f2-169">**D3D12\_TEX2DMS\_ARRAY\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)
-   [<span data-ttu-id="887f2-170">**D3D12 \_ TEX1D \_ array \_ РТВ**</span><span class="sxs-lookup"><span data-stu-id="887f2-170">**D3D12\_TEX1D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [<span data-ttu-id="887f2-171">**D3D12 \_ TEX2D \_ array \_ РТВ**</span><span class="sxs-lookup"><span data-stu-id="887f2-171">**D3D12\_TEX2D\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [<span data-ttu-id="887f2-172">**D3D12 \_ TEX2DMS \_ array \_ РТВ**</span><span class="sxs-lookup"><span data-stu-id="887f2-172">**D3D12\_TEX2DMS\_ARRAY\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [<span data-ttu-id="887f2-173">**D3D12 \_ TEX1D \_ массив \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="887f2-173">**D3D12\_TEX1D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [<span data-ttu-id="887f2-174">**D3D12 \_ TEX2D \_ массив \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="887f2-174">**D3D12\_TEX2D\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [<span data-ttu-id="887f2-175">**D3D12 \_ TEX2DMS \_ массив \_ SRV**</span><span class="sxs-lookup"><span data-stu-id="887f2-175">**D3D12\_TEX2DMS\_ARRAY\_SRV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [<span data-ttu-id="887f2-176">**D3D12 \_ TEX1D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="887f2-176">**D3D12\_TEX1D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [<span data-ttu-id="887f2-177">**D3D12 \_ TEX2D \_ array \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="887f2-177">**D3D12\_TEX2D\_ARRAY\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)

<span data-ttu-id="887f2-178">Следующие структуры содержат индексы *мипслице* , но ни *Аррайслице* , ни *планеслице* индексы.</span><span class="sxs-lookup"><span data-stu-id="887f2-178">The following structures contain *MipSlice* indexes, but neither *ArraySlice* nor *PlaneSlice* indexes.</span></span>

-   [<span data-ttu-id="887f2-179">**D3D12 \_ TEX1D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="887f2-179">**D3D12\_TEX1D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [<span data-ttu-id="887f2-180">**D3D12 \_ TEX2D \_ DSV**</span><span class="sxs-lookup"><span data-stu-id="887f2-180">**D3D12\_TEX2D\_DSV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [<span data-ttu-id="887f2-181">**D3D12 \_ TEX1D \_ РТВ**</span><span class="sxs-lookup"><span data-stu-id="887f2-181">**D3D12\_TEX1D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [<span data-ttu-id="887f2-182">**D3D12 \_ TEX3D \_ РТВ**</span><span class="sxs-lookup"><span data-stu-id="887f2-182">**D3D12\_TEX3D\_RTV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)
-   [<span data-ttu-id="887f2-183">**D3D12 \_ TEX1D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="887f2-183">**D3D12\_TEX1D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [<span data-ttu-id="887f2-184">**D3D12 \_ TEX3D \_ UAV**</span><span class="sxs-lookup"><span data-stu-id="887f2-184">**D3D12\_TEX3D\_UAV**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

<span data-ttu-id="887f2-185">Следующие структуры также ссылаются на подресурсы:</span><span class="sxs-lookup"><span data-stu-id="887f2-185">The following structures also reference subresources:</span></span>

-   <span data-ttu-id="887f2-186">[**D3D12 \_ УДАЛИТЬ \_ регион**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : структура, используемая при подготовке к отмене ресурса.</span><span class="sxs-lookup"><span data-stu-id="887f2-186">[**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) : a structure used in preparation for discarding a resource.</span></span>
-   <span data-ttu-id="887f2-187">[**D3D12 \_ Размещение размещенных \_ \_ подресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) . добавляет смещение в ресурс к базовому объему.</span><span class="sxs-lookup"><span data-stu-id="887f2-187">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) : adds an offset into a resource to the basic footprint.</span></span>
-   <span data-ttu-id="887f2-188">[**D3D12 \_ \_ \_ Барьер переключения ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : описывает переход подресурсов между различными использованиями (ресурс шейдера, целевой объект прорисовки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="887f2-188">[**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) : describes the transition of subresources between different usages (shader resource, render target, etc.).</span></span>
-   <span data-ttu-id="887f2-189">[**D3D12 \_ \_Данные подресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : данные о подресурсе включают сами данные, а также шаг строки и срез.</span><span class="sxs-lookup"><span data-stu-id="887f2-189">[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) : subresource data includes the data itself, and the row and slice pitch.</span></span>
-   <span data-ttu-id="887f2-190">[**D3D12 \_ \_Занимаемое ПОДресурсом**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) место: формат, ширина, высота, глубина и шаг строки для вложенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="887f2-190">[**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) : a footprint includes the format, width, height, depth and row-pitch of the subresource.</span></span>
-   <span data-ttu-id="887f2-191">[**D3D12 \_ \_Сведения о ПОДресурсе**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : содержит смещение, шаг строки и шаг глубины для вложенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="887f2-191">[**D3D12\_SUBRESOURCE\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info) : contains the offset, row pitch and depth pitch of the subresource.</span></span>
-   <span data-ttu-id="887f2-192">[**D3D12 \_ \_Мозаичное заполнение подресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) . Описание тома подресурсов мозаики (см. раздел [ресурсы для мозаичного размещения томов](volume-tiled-resources.md)).</span><span class="sxs-lookup"><span data-stu-id="887f2-192">[**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) : describes a tiled subresource volume (refer to [Volume Tiled Resources](volume-tiled-resources.md)).</span></span>
-   <span data-ttu-id="887f2-193">[**D3D12 \_ \_ \_ Расположение для копирования текстуры**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : описывает часть текстуры для копирования.</span><span class="sxs-lookup"><span data-stu-id="887f2-193">[**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) : describes a portion of a texture for the purpose of copying.</span></span>
-   <span data-ttu-id="887f2-194">[**D3D12 \_ \_ \_ КООРДИНАТа мозаичного ресурса**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : описывает координаты мозаичного ресурса.</span><span class="sxs-lookup"><span data-stu-id="887f2-194">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : describes the coordinates of a tiled resource.</span></span>

<span data-ttu-id="887f2-195">Методы:</span><span class="sxs-lookup"><span data-stu-id="887f2-195">Methods:</span></span>

-   <span data-ttu-id="887f2-196">[**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : получает сведения о ресурсе, чтобы обеспечить возможность копирования.</span><span class="sxs-lookup"><span data-stu-id="887f2-196">[**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints) : gets information on a resource, to enable a copy to be made.</span></span>
-   <span data-ttu-id="887f2-197">[**ID3D12Device:: жетресаурцетилинг**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : получает сведения о том, как мозаичный ресурс разбивается на плитки.</span><span class="sxs-lookup"><span data-stu-id="887f2-197">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>
-   <span data-ttu-id="887f2-198">[**ID3D12GraphicsCommandList:: ресолвесубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : копирует многовыборочный составной ресурс в многовыборочную подресурс.</span><span class="sxs-lookup"><span data-stu-id="887f2-198">[**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource) : copies a multi-sampled subresource into a non-multi-sampled subresource.</span></span>
-   <span data-ttu-id="887f2-199">[**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : возвращает указатель на указанные данные в ресурсе и запрещает доступ GPU к подресурсу.</span><span class="sxs-lookup"><span data-stu-id="887f2-199">[**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) : returns a pointer to the specified data in the resource, and denies the GPU access to the subresource.</span></span>
-   <span data-ttu-id="887f2-200">[**ID3D12Resource:: реадфромсубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : копирует данные из подресурса или прямоугольной области подресурса.</span><span class="sxs-lookup"><span data-stu-id="887f2-200">[**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) : copies data from a subresource, or a rectangular region of a subresource.</span></span>
-   <span data-ttu-id="887f2-201">[**ID3D12Resource::**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) unmaps: отменяет сопоставление указанного диапазона памяти и делает указатель на ресурс недействительным.</span><span class="sxs-lookup"><span data-stu-id="887f2-201">[**ID3D12Resource::Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) : unmaps the specified range of memory and invalidates the pointer to the resource.</span></span> <span data-ttu-id="887f2-202">Возобновление доступа GPU к подресурсу.</span><span class="sxs-lookup"><span data-stu-id="887f2-202">Reinstates GPU access to the subresource.</span></span>
-   <span data-ttu-id="887f2-203">[**ID3D12Resource:: вритетосубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : копирует данные во подресурс или прямоугольную область подресурса.</span><span class="sxs-lookup"><span data-stu-id="887f2-203">[**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) : copies data to a subresource, or a rectangular region of a subresource.</span></span>

<span data-ttu-id="887f2-204">Текстуры должны находиться в состоянии [**\_ ресурса D3D12 \_ \_ Общее**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) состояние для доступа ЦП через [**вритетосубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) , а [**реадфромсубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) — как юридические, но буферы — нет.</span><span class="sxs-lookup"><span data-stu-id="887f2-204">Textures must be in the [**D3D12\_RESOURCE\_STATE\_COMMON**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) state for CPU access through [**WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource) and [**ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource) to be legal; but buffers do not.</span></span> <span data-ttu-id="887f2-205">Доступ ЦП к ресурсу обычно осуществляется через сопоставление [**сопоставления**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span><span class="sxs-lookup"><span data-stu-id="887f2-205">CPU access to a resource is typically done through [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)/[**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap).</span></span>

## <a name="related-topics"></a><span data-ttu-id="887f2-206">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="887f2-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="887f2-207">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="887f2-207">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 




