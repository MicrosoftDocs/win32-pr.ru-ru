---
title: Подготовка к просмотру с помощью контекста устройства Direct2D
description: В этом разделе вы узнаете, как создать Direct2D \ 32; контекст устройства в Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Устройство Direct2D
- Контекст устройства Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104568151"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a>Подготовка к просмотру с помощью контекста устройства Direct2D

В этом разделе вы узнаете, как создать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) в Windows 8. Эти сведения относятся к вам при разработке приложений для Магазина Windows или классических приложений с помощью Direct2D. В этом разделе описывается назначение объектов контекста устройства Direct2D, создание этого объекта и пошаговое руководство по отрисовке и отображению примитивов и изображений Direct2D. Кроме того, вы узнаете о переключении целевых объектов рендеринга и добавлении эффектов в приложение.

-   [Что такое устройство Direct2D?](#what-is-a-direct2d-device)
-   [Что такое контекст устройства Direct2D?](#what-is-a-direct2d-device-context)
-   [Подготовка к просмотру с помощью Direct2D в Windows 8](#rendering-with-direct2d-on-windows-8)
-   [Зачем использовать контекст устройства для подготовки к просмотру?](#why-use-a-device-context-to-render)
-   [Создание контекста устройства Direct2D для подготовки к просмотру](#how-to-create-a-direct2d-device-context-for-rendering)
-   [Выбор целевого объекта](#selecting-a-target)
-   [Как отобразить и отобразить](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a>Что такое устройство Direct2D?

Для создания контекста устройства Direct2D требуется устройство Direct2D и устройство Direct3D. [**Устройство Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (предоставляет указатель на интерфейс **ID2D1Device** ) представляет адаптер дисплея. Устройство Direct3D (предоставляет указатель на интерфейс [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) связывается с устройством Direct2D. Каждое приложение должно иметь одно **устройство Direct2D**, но может иметь более одного **устройства**.

## <a name="what-is-a-direct2d-device-context"></a>Что такое контекст устройства Direct2D?

[**Контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) (предоставляет указатель на интерфейс **ID2D1DeviceContext** ) представляет набор состояний и буферов команд, которые используются для отображения в целевом объекте. Вы можете вызывать методы в контексте устройства для задания состояния конвейера и создания команд отрисовки с помощью ресурсов, принадлежащих устройству.

## <a name="rendering-with-direct2d-on-windows-8"></a>Подготовка к просмотру с помощью Direct2D в Windows 8

В Windows 7 и более ранних версиях вы используете [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) или другой целевой интерфейс рендеринга для отображения в окне или на поверхности. Начиная с Windows 8, мы не рекомендуем выполнять отрисовку с помощью методов, зависящих от интерфейсов, таких как **ID2D1HwndRenderTarget** , так как они не работают с приложениями Магазина Windows. Вы можете использовать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) для отображения в HWND, если хотите создать классическое приложение и использовать преимущества дополнительных функций **контекста устройства** . Однако для отображения содержимого в приложениях Магазина Windows с помощью [Direct2D](./direct2d-portal.md)требуется **контекст устройства** .

## <a name="why-use-a-device-context-to-render"></a>Зачем использовать контекст устройства для подготовки к просмотру?

-   Можно визуализировать приложения для Магазина Windows.
-   Целевой объект отрисовки можно изменить в любое время до, во время и после отрисовки. Контекст устройства гарантирует, что вызовы методов рисования выполняются по порядку и применяют их при переключении целевого объекта рендеринга.
-   В контексте устройства можно использовать более одного типа окон. Вы можете использовать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) и [**цепочку подкачки DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) для непосредственного отображения в [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) или в [**Windows:: UI:: XAML:: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).
-   Вы можете использовать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) для создания [эффектов Direct2D](effects-overview.md) и визуализации выходных данных эффекта изображения или графа эффектов в целевой объект прорисовки.
-   Можно использовать несколько [**контекстов устройств**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), что может быть полезно для повышения производительности в многопоточном приложении. Дополнительные сведения см. в разделе [многопоточные приложения Direct2D](multi-threaded-direct2d-apps.md) .
-   [**Контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) тесно взаимодействует с Direct3D, обеспечивая вам больше доступа к параметрам Direct3D.

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a>Создание контекста устройства Direct2D для подготовки к просмотру

В этом примере кода показано, как создать устройство Direct3D11, получить связанное устройство DXGI, создать [**устройство Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)и, наконец, создать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D для подготовки к просмотру.

Ниже приведена схема вызовов методов и интерфейсов, используемых этим кодом.

![Схема устройств Direct2D и Direct3D и контекстов устройств.](images/devicecontextdiagram.png)

> [!Note]  
> В этом коде предполагается, что у вас уже есть объект [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) . Дополнительные сведения см. на [**странице справочника по ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).

 


```C++
    // This flag adds support for surfaces with a different color channel ordering than the API default.
    // You need it for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    
    // This array defines the set of DirectX hardware feature levels this app  supports.
    // The ordering is important and you should  preserve it.
    // Don't forget to declare your app's minimum required feature level in its
    // description.  All apps are assumed to support 9.1 unless otherwise stated.
    D3D_FEATURE_LEVEL featureLevels[] = 
    {
        D3D_FEATURE_LEVEL_11_1,
        D3D_FEATURE_LEVEL_11_0,
        D3D_FEATURE_LEVEL_10_1,
        D3D_FEATURE_LEVEL_10_0,
        D3D_FEATURE_LEVEL_9_3,
        D3D_FEATURE_LEVEL_9_2,
        D3D_FEATURE_LEVEL_9_1
    };

    // Create the DX11 API device object, and get a corresponding context.
    ComPtr<ID3D11Device> device;
    ComPtr<ID3D11DeviceContext> context;

    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of possible feature levels
            D3D11_SDK_VERSION,          
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );

    ComPtr<IDXGIDevice> dxgiDevice;
    // Obtain the underlying DXGI device of the Direct3D11 device.
    DX::ThrowIfFailed(
        device.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // Get Direct2D device's corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Давайте подробно рассмотрим шаги, описанные в предыдущем примере кода.

1.  Получите указатель интерфейса ID3D11Device, который потребуется для создания контекста устройства.

    -   Объявите флаги создания, чтобы настроить устройство [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) для поддержки BGRA. Для [Direct2D](./direct2d-portal.md) требуется BGRA цветовой порядок.
    -   Объявите массив записей [**\_ \_ уровня компонента D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) , представляющих набор уровней компонентов, которые будет поддерживать ваше приложение.
        > [!Note]  
        > [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) выполняет поиск в списке, пока не найдет уровень компонентов, поддерживаемый основной системой.

         

    -   Используйте функцию [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) для создания объекта [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) , функция также возвращает объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , но этот объект не требуется для этого примера.

2.  Запросите [**устройство Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) для своего интерфейса [**устройства DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .
3.  Создайте объект [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) , вызвав метод [**ID2D1Factory:: креатедевице**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) и передав объект [**идксгидевице**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .
4.  Создайте указатель [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) с помощью метода [**ID2D1Device:: креатедевицеконтекст**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .

## <a name="selecting-a-target"></a>Выбор целевого объекта

В этом примере кода показано, как получить [**двухмерную текстуру Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) для буфера окна и создать цель точечного рисунка, ссылающуюся на эту текстуру, в которую визуализируется [**контекст устройства Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .


```C++
        // Allocate a descriptor.
        DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};
        swapChainDesc.Width = 0;                           // use automatic sizing
        swapChainDesc.Height = 0;
        swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM; // this is the most common swapchain format
        swapChainDesc.Stereo = false; 
        swapChainDesc.SampleDesc.Count = 1;                // don't use multi-sampling
        swapChainDesc.SampleDesc.Quality = 0;
        swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapChainDesc.BufferCount = 2;                     // use double buffering to enable flip
        swapChainDesc.Scaling = DXGI_SCALING_NONE;
        swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL; // all apps must use this SwapEffect
        swapChainDesc.Flags = 0;

        // Identify the physical adapter (GPU or card) this device is runs on.
        ComPtr<IDXGIAdapter> dxgiAdapter;
        DX::ThrowIfFailed(
            dxgiDevice->GetAdapter(&dxgiAdapter)
            );

        // Get the factory object that created the DXGI device.
        ComPtr<IDXGIFactory2> dxgiFactory;
        DX::ThrowIfFailed(
            dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory))
            );

        // Get the final swap chain for this window from the DXGI factory.
        DX::ThrowIfFailed(
            dxgiFactory->CreateSwapChainForCoreWindow(
                device.Get(),
                reinterpret_cast<IUnknown*>(m_window),
                &swapChainDesc,
                nullptr,    // allow on all displays
                &m_swapChain
                )
            );

        // Ensure that DXGI doesn't queue more than one frame at a time.
        DX::ThrowIfFailed(
            dxgiDevice->SetMaximumFrameLatency(1)
            );

    // Get the backbuffer for this window which is be the final 3D render target.
    ComPtr<ID3D11Texture2D> backBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&backBuffer))
        );

    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it is directly rendered to the 
    // swap chain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_IGNORE),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // Now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



Давайте подробно рассмотрим шаги, описанные в предыдущем примере кода.

1.  Выделите структуру [**\_ \_ \_ DESC1 цепочки подкачки**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) и определите параметры для [**цепочки**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)буферов.

    Эти параметры показывают пример создания цепочки буферов, которую может использовать приложение Магазина Windows.

2.  Получите адаптер, на котором выполняется [**устройство Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) и [**Устройство DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) , и получите связанный с ними объект [**идксгифактори**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) . Эту **фабрику DXGI** необходимо использовать, чтобы убедиться, что [**цепочка**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) буферов создана на том же адаптере.

3.  Вызовите метод [**IDXGIFactory2:: креатесвапчаинфоркоревиндов**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) , чтобы создать цепочку буферов. Используйте класс [**Windows:: UI:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) для главного окна приложения Магазина Windows.

    Убедитесь, что для параметра Максимальная задержка кадра задано значение 1, что снизит энергопотребление.

    Если вы хотите визуализировать содержимое Direct2D в приложении для Магазина Windows, см. метод [**креатесвапчаинфоркомпоситион**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .

4.  Получение заднего буфера из [**цепочки**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)буферов обмена. Задний буфер предоставляет интерфейс [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , выделенный **цепочкой** буферов обмена.

5.  Объявите структуру [**D2D1 \_ Bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) и задайте значения свойств. Задайте формат пикселей BGRA, так как это формат [**устройства Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) и [**устройства DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .

6.  Получите задний буфер в качестве [**идксгисурфаце**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) для передачи в Direct2D. Direct2D не принимает [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) напрямую.

    Создайте объект [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) из заднего буфера с помощью метода [**ID2D1DeviceContext:: креатебитмапфромдксгисурфаце**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .

7.  Теперь [**точечный рисунок Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) связан с задним буфером. Задайте для целевого объекта в [**контексте устройства Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) **точечный рисунок**.

## <a name="how-to-render-and-display"></a>Как отобразить и отобразить

Теперь, когда у вас есть целевой точечный рисунок, вы можете рисовать примитивы, изображения, эффекты изображения и текст с помощью [**контекста устройства Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext). В коде показано, как нарисовать прямоугольник.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);

m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



Давайте подробно рассмотрим шаги, описанные в предыдущем примере кода.

1.  Вызовите [**креатесолидколорбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , чтобы создать кисть для рисования прямоугольника.
2.  Вызовите метод [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) перед выполнением любых команд рисования.
3.  Вызовите метод [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) , прямоугольник для рисования и кисть.
4.  Вызовите метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) после завершения выдачи команд рисования.
5.  Отобразите результат, вызвав метод [**идксгисвапчаин::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) повторной отправки.

Теперь можно использовать [**контекст устройства Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) для рисования примитивов, изображений, эффектов изображения и текста на экране.

 

 