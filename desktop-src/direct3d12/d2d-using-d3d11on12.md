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
# <a name="d2d-using-d3d11on12"></a>D2D с использованием D3D11on12

В примере **D3D1211on12** показано, как ВИЗУАЛИЗИРОВАТЬ содержимое D2D через D3D12 содержимое путем совместного использования ресурсов между устройством на базе 11 и устройством на 12 устройств.

-   [Создание ID3D11On12Device](#create-an-id3d11on12device)
-   [Создание фабрики D2D](#create-a-d2d-factory)
-   [Создание целевого объекта отрисовки для D2D](#create-a-render-target-for-d2d)
-   [Создание базовых текстовых объектов D2D](#create-basic-d2d-text-objects)
-   [Обновление основного цикла рендеринга](#updating-the-main-render-loop)
-   [Запуск примера](#run-the-sample)
-   [Связанные темы](#related-topics)

## <a name="create-an-id3d11on12device"></a>Создание ID3D11On12Device

Первым шагом является создание [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) после создания [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) , который включает создание [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , заключенного в оболочку **ID3D12Device** через API-интерфейс [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Этот API также использует, помимо прочих параметров, [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) , чтобы устройство 11On12 могла отправлять свои команды. После создания **ID3D11Device** можно запросить от него интерфейс **ID3D11On12Device** . Это основной объект устройства, который будет использоваться для настройки D2D.

В методе **лоадпипелине** Настройте устройства.

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



| Поток вызовов                                              | Параметры |
|--------------------------------------------------------|------------|
| [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device)            |            |
| [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice) |            |



 

## <a name="create-a-d2d-factory"></a>Создание фабрики D2D

Теперь, когда у нас есть устройство 11On12, мы используем его для создания фабрики и устройства D2D точно так же, как это обычно делается с D3D11.

Добавьте в метод **лоадассетс** .

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



| Поток вызовов                                                                        | Параметры                                                   |
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_ \_ Параметры контекста устройства \_ D2D1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options)     |                                                              |
| [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)                              | [**\_Тип фабрики D2D1 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)        |
| [**идксгидевице**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)                                      |                                                              |
| [**ID2D1Factory3:: Креатедевице**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1factory3-createdevice)           |                                                              |
| [**ID2D1Device:: Креатедевицеконтекст**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) |                                                              |
| [**двритекреатефактори**](/windows/desktop/api/dwrite/nf-dwrite-dwritecreatefactory)                       | [**\_Тип фабрики дврите \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_factory_type) |



 

## <a name="create-a-render-target-for-d2d"></a>Создание целевого объекта отрисовки для D2D

D3D12 владеет цепочкой буферов обмена, поэтому, если нам нужно отобразить в задний буфер с помощью нашего устройства 11On12 (содержимое D2D), необходимо создать Упакованные ресурсы типа [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) из задних буферов типа [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource). Это связывает **ID3D12Resource** с интерфейсом на основе D3D11, чтобы его можно было использовать с устройством 11On12. После того как у нас есть заключенный в оболочку ресурс, можно создать поверхность целевого объекта рендеринга для преобразования D2D, а также в метод **лоадассетс** .

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
<th>Поток вызовов</th>
<th>Параметры</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory:: Жетдесктопдпи</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></td>
<td><dl><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a><br />
[<strong>D2D1_BITMAP_OPTIONS</strong>] (/Виндовс/десктоп/АПИ/d2d1_1/не-d2d1_1 d2d1_bitmap_options)<br />
[<strong>PixelFormat</strong>] (/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)<br />
[<strong>DXGI_FORMAT</strong>] (/Виндовс/десктоп/АПИ/дксгиформат/не-дксгиформат-dxgi_format)<br />
[<strong>D2D1_ALPHA_MODE</strong>] (/Виндовс/десктоп/АПИ/дкоммон/не-дкоммон-d2d1_alpha_mode)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>жеткпудескрипторхандлефорхеапстарт</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>Идксгисвапчаин:: buffer</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>креатерендертаржетвиев</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></td>
<td><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>креатевраппедресаурце</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>идксгисурфаце</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext:: Креатебитмапфромдксгисурфаце</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>креатекоммандаллокатор</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="create-basic-d2d-text-objects"></a>Создание базовых текстовых объектов D2D

Теперь у нас есть [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) для отрисовки трехмерного содержимого, [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) , который является общим для нашего 12 устройств через [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) , который можно использовать для отображения 2D-содержимого, и они настроены для отображения в одной цепочке буферов. В этом примере просто используется устройство D2D для отрисовки текста по трехмерной сцене, подобно тому, как игры визуализируют свой пользовательский интерфейс. Для этого необходимо создать базовые объекты D2D, все еще находясь в методе **лоадассетс** .

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



| Поток вызовов                                                                                           | Параметры                                                                 |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ID2D1RenderTarget:: Креатесолидколорбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))    | [**колорф**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)                                              |
| [**Идвритефактори:: Креатетекстформат**](/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat)                 | [**\_ \_ насыщенность шрифта дврите**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_weight)                 |
| [**Идвритетекстформат:: Сеттексталигнмент**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)           | [**\_Выравнивание текста \_ дврите**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_text_alignment)           |
| [**Идвритетекстформат:: Сетпараграфалигнмент**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) | [**\_Выравнивание абзаца дврите \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_paragraph_alignment) |



 

## <a name="updating-the-main-render-loop"></a>Обновление основного цикла рендеринга

После завершения инициализации образца можно перейти к основному циклу рендеринга.

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



| Поток вызовов                                                              | Параметры |
|------------------------------------------------------------------------|------------|
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**ексекутекоммандлистс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

Единственное, что нового в нашем цикле подготовки к просмотру — это вызов **рендеруи** , который будет использовать D2D для визуализации нашего пользовательского интерфейса. Обратите внимание, что мы сначала выполняем все списки команд D3D12, чтобы визуализировать трехмерную сцену, а затем отрисовка пользовательского интерфейса поверх него. Прежде чем мы подробно рассмотрим **рендеруи**, мы должны взглянуть на изменения в **популатекоммандлистс**. В других примерах мы обычно помещаем барьер ресурсов в список команд перед его закрытием, чтобы перевести задний буфер из целевого состояния прорисовки в текущее состояние. Однако в этом примере мы удалим этот барьер ресурсов, так как нам по-прежнему нужно выполнить рендеринг в задние буферы с D2D. Обратите внимание, что при создании заключенных в оболочку ресурсов заднего буфера мы указали состояние целевого объекта прорисовки как "IN" (состояние "IN") и текущее состояние в качестве состояния "OUT" (исходящие).

**Рендеруи** довольно прямо вперед с точки зрения использования D2D. Мы устанавливаем целевой объект отрисовки и отображаем наш текст. Однако перед использованием любых ресурсов, переносимых на устройство 11On12, таких как целевые объекты рендеринга заднего буфера, необходимо вызвать API [**аккуиревраппедресаурцес**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) на устройстве 11On12. После подготовки к просмотру мы вызываем API [**релеасевраппедресаурцес**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) на устройстве 11On12. Вызывая **релеасевраппедресаурцес** , мы создаем барьер ресурсов в фоновом режиме, который будет переносить указанный ресурс в состояние «Out», указанное во время создания. В нашем случае это текущее состояние. Наконец, чтобы отправить все команды, выполненные на устройстве 11On12, в общую [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue), необходимо вызвать [**flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) на [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).

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



| Поток вызовов                                                                                                                                                                                 | Параметры                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [**D2D1 \_ размер \_ F**](/windows/desktop/Direct2D/d2d1-size-f)                                                                                                                                                 |                                       |
| [**D2D1 \_ Rect \_ F**](/windows/desktop/Direct2D/d2d1-rect-f)                                                                                                                                                 | [**ректф**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rectf)           |
| [**аккуиревраппедресаурцес**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)                                                                                                               |                                       |
| [**ID2D1DeviceContext:: Сеттаржет**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget)                                                                                                                |                                       |
| [**ID2D1RenderTarget:: Бегиндрав**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)                                                                                                                  |                                       |
| [**ID2D1RenderTarget:: Сеттрансформ**](/windows/desktop/Direct2D/id2d1rendertarget-settransform)                                                                                                            | [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) |
| [**ID2D1RenderTarget::D Равтекств**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) |                                       |
| [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)                                                                                                                      |                                       |
| [**релеасевраппедресаурцес**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)                                                                                                               |                                       |
| [**Ссылку ID3D11DeviceContext:: Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush)                                                                                                                    |                                       |



 

## <a name="run-the-sample"></a>Запуск примера

![Окончательные выходные данные примера 11 в 12 примере](images/11on12image.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Пошаговые инструкции по коду D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Direct3D 11 на 12](direct3d-11-on-12.md)
</dt> <dt>

[Взаимодействие Direct3D 12](direct3d-12-interop.md)
</dt> <dt>

[Справочник по 11on12](direct3d-11on12-reference.md)
</dt> </dl>

 

 