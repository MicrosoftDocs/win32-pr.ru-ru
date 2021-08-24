---
title: Общие сведения о взаимодействии Direct2D и Direct3D
description: Общие сведения о взаимодействии Direct2D и Direct3D
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D, взаимодействие Direct3D
- Direct2D, взаимодействие
- взаимодействие, Direct2D
- взаимодействие, Direct3D
- Direct3D, взаимодействие
- Direct3D, Direct2D взаимодействие
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1aca1eac7218528e897a2a519543d80ab4ae2be3fa5d11a4107b02f1b23f2061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698194"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Общие сведения о взаимодействии Direct2D и Direct3D

Высокопроизводительные и трехмерные графики с аппаратным ускорением все чаще становятся частью приложений, не являющихся играми, и большинство игровых приложений используют Двумерные графики в виде меню и Heads-Up отображения (Худс). Существует множество значений, которые можно добавить, включив традиционную плоскую отрисовку для эффективного использования при визуализации Direct3D.

В этом разделе описывается интеграция двухмерной и трехмерной графики с помощью Direct2D и [Direct3D](../graphics-and-multimedia.md).

В него входят следующие разделы.

-   [Предварительные требования](#prerequisites)
-   [Поддерживаемые версии Direct3D](#supported-direct3d-versions)
-   [Взаимодействие через DXGI](#interoperability-through-dxgi)
-   [Запись в поверхность Direct3D с целевым объектом отрисовки поверхности DXGI](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Создание поверхности DXGI](#creating-a-dxgi-surface)
-   [Запись содержимого Direct2D в буфер цепочки подкачки](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Пример: Рисование двухмерного фона](#example-draw-a-2-d-background)
-   [Использование содержимого Direct2D в качестве текстуры](#using-direct2d-content-as-a-texture)
    -   [Пример. использование содержимого Direct2D в качестве текстуры](#example-use-direct2d-content-as-a-texture)
-   [Изменение размера целевого объекта отрисовки поверхности DXGI](#resizing-a-dxgi-surface-render-target)
-   [Связанные темы](#related-topics)

## <a name="prerequisites"></a>Предварительные требования

В этом обзоре предполагается, что вы знакомы с базовыми операциями рисования Direct2D. Инструкции см. в [кратком](direct2d-quickstart.md)руководстве по Direct2D. Также предполагается, что вы можете программировать с помощью [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="supported-direct3d-versions"></a>Поддерживаемые версии Direct3D

В DirectX 11,0 Direct2D поддерживает взаимодействие только с устройствами Direct3D 10,1. В DirectX 11,1 или более поздней версии Direct2D поддерживает взаимодействие с Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Взаимодействие через DXGI

Начиная с Direct3D 10, среда выполнения Direct3D использует [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) для управления ресурсами. Уровень среды выполнения DXGI обеспечивает межпроцессное совместное использование поверхностей видеопамяти и служит основой для других платформ среды выполнения на основе видеопамяти. Direct2D использует DXGI для взаимодействия с Direct3D.

Существует два основных способа совместного использования Direct2D и Direct3D:

-   Вы можете записать содержимое Direct2D на поверхность Direct3D, получив [**идксгисурфаце**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) и используя его с [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) , чтобы создать [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Затем можно использовать целевой объект отрисовки для добавления двумерного интерфейса или фона к трехмерной графике или использовать Direct2D рисунок в качестве текстуры для трехмерного объекта.
-   Используя [**креатешаредбитмап**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) для создания [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) из [**Идксгисурфаце**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), можно записать сцену Direct3D в растровое изображение и визуализировать ее с помощью Direct2D.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Запись в поверхность Direct3D с целевым объектом отрисовки поверхности DXGI

Для записи в поверхность Direct3D вы получаете [**идксгисурфаце**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) и передаете его методу [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) для создания целевого объекта отрисовки поверхности DXGI. Затем можно использовать целевой объект прорисовки поверхности DXGI для рисования двухмерного содержимого на поверхности DXGI.

Целевой объект отрисовки поверхности DXGI — это разновидность [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Как и другие целевые объекты рендеринга Direct2D, их можно использовать для создания ресурсов и выполнения команд рисования.

Целевой объект прорисовки поверхности DXGI и поверхность DXGI должны использовать один и тот же формат DXGI. Если при создании целевого объекта рендеринга указать формат неизвестного формата DXGI, он будет автоматически использовать формат поверхности. [**\_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Целевой объект прорисовки поверхности DXGI не выполняет синхронизацию рабочей области DXGI.

### <a name="creating-a-dxgi-surface"></a>Создание поверхности DXGI

С помощью Direct3D 10 существует несколько способов получить поверхность DXGI. Вы можете создать [**идксгисвапчаин**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) для устройства, а затем использовать метод метода цепочки [**буферов**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) для получения поверхности DXGI. Вы также можете использовать устройство для создания текстуры, а затем использовать эту текстуру в качестве поверхности DXGI.

Независимо от того, как вы создаете поверхность DXGI, поверхность должна использовать один из форматов DXGI, поддерживаемых объектами рендеринга поверхности DXGI. Список см. в разделе [Поддерживаемые форматы пикселей и альфа-режимы](supported-pixel-formats-and-alpha-modes.md).

Кроме того, [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) , связанный с ПОВЕРХНОСТЬю DXGI, должен поддерживать форматы BGRA DXGI, чтобы поверхность работала с Direct2D. Чтобы обеспечить эту поддержку, используйте флаг [**D3D10 \_ Create \_ Device \_ BGRA \_ support**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) при вызове метода [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) для создания устройства.

В следующем коде определяется метод, создающий [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1). он выбирает оптимальный уровень функций и возвращается к [Windows расширенной платформы растрирования (деформация)](./installing-the-direct2d-debug-layer.md) , если аппаратная отрисовка недоступна.


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



В следующем примере кода используется `CreateD3DDevice` метод, показанный в предыдущем примере, для создания устройства Direct3D, которое может создавать поверхности DXGI для использования с Direct2D.


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a>Запись содержимого Direct2D в буфер цепочки подкачки

Самый простой способ добавить Direct2D содержимое в сцену Direct3D — использовать [**метод метода**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) [**идксгисвапчаин**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) для получения поверхности DXGI, а затем использовать поверхность с методом [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) для создания [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) , с помощью которого будет нарисовано трехмерное содержимое.

Этот подход не отображает содержимое в трех измерениях. Он не будет иметь перспективу или глубину. Однако это полезно для нескольких распространенных задач:

-   Создание двухмерного фона для трехмерной сцены.
-   Создание двухмерного интерфейса перед трехмерной сценой.
-   Использование множественной выборки Direct3D при отрисовке содержимого Direct2D.

В следующем разделе показано, как создать двумерной фон для трехмерной сцены.

### <a name="example-draw-a-2-d-background"></a>Пример: Рисование двухмерного фона

В следующих шагах описывается создание целевого объекта отрисовки поверхности DXGI и его использование для рисования градиентного фона.

1.  Используйте метод [**креатесвапчаин**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) для создания цепочки буферов для [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (переменная *\_ пдевице m* ). Цепочка буферов обмена использует формат DXGI [**\_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, один из форматов DXGI, поддерживаемых Direct2D.

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  Используйте метод метода buffer цепочки [**буферов**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) для получения поверхности DXGI.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Используйте поверхность DXGI для создания целевого объекта отрисовки DXGI.
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  Чтобы нарисовать градиентный фон, используйте целевой объект рендеринга.

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

В этом примере код пропущен.

## <a name="using-direct2d-content-as-a-texture"></a>Использование содержимого Direct2D в качестве текстуры

Другим способом использования Direct2D содержимого с помощью Direct3D является использование Direct2D для создания двухмерной текстуры, а затем применение текстуры к трехмерной модели. Это делается путем создания [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), получения поверхности DXGI из текстуры и последующего использования поверхности для создания целевого объекта отрисовки поверхности DXGI. Поверхность **ID3D10Texture2D** должна использовать флаг привязки [**\_ \_ \_ целевого объекта ПРОРИСОВКи D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) и использовать формат DXGI, поддерживаемый целями рендеринга поверхности DXGI. Список поддерживаемых форматов DXGI см. в разделе [Поддерживаемые форматы пикселей и альфа-режимы](supported-pixel-formats-and-alpha-modes.md).

### <a name="example-use-direct2d-content-as-a-texture"></a>Пример. использование содержимого Direct2D в качестве текстуры

В следующих примерах показано, как создать целевой объект отрисовки поверхности DXGI, который визуализируется в двумерной текстуре (представленной [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).

1.  Во-первых, используйте устройство Direct3D для создания двухмерной текстуры. Текстура использует [**\_ \_ \_ целевой объект прорисовки привязки D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) и флаги привязки **D3D10 \_ привязки \_ \_ ресурса шейдера** и использует [**Формат DXGI \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, один из форматов DXGI, поддерживаемых Direct2D.

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  Используйте текстуру для получения поверхности DXGI.

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  Используйте поверхность с методом [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) , чтобы получить целевой объект прорисовки Direct2D.

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

Теперь, когда вы получили целевой объект рендеринга Direct2D и со его с текстурой Direct3D, вы можете использовать целевой объект рендеринга для рисования содержимого Direct2D в этой текстуре, и вы можете применить эту текстуру к примитивам Direct3D.

В этом примере код пропущен.

## <a name="resizing-a-dxgi-surface-render-target"></a>Изменение размера целевого объекта отрисовки поверхности DXGI

Целевые объекты прорисовки поверхности DXGI не поддерживают метод [**ID2D1RenderTarget:: resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) . Чтобы изменить размер целевого объекта рендеринга для поверхности DXGI, приложение должно освободить и создать его повторно.

Эта операция потенциально может привести к проблемам с производительностью. Целью отрисовки может быть последний активный ресурс Direct2D, который хранит ссылку на [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) , связанный с поверхностью DXGI целевого объекта отрисовки. Если приложение освобождает целевой объект отрисовки, а ссылка **ID3D10Device1** уничтожается, новый объект должен быть создан заново.

Эту потенциально дорогостоящую операцию можно избежать, сохранив по крайней мере один ресурс Direct2D, созданный целевым объектом рендеринга, при повторном создании этого целевого объекта отрисовки. Ниже приведены некоторые Direct2D ресурсы, которые подходят для этого подхода:

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (который может храниться косвенно [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Для реализации этого подхода метод изменения размера должен проверить, доступно ли устройство Direct3D. Если она доступна, выпустите и повторно создайте целевые объекты отрисовки для поверхности DXGI, но сохраните все созданные ранее ресурсы и используйте их повторно. Это работает потому, что, как описано в [обзоре ресурсов](resources-and-resource-domains.md), ресурсы, созданные двумя целевыми объектами рендеринга, совместимы, если обе цели рендеринга связаны с одним и тем же устройством Direct3D.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поддерживаемые форматы пикселей и режимы альфа-канала](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Windows Графика DirectX](../graphics-and-multimedia.md)
</dt> </dl>

 

 
