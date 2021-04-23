---
title: D2D с использованием D3D11on12
description: В примере D3D1211on12 показано, как визуализировать содержимое D2D через D3D12 содержимое путем совместного использования ресурсов между устройством на базе 11 и устройством на 12 устройств.
ms.assetid: FAEF1412-053C-4B5F-80FA-85396C2586B4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18399b85499787f74dab725d562b6a299878b35
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104549051"
---
# <a name="d2d-using-d3d11on12"></a><span data-ttu-id="53635-103">D2D с использованием D3D11on12</span><span class="sxs-lookup"><span data-stu-id="53635-103">D2D using D3D11on12</span></span>

<span data-ttu-id="53635-104">В примере **D3D1211on12** показано, как ВИЗУАЛИЗИРОВАТЬ содержимое D2D через D3D12 содержимое путем совместного использования ресурсов между устройством на базе 11 и устройством на 12 устройств.</span><span class="sxs-lookup"><span data-stu-id="53635-104">The **D3D1211on12** sample demonstrates how to render D2D content over D3D12 content by sharing resources between an 11 based device and a 12 based device.</span></span>

-   [<span data-ttu-id="53635-105">Создание ID3D11On12Device</span><span class="sxs-lookup"><span data-stu-id="53635-105">Create an ID3D11On12Device</span></span>](#create-an-id3d11on12device)
-   [<span data-ttu-id="53635-106">Создание фабрики D2D</span><span class="sxs-lookup"><span data-stu-id="53635-106">Create a D2D factory</span></span>](#create-a-d2d-factory)
-   [<span data-ttu-id="53635-107">Создание целевого объекта отрисовки для D2D</span><span class="sxs-lookup"><span data-stu-id="53635-107">Create a render target for D2D</span></span>](#create-a-render-target-for-d2d)
-   [<span data-ttu-id="53635-108">Создание базовых текстовых объектов D2D</span><span class="sxs-lookup"><span data-stu-id="53635-108">Create basic D2D text objects</span></span>](#create-basic-d2d-text-objects)
-   [<span data-ttu-id="53635-109">Обновление основного цикла рендеринга</span><span class="sxs-lookup"><span data-stu-id="53635-109">Updating the main render loop</span></span>](#updating-the-main-render-loop)
-   [<span data-ttu-id="53635-110">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="53635-110">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="53635-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="53635-111">Related topics</span></span>](#related-topics)

## <a name="create-an-id3d11on12device"></a><span data-ttu-id="53635-112">Создание ID3D11On12Device</span><span class="sxs-lookup"><span data-stu-id="53635-112">Create an ID3D11On12Device</span></span>

<span data-ttu-id="53635-113">Первым шагом является создание [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) после создания [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) , который включает создание [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , заключенного в оболочку **ID3D12Device** через API-интерфейс [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice).</span><span class="sxs-lookup"><span data-stu-id="53635-113">The first step is to create an [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) after the [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) has been created, which involves creating an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) that is wrapped around the **ID3D12Device** via the API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice).</span></span> <span data-ttu-id="53635-114">Этот API также использует, помимо прочих параметров, [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) , чтобы устройство 11On12 могла отправлять свои команды.</span><span class="sxs-lookup"><span data-stu-id="53635-114">This API also takes in, among other parameters, an [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) so that the 11On12 device can submit its commands.</span></span> <span data-ttu-id="53635-115">После создания **ID3D11Device** можно запросить от него интерфейс **ID3D11On12Device** .</span><span class="sxs-lookup"><span data-stu-id="53635-115">After the **ID3D11Device** is created, you can query the **ID3D11On12Device** interface from it.</span></span> <span data-ttu-id="53635-116">Это основной объект устройства, который будет использоваться для настройки D2D.</span><span class="sxs-lookup"><span data-stu-id="53635-116">This is the primary device object that will be used to set up D2D.</span></span>

<span data-ttu-id="53635-117">В методе **лоадпипелине** Настройте устройства.</span><span class="sxs-lookup"><span data-stu-id="53635-117">In the **LoadPipeline** method, setup the devices.</span></span>

``` syntax
 // Create an 11 device wrapped around the 12 device and share
    // 12's command queue.
    ComPtr<ID3D11Device> d3d11Device;
    ThrowIfFailed(D3D11On12CreateDevice(
        m_d3d12Device.Get(),
        d3d11DeviceFlags,
        nullptr,
        0,
        reinterpret_cast<IUnknown**>(m_commandQueue.GetAddressOf()),
        1,
        0,
        &d3d11Device,
        &m_d3d11DeviceContext,
        nullptr
        ));

    // Query the 11On12 device from the 11 device.
    ThrowIfFailed(d3d11Device.As(&m_d3d11On12Device));
```



| <span data-ttu-id="53635-118">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="53635-118">Call flow</span></span>                                              | <span data-ttu-id="53635-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="53635-119">Parameters</span></span> |
|--------------------------------------------------------|------------|
| [<span data-ttu-id="53635-120">**ID3D11Device**</span><span class="sxs-lookup"><span data-stu-id="53635-120">**ID3D11Device**</span></span>](/windows/desktop/api/d3d11/nn-d3d11-id3d11device)            |            |
| [<span data-ttu-id="53635-121">**D3D11On12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="53635-121">**D3D11On12CreateDevice**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice) |            |



 

## <a name="create-a-d2d-factory"></a><span data-ttu-id="53635-122">Создание фабрики D2D</span><span class="sxs-lookup"><span data-stu-id="53635-122">Create a D2D factory</span></span>

<span data-ttu-id="53635-123">Теперь, когда у нас есть устройство 11On12, мы используем его для создания фабрики и устройства D2D точно так же, как это обычно делается с D3D11.</span><span class="sxs-lookup"><span data-stu-id="53635-123">Now that we have an 11On12 device, we use it to create a D2D factory and device just as it would normally be done with D3D11.</span></span>

<span data-ttu-id="53635-124">Добавьте в метод **лоадассетс** .</span><span class="sxs-lookup"><span data-stu-id="53635-124">Add to the **LoadAssets** method.</span></span>

``` syntax
 // Create D2D/DWrite components.
    {
        D2D1_DEVICE_CONTEXT_OPTIONS deviceOptions = D2D1_DEVICE_CONTEXT_OPTIONS_NONE;
        ThrowIfFailed(D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, __uuidof(ID2D1Factory3), &d2dFactoryOptions, &m_d2dFactory));
        ComPtr<IDXGIDevice> dxgiDevice;
        ThrowIfFailed(m_d3d11On12Device.As(&dxgiDevice));
        ThrowIfFailed(m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice));
        ThrowIfFailed(m_d2dDevice->CreateDeviceContext(deviceOptions, &m_d2dDeviceContext));
        ThrowIfFailed(DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED, __uuidof(IDWriteFactory), &m_dWriteFactory));
    }
```



| <span data-ttu-id="53635-125">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="53635-125">Call flow</span></span>                                                                        | <span data-ttu-id="53635-126">Параметры</span><span class="sxs-lookup"><span data-stu-id="53635-126">Parameters</span></span>                                                   |
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="53635-127">**\_ \_ Параметры контекста устройства \_ D2D1**</span><span class="sxs-lookup"><span data-stu-id="53635-127">**D2D1\_DEVICE\_CONTEXT\_OPTIONS**</span></span>](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options)     |                                                              |
| [<span data-ttu-id="53635-128">**D2D1CreateFactory**</span><span class="sxs-lookup"><span data-stu-id="53635-128">**D2D1CreateFactory**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)                              | [<span data-ttu-id="53635-129">**\_Тип фабрики D2D1 \_**</span><span class="sxs-lookup"><span data-stu-id="53635-129">**D2D1\_FACTORY\_TYPE**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)        |
| [<span data-ttu-id="53635-130">**идксгидевице**</span><span class="sxs-lookup"><span data-stu-id="53635-130">**IDXGIDevice**</span></span>](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)                                      |                                                              |
| [<span data-ttu-id="53635-131">**ID2D1Factory3:: Креатедевице**</span><span class="sxs-lookup"><span data-stu-id="53635-131">**ID2D1Factory3::CreateDevice**</span></span>](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1factory3-createdevice)           |                                                              |
| [<span data-ttu-id="53635-132">**ID2D1Device:: Креатедевицеконтекст**</span><span class="sxs-lookup"><span data-stu-id="53635-132">**ID2D1Device::CreateDeviceContext**</span></span>](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) |                                                              |
| [<span data-ttu-id="53635-133">**двритекреатефактори**</span><span class="sxs-lookup"><span data-stu-id="53635-133">**DWriteCreateFactory**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-dwritecreatefactory)                       | [<span data-ttu-id="53635-134">**\_Тип фабрики дврите \_**</span><span class="sxs-lookup"><span data-stu-id="53635-134">**DWRITE\_FACTORY\_TYPE**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_factory_type) |



 

## <a name="create-a-render-target-for-d2d"></a><span data-ttu-id="53635-135">Создание целевого объекта отрисовки для D2D</span><span class="sxs-lookup"><span data-stu-id="53635-135">Create a render target for D2D</span></span>

<span data-ttu-id="53635-136">D3D12 владеет цепочкой буферов обмена, поэтому, если нам нужно отобразить в задний буфер с помощью нашего устройства 11On12 (содержимое D2D), необходимо создать Упакованные ресурсы типа [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) из задних буферов типа [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="53635-136">D3D12 owns the swap chain, so if we want to render to the back buffer using our 11On12 device (D2D content), then we need to create wrapped resources of type [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) from the back buffers of type [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span> <span data-ttu-id="53635-137">Это связывает **ID3D12Resource** с интерфейсом на основе D3D11, чтобы его можно было использовать с устройством 11On12.</span><span class="sxs-lookup"><span data-stu-id="53635-137">This links the **ID3D12Resource** with a D3D11 based interface so that it can be used with the 11On12 device.</span></span> <span data-ttu-id="53635-138">После того как у нас есть заключенный в оболочку ресурс, можно создать поверхность целевого объекта рендеринга для преобразования D2D, а также в метод **лоадассетс** .</span><span class="sxs-lookup"><span data-stu-id="53635-138">After we have a wrapped resource, we can then create a render target surface for D2D to render to, also in the **LoadAssets** method.</span></span>

``` syntax
 // Query the desktop's dpi settings, which will be used to create
    // D2D's render targets.
    float dpiX;
    float dpiY;
    m_d2dFactory->GetDesktopDpi(&dpiX, &dpiY);
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = D2D1::BitmapProperties1(
        D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
        D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX,
        dpiY
        );  

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="53635-139">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="53635-139">Call flow</span></span></th>
<th><span data-ttu-id="53635-140">Параметры</span><span class="sxs-lookup"><span data-stu-id="53635-140">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53635-141"><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory:: Жетдесктопдпи</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-141"><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory::GetDesktopDpi</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="53635-142"><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-142"><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></span></span></td>
<td><dl><span data-ttu-id="53635-143"><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-143"><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a></span></span><br />
<span data-ttu-id="53635-144">[<strong>D2D1_BITMAP_OPTIONS</strong>] (/Виндовс/десктоп/АПИ/d2d1_1/не-d2d1_1 d2d1_bitmap_options)</span><span class="sxs-lookup"><span data-stu-id="53635-144">[<strong>D2D1_BITMAP_OPTIONS</strong>](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)</span></span><br />
<span data-ttu-id="53635-145">[<strong>PixelFormat</strong>] (/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)</span><span class="sxs-lookup"><span data-stu-id="53635-145">[<strong>PixelFormat</strong>](/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)</span></span><br />
<span data-ttu-id="53635-146">[<strong>DXGI_FORMAT</strong>] (/Виндовс/десктоп/АПИ/дксгиформат/не-дксгиформат-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="53635-146">[<strong>DXGI_FORMAT</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span></span><br />
<span data-ttu-id="53635-147">[<strong>D2D1_ALPHA_MODE</strong>] (/Виндовс/десктоп/АПИ/дкоммон/не-дкоммон-d2d1_alpha_mode)</span><span class="sxs-lookup"><span data-stu-id="53635-147">[<strong>D2D1_ALPHA_MODE</strong>](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53635-148"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-148"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="53635-149"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>жеткпудескрипторхандлефорхеапстарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-149"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53635-150"><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>Идксгисвапчаин:: buffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-150"><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain::GetBuffer</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="53635-151"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>креатерендертаржетвиев</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-151"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="53635-152"><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-152"><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></span></span></td>
<td><span data-ttu-id="53635-153"><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-153"><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53635-154"><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>креатевраппедресаурце</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-154"><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></span></span></td>
<td><span data-ttu-id="53635-155"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-155"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53635-156"><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>идксгисурфаце</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-156"><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="53635-157"><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext:: Креатебитмапфромдксгисурфаце</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-157"><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext::CreateBitmapFromDxgiSurface</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="53635-158"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>креатекоммандаллокатор</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-158"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></span></span></td>
<td><span data-ttu-id="53635-159"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="53635-159"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="create-basic-d2d-text-objects"></a><span data-ttu-id="53635-160">Создание базовых текстовых объектов D2D</span><span class="sxs-lookup"><span data-stu-id="53635-160">Create basic D2D text objects</span></span>

<span data-ttu-id="53635-161">Теперь у нас есть [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) для отрисовки трехмерного содержимого, [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) , который является общим для нашего 12 устройств через [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) , который можно использовать для отображения 2D-содержимого, и они настроены для отображения в одной цепочке буферов.</span><span class="sxs-lookup"><span data-stu-id="53635-161">Now we have an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) to render 3D content, an [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) that is shared with our 12 device via an [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) - which we can use to render 2D content - and they are both configured to render to the same swap chain.</span></span> <span data-ttu-id="53635-162">В этом примере просто используется устройство D2D для отрисовки текста по трехмерной сцене, подобно тому, как игры визуализируют свой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="53635-162">This sample simply uses the D2D device to render text over the 3D scene, similar to how games render their UI.</span></span> <span data-ttu-id="53635-163">Для этого необходимо создать базовые объекты D2D, все еще находясь в методе **лоадассетс** .</span><span class="sxs-lookup"><span data-stu-id="53635-163">For that, we need to create some basic D2D objects, still in the **LoadAssets** method.</span></span>

``` syntax
 // Create D2D/DWrite objects for rendering text.
    {
        ThrowIfFailed(m_d2dDeviceContext->CreateSolidColorBrush(D2D1::ColorF(D2D1::ColorF::Black), &m_textBrush));
        ThrowIfFailed(m_dWriteFactory->CreateTextFormat(
            L"Verdana",
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            50,
            L"en-us",
            &m_textFormat
            ));
        ThrowIfFailed(m_textFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER));
        ThrowIfFailed(m_textFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER));
    }
```



| <span data-ttu-id="53635-164">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="53635-164">Call flow</span></span>                                                                                           | <span data-ttu-id="53635-165">Параметры</span><span class="sxs-lookup"><span data-stu-id="53635-165">Parameters</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="53635-166">[**ID2D1RenderTarget:: Креатесолидколорбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))</span><span class="sxs-lookup"><span data-stu-id="53635-166">[**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))</span></span>    | [<span data-ttu-id="53635-167">**колорф**</span><span class="sxs-lookup"><span data-stu-id="53635-167">**ColorF**</span></span>](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)                                              |
| [<span data-ttu-id="53635-168">**Идвритефактори:: Креатетекстформат**</span><span class="sxs-lookup"><span data-stu-id="53635-168">**IDWriteFactory::CreateTextFormat**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat)                 | [<span data-ttu-id="53635-169">**\_ \_ насыщенность шрифта дврите**</span><span class="sxs-lookup"><span data-stu-id="53635-169">**DWRITE\_FONT\_WEIGHT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_weight)                 |
| [<span data-ttu-id="53635-170">**Идвритетекстформат:: Сеттексталигнмент**</span><span class="sxs-lookup"><span data-stu-id="53635-170">**IDWriteTextFormat::SetTextAlignment**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)           | [<span data-ttu-id="53635-171">**\_Выравнивание текста \_ дврите**</span><span class="sxs-lookup"><span data-stu-id="53635-171">**DWRITE\_TEXT\_ALIGNMENT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_text_alignment)           |
| [<span data-ttu-id="53635-172">**Идвритетекстформат:: Сетпараграфалигнмент**</span><span class="sxs-lookup"><span data-stu-id="53635-172">**IDWriteTextFormat::SetParagraphAlignment**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) | [<span data-ttu-id="53635-173">**\_Выравнивание абзаца дврите \_**</span><span class="sxs-lookup"><span data-stu-id="53635-173">**DWRITE\_PARAGRAPH\_ALIGNMENT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_paragraph_alignment) |



 

## <a name="updating-the-main-render-loop"></a><span data-ttu-id="53635-174">Обновление основного цикла рендеринга</span><span class="sxs-lookup"><span data-stu-id="53635-174">Updating the main render loop</span></span>

<span data-ttu-id="53635-175">После завершения инициализации образца можно перейти к основному циклу рендеринга.</span><span class="sxs-lookup"><span data-stu-id="53635-175">Now that the initialization of the sample is complete, we can move on to the main render loop.</span></span>

``` syntax
// Render the scene.
void D3D1211on12::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    RenderUI();

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(0, 0));

    MoveToNextFrame();
}
```



| <span data-ttu-id="53635-176">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="53635-176">Call flow</span></span>                                                              | <span data-ttu-id="53635-177">Параметры</span><span class="sxs-lookup"><span data-stu-id="53635-177">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="53635-178">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="53635-178">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="53635-179">**ексекутекоммандлистс**</span><span class="sxs-lookup"><span data-stu-id="53635-179">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="53635-180">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="53635-180">**IDXGISwapChain1::Present1**</span></span>](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="53635-181">Единственное, что нового в нашем цикле подготовки к просмотру — это вызов **рендеруи** , который будет использовать D2D для визуализации нашего пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="53635-181">The only thing new to our render loop is the **RenderUI** call, which will use D2D to render our UI.</span></span> <span data-ttu-id="53635-182">Обратите внимание, что мы сначала выполняем все списки команд D3D12, чтобы визуализировать трехмерную сцену, а затем отрисовка пользовательского интерфейса поверх него.</span><span class="sxs-lookup"><span data-stu-id="53635-182">Notice that we execute all of our D3D12 command lists first to render our 3D scene, and then we render our UI on top of that.</span></span> <span data-ttu-id="53635-183">Прежде чем мы подробно рассмотрим **рендеруи**, мы должны взглянуть на изменения в **популатекоммандлистс**.</span><span class="sxs-lookup"><span data-stu-id="53635-183">Before we dive into **RenderUI**, we must look at a change to **PopulateCommandLists**.</span></span> <span data-ttu-id="53635-184">В других примерах мы обычно помещаем барьер ресурсов в список команд перед его закрытием, чтобы перевести задний буфер из целевого состояния прорисовки в текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="53635-184">In other samples we commonly put a resource barrier on the command list prior to closing it to transition the back buffer from the render target state to the present state.</span></span> <span data-ttu-id="53635-185">Однако в этом примере мы удалим этот барьер ресурсов, так как нам по-прежнему нужно выполнить рендеринг в задние буферы с D2D.</span><span class="sxs-lookup"><span data-stu-id="53635-185">However, in this sample we remove that resource barrier, because we still need to render to the back buffers with D2D.</span></span> <span data-ttu-id="53635-186">Обратите внимание, что при создании заключенных в оболочку ресурсов заднего буфера мы указали состояние целевого объекта прорисовки как "IN" (состояние "IN") и текущее состояние в качестве состояния "OUT" (исходящие).</span><span class="sxs-lookup"><span data-stu-id="53635-186">Note that when we created our wrapped resources of the back buffer that we specified the render target state as the “IN” state and the present state as the “OUT” state.</span></span>

<span data-ttu-id="53635-187">**Рендеруи** довольно прямо вперед с точки зрения использования D2D.</span><span class="sxs-lookup"><span data-stu-id="53635-187">**RenderUI** is fairly straight-forward in terms of D2D usage.</span></span> <span data-ttu-id="53635-188">Мы устанавливаем целевой объект отрисовки и отображаем наш текст.</span><span class="sxs-lookup"><span data-stu-id="53635-188">We set our render target and render our text.</span></span> <span data-ttu-id="53635-189">Однако перед использованием любых ресурсов, переносимых на устройство 11On12, таких как целевые объекты рендеринга заднего буфера, необходимо вызвать API [**аккуиревраппедресаурцес**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) на устройстве 11On12.</span><span class="sxs-lookup"><span data-stu-id="53635-189">However, before using any wrapped resources on an 11On12 device, such as our back buffer render targets, we must call the [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) API on the 11On12 device.</span></span> <span data-ttu-id="53635-190">После подготовки к просмотру мы вызываем API [**релеасевраппедресаурцес**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) на устройстве 11On12.</span><span class="sxs-lookup"><span data-stu-id="53635-190">After rendering we call the [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) API on the 11On12 device.</span></span> <span data-ttu-id="53635-191">Вызывая **релеасевраппедресаурцес** , мы создаем барьер ресурсов в фоновом режиме, который будет переносить указанный ресурс в состояние «Out», указанное во время создания.</span><span class="sxs-lookup"><span data-stu-id="53635-191">By calling **ReleaseWrappedResources** we incur a resource barrier behind the scenes that will transition the specified resource to the “OUT” state specified at creation time.</span></span> <span data-ttu-id="53635-192">В нашем случае это текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="53635-192">In our case, this is the present state.</span></span> <span data-ttu-id="53635-193">Наконец, чтобы отправить все команды, выполненные на устройстве 11On12, в общую [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue), необходимо вызвать [**flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) на [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).</span><span class="sxs-lookup"><span data-stu-id="53635-193">Finally, in order to submit all of our commands performed on the 11On12 device to the shared [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue), we must call [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).</span></span>

``` syntax
// Render text over D3D12 using D2D via the 11On12 device.
void D3D1211on12::RenderUI()
{
    D2D1_SIZE_F rtSize = m_d2dRenderTargets[m_frameIndex]->GetSize();
    D2D1_RECT_F textRect = D2D1::RectF(0, 0, rtSize.width, rtSize.height);
    static const WCHAR text[] = L"11On12";

    // Acquire our wrapped render target resource for the current back buffer.
    m_d3d11On12Device->AcquireWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Render text directly to the back buffer.
    m_d2dDeviceContext->SetTarget(m_d2dRenderTargets[m_frameIndex].Get());
    m_d2dDeviceContext->BeginDraw();
    m_d2dDeviceContext->SetTransform(D2D1::Matrix3x2F::Identity());
    m_d2dDeviceContext->DrawTextW(
        text,
        _countof(text) - 1,
        m_textFormat.Get(),
        &textRect,
        m_textBrush.Get()
        );
    ThrowIfFailed(m_d2dDeviceContext->EndDraw());

    // Release our wrapped render target resource. Releasing 
    // transitions the back buffer resource to the state specified
    // as the OutState when the wrapped resource was created.
    m_d3d11On12Device->ReleaseWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Flush to submit the 11 command list to the shared command queue.
    m_d3d11DeviceContext->Flush();
}
```



| <span data-ttu-id="53635-194">Поток вызовов</span><span class="sxs-lookup"><span data-stu-id="53635-194">Call flow</span></span>                                                                                                                                                                                 | <span data-ttu-id="53635-195">Параметры</span><span class="sxs-lookup"><span data-stu-id="53635-195">Parameters</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="53635-196">**D2D1 \_ размер \_ F**</span><span class="sxs-lookup"><span data-stu-id="53635-196">**D2D1\_SIZE\_F**</span></span>](/windows/desktop/Direct2D/d2d1-size-f)                                                                                                                                                 |                                       |
| [<span data-ttu-id="53635-197">**D2D1 \_ Rect \_ F**</span><span class="sxs-lookup"><span data-stu-id="53635-197">**D2D1\_RECT\_F**</span></span>](/windows/desktop/Direct2D/d2d1-rect-f)                                                                                                                                                 | [<span data-ttu-id="53635-198">**ректф**</span><span class="sxs-lookup"><span data-stu-id="53635-198">**RectF**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-rectf)           |
| [<span data-ttu-id="53635-199">**аккуиревраппедресаурцес**</span><span class="sxs-lookup"><span data-stu-id="53635-199">**AcquireWrappedResources**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)                                                                                                               |                                       |
| [<span data-ttu-id="53635-200">**ID2D1DeviceContext:: Сеттаржет**</span><span class="sxs-lookup"><span data-stu-id="53635-200">**ID2D1DeviceContext::SetTarget**</span></span>](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget)                                                                                                                |                                       |
| [<span data-ttu-id="53635-201">**ID2D1RenderTarget:: Бегиндрав**</span><span class="sxs-lookup"><span data-stu-id="53635-201">**ID2D1RenderTarget::BeginDraw**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)                                                                                                                  |                                       |
| [<span data-ttu-id="53635-202">**ID2D1RenderTarget:: Сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="53635-202">**ID2D1RenderTarget::SetTransform**</span></span>](/windows/desktop/Direct2D/id2d1rendertarget-settransform)                                                                                                            | [<span data-ttu-id="53635-203">**Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="53635-203">**Matrix3x2F**</span></span>](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) |
| <span data-ttu-id="53635-204">[**ID2D1RenderTarget::D Равтекств**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="53635-204">[**ID2D1RenderTarget::DrawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> |                                       |
| [<span data-ttu-id="53635-205">**ID2D1RenderTarget:: EndDraw**</span><span class="sxs-lookup"><span data-stu-id="53635-205">**ID2D1RenderTarget::EndDraw**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)                                                                                                                      |                                       |
| [<span data-ttu-id="53635-206">**релеасевраппедресаурцес**</span><span class="sxs-lookup"><span data-stu-id="53635-206">**ReleaseWrappedResources**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)                                                                                                               |                                       |
| [<span data-ttu-id="53635-207">**Ссылку ID3D11DeviceContext:: Flush**</span><span class="sxs-lookup"><span data-stu-id="53635-207">**ID3D11DeviceContext::Flush**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush)                                                                                                                    |                                       |



 

## <a name="run-the-sample"></a><span data-ttu-id="53635-208">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="53635-208">Run the sample</span></span>

![Окончательные выходные данные примера 11 в 12 примере](images/11on12image.png)

## <a name="related-topics"></a><span data-ttu-id="53635-210">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="53635-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53635-211">Пошаговые инструкции по коду D3D12</span><span class="sxs-lookup"><span data-stu-id="53635-211">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="53635-212">Direct3D 11 на 12</span><span class="sxs-lookup"><span data-stu-id="53635-212">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)
</dt> <dt>

[<span data-ttu-id="53635-213">Взаимодействие Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="53635-213">Direct3D 12 Interop</span></span>](direct3d-12-interop.md)
</dt> <dt>

[<span data-ttu-id="53635-214">Справочник по 11on12</span><span class="sxs-lookup"><span data-stu-id="53635-214">11on12 Reference</span></span>](direct3d-11on12-reference.md)
</dt> </dl>

 

 