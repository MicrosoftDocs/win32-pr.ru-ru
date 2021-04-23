---
title: Отправка данных текстуры через буферы
description: Передача данных двухмерной или трехмерной текстуры аналогична передаче данных 1D, за исключением того, что приложениям необходимо обратить особое внимание на выравнивание данных, связанное с шагом строки.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadbd1e71b3c9895b75c973397488472b57f8eb1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549032"
---
# <a name="uploading-texture-data-through-buffers"></a><span data-ttu-id="53dea-103">Отправка данных текстуры через буферы</span><span class="sxs-lookup"><span data-stu-id="53dea-103">Uploading Texture Data Through Buffers</span></span>

<span data-ttu-id="53dea-104">Передача данных двухмерной или трехмерной текстуры аналогична передаче данных 1D, за исключением того, что приложениям необходимо обратить особое внимание на выравнивание данных, связанное с шагом строки.</span><span class="sxs-lookup"><span data-stu-id="53dea-104">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="53dea-105">Буферы можно использовать последовательно и параллельно из нескольких частей графического конвейера, и они являются очень гибкими.</span><span class="sxs-lookup"><span data-stu-id="53dea-105">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span>

-   [<span data-ttu-id="53dea-106">Передача данных текстуры с помощью буферов</span><span class="sxs-lookup"><span data-stu-id="53dea-106">Upload Texture Data via Buffers</span></span>](#upload-texture-data-via-buffers)
-   [<span data-ttu-id="53dea-107">Идет</span><span class="sxs-lookup"><span data-stu-id="53dea-107">Copying</span></span>](#copying)
-   [<span data-ttu-id="53dea-108">Сопоставление и отмена сопоставления</span><span class="sxs-lookup"><span data-stu-id="53dea-108">Mapping and unmapping</span></span>](#mapping-and-unmapping)
-   [<span data-ttu-id="53dea-109">Выравнивание буфера</span><span class="sxs-lookup"><span data-stu-id="53dea-109">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="53dea-110">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="53dea-110">Related topics</span></span>](#related-topics)

## <a name="upload-texture-data-via-buffers"></a><span data-ttu-id="53dea-111">Передача данных текстуры с помощью буферов</span><span class="sxs-lookup"><span data-stu-id="53dea-111">Upload Texture Data via Buffers</span></span>

<span data-ttu-id="53dea-112">Приложения должны передавать данные через [**ID3D12GraphicsCommandList:: копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) или [**ID3D12GraphicsCommandList:: копибуфферрегион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span><span class="sxs-lookup"><span data-stu-id="53dea-112">Applications must upload data via [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span></span> <span data-ttu-id="53dea-113">Данные текстуры, скорее всего, будут более крупными, доступными для многократного доступа и преимуществами улучшенной согласованности в кэше для нелинейных макетов памяти, чем для других данных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53dea-113">Texture data is much more likely to be larger, accessed repeatedly, and benefit from the improved cache-coherency of non-linear memory layouts than other resource data.</span></span> <span data-ttu-id="53dea-114">Когда буферы используются в D3D12, приложения получают полный контроль над размещением и упорядочением данных, связанными с копированием данных ресурсов, при условии, что требования к выравниванию памяти удовлетворяются.</span><span class="sxs-lookup"><span data-stu-id="53dea-114">When buffers are used in D3D12, applications have full control on data placement and arrangement associated with copying resource data around, as long as the memory alignment requirements are satisfied.</span></span>

<span data-ttu-id="53dea-115">Пример демонстрирует, где приложение просто выполняет сведение 2D-данных в 1D перед помещением в буфер.</span><span class="sxs-lookup"><span data-stu-id="53dea-115">The sample highlights where the application simply flattens 2D data into 1D before placing it in the buffer.</span></span> <span data-ttu-id="53dea-116">В случае 2D-сценария mipmap приложение может либо свести каждый дискретными к подресурсу, либо быстро использовать алгоритм подраспределений 1D, или использовать более сложный способ плоского выделения, чтобы свести к минимальному использованию видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="53dea-116">For the mipmap 2D scenario, the application can either flatten each sub-resource discretely and quickly use a 1D sub-allocation algorithm, or, use a more complicated 2D sub-allocation technique to minimize video memory utilization.</span></span> <span data-ttu-id="53dea-117">Первый метод должен использоваться чаще, чем проще.</span><span class="sxs-lookup"><span data-stu-id="53dea-117">The first technique is expected to be used more often as it is simpler.</span></span> <span data-ttu-id="53dea-118">Второй способ может быть полезен при упаковке данных на диск или по сети.</span><span class="sxs-lookup"><span data-stu-id="53dea-118">The second technique may be useful when packing data onto a disk or across a network.</span></span> <span data-ttu-id="53dea-119">В любом случае приложение по-прежнему должно вызывать API копирования для каждого подресурса.</span><span class="sxs-lookup"><span data-stu-id="53dea-119">In either case, the application must still call the copy APIs for each sub-resource.</span></span>

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

<span data-ttu-id="53dea-120">Обратите внимание на использование вспомогательных [**структур \_ CD3DX12 \_ Свойства кучи**](cd3dx12-heap-properties.md) и [**\_ \_ \_ расположения CD3DX12 текстуры**](cd3dx12-texture-copy-location.md), а также методы [**креатекоммиттедресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) и [**копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span><span class="sxs-lookup"><span data-stu-id="53dea-120">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_TEXTURE\_COPY\_LOCATION**](cd3dx12-texture-copy-location.md), and the methods [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) and [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span></span>

## <a name="copying"></a><span data-ttu-id="53dea-121">Копирование</span><span class="sxs-lookup"><span data-stu-id="53dea-121">Copying</span></span>

<span data-ttu-id="53dea-122">Методы D3D12 позволяют приложениям заменять начальные данные D3D11 [**упдатесубресаурце**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**кописубресаурцерегион**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)и Resource.</span><span class="sxs-lookup"><span data-stu-id="53dea-122">D3D12 methods enable applications to replace D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion), and resource initial data.</span></span> <span data-ttu-id="53dea-123">В буферных ресурсах может размещаться один трехмерный подресурс с данными текстуры по строкам.</span><span class="sxs-lookup"><span data-stu-id="53dea-123">A single 3D subresource worth of row-major texture data may be located in buffer resources.</span></span> <span data-ttu-id="53dea-124">[**Копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) может копировать данные текстуры из буфера в ресурс текстуры с неизвестной структурой текстуры и наоборот.</span><span class="sxs-lookup"><span data-stu-id="53dea-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) can copy that texture data from the buffer to a texture resource with an unknown texture layout, and vice versa.</span></span> <span data-ttu-id="53dea-125">Приложения должны предпочесть этот тип приема для заполнения часто используемых ресурсов GPU, создавая большие буферы в куче передачи при создании часто используемых ресурсов GPU в куче по УМОЛЧАНИю без доступа к ЦП.</span><span class="sxs-lookup"><span data-stu-id="53dea-125">Applications should prefer this type of technique to populate frequently accessed GPU resources, by creating large buffers in an UPLOAD heap while creating the frequently accessed GPU resources in a DEFAULT heap that has no CPU access.</span></span> <span data-ttu-id="53dea-126">Такой метод эффективно поддерживает отдельные GPU и их большой объем памяти, недоступной для ЦП, без частого нарушения архитектуры.</span><span class="sxs-lookup"><span data-stu-id="53dea-126">Such a technique efficiently supports discrete GPUs and their large amounts of CPU-inaccessible memory, without commonly impairing UMA architectures.</span></span>

<span data-ttu-id="53dea-127">Обратите внимание на две следующие константы:</span><span class="sxs-lookup"><span data-stu-id="53dea-127">Note the following two constants:</span></span>

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [<span data-ttu-id="53dea-128">**\_Объем ПОДРЕСУРСОВ \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="53dea-128">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [<span data-ttu-id="53dea-129">**D3D12 \_ размещенных \_ подресурсов \_**</span><span class="sxs-lookup"><span data-stu-id="53dea-129">**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [<span data-ttu-id="53dea-130">**\_ \_ Расположение копии текстуры \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="53dea-130">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [<span data-ttu-id="53dea-131">**\_ \_ Тип копирования текстур \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="53dea-131">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [<span data-ttu-id="53dea-132">**ID3D12Device:: GetCopyableFootprints**</span><span class="sxs-lookup"><span data-stu-id="53dea-132">**ID3D12Device::GetCopyableFootprints**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [<span data-ttu-id="53dea-133">**ID3D12GraphicsCommandList:: Копиресаурце**</span><span class="sxs-lookup"><span data-stu-id="53dea-133">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="53dea-134">**ID3D12GraphicsCommandList:: Копитекстуререгион**</span><span class="sxs-lookup"><span data-stu-id="53dea-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="53dea-135">**ID3D12GraphicsCommandList:: Копибуфферрегион**</span><span class="sxs-lookup"><span data-stu-id="53dea-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="53dea-136">**ID3D12GraphicsCommandList:: Копитилес**</span><span class="sxs-lookup"><span data-stu-id="53dea-136">**ID3D12GraphicsCommandList::CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="53dea-137">**ID3D12CommandQueue:: Упдатетилемаппингс**</span><span class="sxs-lookup"><span data-stu-id="53dea-137">**ID3D12CommandQueue::UpdateTileMappings**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a><span data-ttu-id="53dea-138">Сопоставление и отмена сопоставления</span><span class="sxs-lookup"><span data-stu-id="53dea-138">Mapping and unmapping</span></span>

<span data-ttu-id="53dea-139">[**Сопоставление**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) и [**Отмена сопоставления могут**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) безопасно вызываться несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="53dea-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) can be called by multiple threads safely.</span></span> <span data-ttu-id="53dea-140">Первый вызов функции **Map** выделяет диапазон ВИРТУАЛЬНЫХ адресов ЦП для ресурса.</span><span class="sxs-lookup"><span data-stu-id="53dea-140">The first call to **Map** allocates a CPU virtual address range for the resource.</span></span> <span data-ttu-id="53dea-141">Последний вызов метода **сопоставления** освобождает диапазон ВИРТУАЛЬНЫХ адресов ЦП.</span><span class="sxs-lookup"><span data-stu-id="53dea-141">The last call to **Unmap** deallocates the CPU virtual address range.</span></span> <span data-ttu-id="53dea-142">Виртуальный адрес ЦП обычно возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="53dea-142">The CPU virtual address is commonly returned to the application.</span></span>

<span data-ttu-id="53dea-143">Всякий раз, когда данные передаются между ЦП и GPU через ресурсы в кучах реадбакк, для поддержки всех систем, D3D12 поддерживаются, необходимо использовать [**сопоставление**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) и [**сопоставление**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) .</span><span class="sxs-lookup"><span data-stu-id="53dea-143">Whenever data is passed between the CPU and GPU through resources in readback heaps, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) must be used to support all systems D3D12 is supported on.</span></span> <span data-ttu-id="53dea-144">Максимально эффективное поддержание диапазонов в системах, требующих диапазонов (см. [**D3D12 \_ Range**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span><span class="sxs-lookup"><span data-stu-id="53dea-144">Keeping the ranges as tight as possible maximizes efficiency on the systems that require ranges (refer to [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span></span>

<span data-ttu-id="53dea-145">Производительность средств отладки не только заключается в точном использовании диапазонов во всех вызовах [**сопоставления карты**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , но и из приложений, которые отменяют сопоставление ресурсов, когда изменения ЦП больше не будут выполняться.</span><span class="sxs-lookup"><span data-stu-id="53dea-145">The performance of debugging tools benefit not only from the accurate usage of ranges on all [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) calls, but also from applications unmapping resources when CPU modifications will no longer be made.</span></span>

<span data-ttu-id="53dea-146">Метод D3D11 с использованием [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (с набором параметров Discard) для переименования ресурсов не поддерживается в D3D12.</span><span class="sxs-lookup"><span data-stu-id="53dea-146">The D3D11 method of using [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (with the DISCARD parameter set) to rename resources is not supported in D3D12.</span></span> <span data-ttu-id="53dea-147">Приложения должны самостоятельно реализовывать переименование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53dea-147">Applications must implement resource renaming themselves.</span></span> <span data-ttu-id="53dea-148">Все вызовы **карт** неявно не \_ переписываются и многопоточные.</span><span class="sxs-lookup"><span data-stu-id="53dea-148">All **Map** calls are implicitly NO\_OVERWRITE and multi-threaded.</span></span> <span data-ttu-id="53dea-149">Необходимо, чтобы все необходимые действия GPU, содержащиеся в списках команд, были завершены до получения доступа к данным с помощью ЦП.</span><span class="sxs-lookup"><span data-stu-id="53dea-149">It is the application’s responsibility to ensure that any relevant GPU work contained in command lists is finished before the accessing data with the CPU.</span></span> <span data-ttu-id="53dea-150">Вызовы D3D12 для **Map** не выполняют неявное очистку буферов команд и не блокируют ожидание завершения работы GPU.</span><span class="sxs-lookup"><span data-stu-id="53dea-150">D3D12 calls to **Map** do not implicitly flush any command buffers, nor do they block waiting for the GPU to finish work.</span></span> <span data-ttu-id="53dea-151">В результате в некоторых сценариях можно даже оптимизировать **сопоставление** [**и сопоставление**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) .</span><span class="sxs-lookup"><span data-stu-id="53dea-151">As a result, **Map** and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) may even be optimized out in some scenarios.</span></span>

## <a name="buffer-alignment"></a><span data-ttu-id="53dea-152">Выравнивание буфера</span><span class="sxs-lookup"><span data-stu-id="53dea-152">Buffer alignment</span></span>

<span data-ttu-id="53dea-153">Ограничения выравнивания буфера:</span><span class="sxs-lookup"><span data-stu-id="53dea-153">Buffer alignment restrictions:</span></span>

-   <span data-ttu-id="53dea-154">При копировании линейных подресурсов должно быть выравниваться до 512 байт (со высотам строки, выровненной по D3D12у \_ \_ \_ выравнивания по высоте данных текстуры \_ ).</span><span class="sxs-lookup"><span data-stu-id="53dea-154">Linear subresource copying must be aligned to 512 bytes (with the row pitch aligned to D3D12\_TEXTURE\_DATA\_PITCH\_ALIGNMENT bytes).</span></span>
-   <span data-ttu-id="53dea-155">Число константных операций чтения данных должно быть кратно 256 байт от начала кучи (т. е. только по адресам, поддерживающим 256 байт).</span><span class="sxs-lookup"><span data-stu-id="53dea-155">Constant data reads must be a multiple of 256 bytes from the beginning of the heap (i.e. only from addresses that are 256-byte aligned).</span></span>
-   <span data-ttu-id="53dea-156">Считывание данных индекса должно быть кратным размеру типа данных индекса (т. е. только из адресов, которые естественным образом выровнены для данных).</span><span class="sxs-lookup"><span data-stu-id="53dea-156">Index data reads must be a multiple of the index data type size (i.e. only from addresses that are naturally aligned for the data).</span></span>
-   <span data-ttu-id="53dea-157">[**ID3D12GraphicsCommandList::D равинстанцед**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) и [**ID3D12GraphicsCommandList::D равиндексединстанцед**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) данные должны относиться к значениям offset, кратным 4 (т. е. только из адресов, которые имеют выравниваемая по значению DWORD).</span><span class="sxs-lookup"><span data-stu-id="53dea-157">[**ID3D12GraphicsCommandList::DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) and [**ID3D12GraphicsCommandList::DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) data must be from offsets that are multiples of 4 (i.e. only from addresses that are DWORD aligned).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53dea-158">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="53dea-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53dea-159">Подраспределение в буферах</span><span class="sxs-lookup"><span data-stu-id="53dea-159">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 