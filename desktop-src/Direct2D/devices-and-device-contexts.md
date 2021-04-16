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
# <a name="how-to-render-by-using-a-direct2d-device-context"></a><span data-ttu-id="f7f6f-105">Подготовка к просмотру с помощью контекста устройства Direct2D</span><span class="sxs-lookup"><span data-stu-id="f7f6f-105">How to render by using a Direct2D device context</span></span>

<span data-ttu-id="f7f6f-106">В этом разделе вы узнаете, как создать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-106">In this topic you will learn about creating [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8.</span></span> <span data-ttu-id="f7f6f-107">Эти сведения относятся к вам при разработке приложений для Магазина Windows или классических приложений с помощью Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-107">This information applies to you if you are developing Windows Store apps or a desktop app by using Direct2D.</span></span> <span data-ttu-id="f7f6f-108">В этом разделе описывается назначение объектов контекста устройства Direct2D, создание этого объекта и пошаговое руководство по отрисовке и отображению примитивов и изображений Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-108">This topic describes the purpose of Direct2D device context objects, how to create that object , and a step by step guide about rendering and displaying Direct2D primitives and images.</span></span> <span data-ttu-id="f7f6f-109">Кроме того, вы узнаете о переключении целевых объектов рендеринга и добавлении эффектов в приложение.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-109">You will also learn about switching render targets and adding effects to your app.</span></span>

-   [<span data-ttu-id="f7f6f-110">Что такое устройство Direct2D?</span><span class="sxs-lookup"><span data-stu-id="f7f6f-110">What is a Direct2D device?</span></span>](#what-is-a-direct2d-device)
-   [<span data-ttu-id="f7f6f-111">Что такое контекст устройства Direct2D?</span><span class="sxs-lookup"><span data-stu-id="f7f6f-111">What is a Direct2D device context?</span></span>](#what-is-a-direct2d-device-context)
-   [<span data-ttu-id="f7f6f-112">Подготовка к просмотру с помощью Direct2D в Windows 8</span><span class="sxs-lookup"><span data-stu-id="f7f6f-112">Rendering with Direct2D on Windows 8</span></span>](#rendering-with-direct2d-on-windows-8)
-   [<span data-ttu-id="f7f6f-113">Зачем использовать контекст устройства для подготовки к просмотру?</span><span class="sxs-lookup"><span data-stu-id="f7f6f-113">Why use a device context to render?</span></span>](#why-use-a-device-context-to-render)
-   [<span data-ttu-id="f7f6f-114">Создание контекста устройства Direct2D для подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="f7f6f-114">How to create a Direct2D device context for rendering</span></span>](#how-to-create-a-direct2d-device-context-for-rendering)
-   [<span data-ttu-id="f7f6f-115">Выбор целевого объекта</span><span class="sxs-lookup"><span data-stu-id="f7f6f-115">Selecting a target</span></span>](#selecting-a-target)
-   [<span data-ttu-id="f7f6f-116">Как отобразить и отобразить</span><span class="sxs-lookup"><span data-stu-id="f7f6f-116">How to render and display</span></span>](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a><span data-ttu-id="f7f6f-117">Что такое устройство Direct2D?</span><span class="sxs-lookup"><span data-stu-id="f7f6f-117">What is a Direct2D device?</span></span>

<span data-ttu-id="f7f6f-118">Для создания контекста устройства Direct2D требуется устройство Direct2D и устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-118">You need a Direct2D device and a Direct3D device to create a Direct2D device context.</span></span> <span data-ttu-id="f7f6f-119">[**Устройство Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (предоставляет указатель на интерфейс **ID2D1Device** ) представляет адаптер дисплея.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-119">A [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (exposes an **ID2D1Device** interface pointer) represents a display adapter.</span></span> <span data-ttu-id="f7f6f-120">Устройство Direct3D (предоставляет указатель на интерфейс [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) связывается с устройством Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-120">A Direct3D device (exposes an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) interface pointer) is associated with a Direct2D device.</span></span> <span data-ttu-id="f7f6f-121">Каждое приложение должно иметь одно **устройство Direct2D**, но может иметь более одного **устройства**.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-121">Each app must have one **Direct2D device**, but can have more than one **device**.</span></span>

## <a name="what-is-a-direct2d-device-context"></a><span data-ttu-id="f7f6f-122">Что такое контекст устройства Direct2D?</span><span class="sxs-lookup"><span data-stu-id="f7f6f-122">What is a Direct2D device context?</span></span>

<span data-ttu-id="f7f6f-123">[**Контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) (предоставляет указатель на интерфейс **ID2D1DeviceContext** ) представляет набор состояний и буферов команд, которые используются для отображения в целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-123">A [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (exposes an **ID2D1DeviceContext** interface pointer) represents a set of state and command buffers that you use to render to a target.</span></span> <span data-ttu-id="f7f6f-124">Вы можете вызывать методы в контексте устройства для задания состояния конвейера и создания команд отрисовки с помощью ресурсов, принадлежащих устройству.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-124">You can call methods on the device context to set pipeline state and generate rendering commands by using the resources owned by a device.</span></span>

## <a name="rendering-with-direct2d-on-windows-8"></a><span data-ttu-id="f7f6f-125">Подготовка к просмотру с помощью Direct2D в Windows 8</span><span class="sxs-lookup"><span data-stu-id="f7f6f-125">Rendering with Direct2D on Windows 8</span></span>

<span data-ttu-id="f7f6f-126">В Windows 7 и более ранних версиях вы используете [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) или другой целевой интерфейс рендеринга для отображения в окне или на поверхности.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-126">On Windows 7 and earlier, you use a [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) or another render target interface to render to a window or surface.</span></span> <span data-ttu-id="f7f6f-127">Начиная с Windows 8, мы не рекомендуем выполнять отрисовку с помощью методов, зависящих от интерфейсов, таких как **ID2D1HwndRenderTarget** , так как они не работают с приложениями Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-127">Starting with Windows 8, we do not recommend rendering by using methods that rely on interfaces like **ID2D1HwndRenderTarget** because they won't work with Windows Store apps.</span></span> <span data-ttu-id="f7f6f-128">Вы можете использовать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) для отображения в HWND, если хотите создать классическое приложение и использовать преимущества дополнительных функций **контекста устройства** .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-128">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to render to an Hwnd if you want to make a desktop app and still take advantage of the **device context's** additional features.</span></span> <span data-ttu-id="f7f6f-129">Однако для отображения содержимого в приложениях Магазина Windows с помощью [Direct2D](./direct2d-portal.md)требуется **контекст устройства** .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-129">However, the **device context** is required to render content in a Windows Store apps with [Direct2D](./direct2d-portal.md).</span></span>

## <a name="why-use-a-device-context-to-render"></a><span data-ttu-id="f7f6f-130">Зачем использовать контекст устройства для подготовки к просмотру?</span><span class="sxs-lookup"><span data-stu-id="f7f6f-130">Why use a device context to render?</span></span>

-   <span data-ttu-id="f7f6f-131">Можно визуализировать приложения для Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-131">You can render for Windows Store apps.</span></span>
-   <span data-ttu-id="f7f6f-132">Целевой объект отрисовки можно изменить в любое время до, во время и после отрисовки.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-132">You can change the render target at any time before, during, and after rendering.</span></span> <span data-ttu-id="f7f6f-133">Контекст устройства гарантирует, что вызовы методов рисования выполняются по порядку и применяют их при переключении целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-133">The device context ensures that the calls to drawing methods are executed in order and applies them when you switch the render target.</span></span>
-   <span data-ttu-id="f7f6f-134">В контексте устройства можно использовать более одного типа окон.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-134">You can use more than one type of window with a device context.</span></span> <span data-ttu-id="f7f6f-135">Вы можете использовать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) и [**цепочку подкачки DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) для непосредственного отображения в [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) или в [**Windows:: UI:: XAML:: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span><span class="sxs-lookup"><span data-stu-id="f7f6f-135">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) to render directly to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) or a [**Windows::UI::XAML::SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span></span>
-   <span data-ttu-id="f7f6f-136">Вы можете использовать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) для создания [эффектов Direct2D](effects-overview.md) и визуализации выходных данных эффекта изображения или графа эффектов в целевой объект прорисовки.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-136">You can use the [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to create [Direct2D effects](effects-overview.md) and to render the output of an image effect or effect graph to a render target.</span></span>
-   <span data-ttu-id="f7f6f-137">Можно использовать несколько [**контекстов устройств**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), что может быть полезно для повышения производительности в многопоточном приложении.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-137">You can have multiple [**device contexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), which can be helpful for improving performance in a threaded app.</span></span> <span data-ttu-id="f7f6f-138">Дополнительные сведения см. в разделе [многопоточные приложения Direct2D](multi-threaded-direct2d-apps.md) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-138">See [Multithreaded Direct2D apps](multi-threaded-direct2d-apps.md) for more information.</span></span>
-   <span data-ttu-id="f7f6f-139">[**Контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) тесно взаимодействует с Direct3D, обеспечивая вам больше доступа к параметрам Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-139">The [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interoperates closely with Direct3D, giving you more access to Direct3D options.</span></span>

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a><span data-ttu-id="f7f6f-140">Создание контекста устройства Direct2D для подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="f7f6f-140">How to create a Direct2D device context for rendering</span></span>

<span data-ttu-id="f7f6f-141">В этом примере кода показано, как создать устройство Direct3D11, получить связанное устройство DXGI, создать [**устройство Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)и, наконец, создать [**контекст устройства**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-141">The code here shows you how to create a Direct3D11 device, get the associated DXGI device, create a [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), and then finally create the Direct2D [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) for rendering.</span></span>

<span data-ttu-id="f7f6f-142">Ниже приведена схема вызовов методов и интерфейсов, используемых этим кодом.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-142">Here is a diagram of the method calls and the interfaces this code uses.</span></span>

![Схема устройств Direct2D и Direct3D и контекстов устройств.](images/devicecontextdiagram.png)

> [!Note]  
> <span data-ttu-id="f7f6f-144">В этом коде предполагается, что у вас уже есть объект [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) . Дополнительные сведения см. на [**странице справочника по ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="f7f6f-144">This code assumes you already have an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) object, for more information see the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>

 


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



<span data-ttu-id="f7f6f-145">Давайте подробно рассмотрим шаги, описанные в предыдущем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-145">Let's walk through the steps in the preceding code sample.</span></span>

1.  <span data-ttu-id="f7f6f-146">Получите указатель интерфейса ID3D11Device, который потребуется для создания контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-146">Get an ID3D11Device interface pointer you will need this to create the device context.</span></span>

    -   <span data-ttu-id="f7f6f-147">Объявите флаги создания, чтобы настроить устройство [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) для поддержки BGRA.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-147">Declare the creation flags to set up the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) device for BGRA support.</span></span> <span data-ttu-id="f7f6f-148">Для [Direct2D](./direct2d-portal.md) требуется BGRA цветовой порядок.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-148">[Direct2D](./direct2d-portal.md) requires BGRA color order.</span></span>
    -   <span data-ttu-id="f7f6f-149">Объявите массив записей [**\_ \_ уровня компонента D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) , представляющих набор уровней компонентов, которые будет поддерживать ваше приложение.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-149">Declare an array of [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) entries representing the set of feature levels that your app will support.</span></span>
        > [!Note]  
        > <span data-ttu-id="f7f6f-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) выполняет поиск в списке, пока не найдет уровень компонентов, поддерживаемый основной системой.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) searches your list until it finds the feature level supported by the host system.</span></span>

         

    -   <span data-ttu-id="f7f6f-151">Используйте функцию [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) для создания объекта [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) , функция также возвращает объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , но этот объект не требуется для этого примера.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-151">Use the [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) function to create an [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) object, the function will also return an [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) object, but that object is not needed for this example.</span></span>

2.  <span data-ttu-id="f7f6f-152">Запросите [**устройство Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) для своего интерфейса [**устройства DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-152">Query the [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) for its [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) interface.</span></span>
3.  <span data-ttu-id="f7f6f-153">Создайте объект [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) , вызвав метод [**ID2D1Factory:: креатедевице**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) и передав объект [**идксгидевице**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-153">Create an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) object by calling the [**ID2D1Factory::CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) method and passing in the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) object.</span></span>
4.  <span data-ttu-id="f7f6f-154">Создайте указатель [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) с помощью метода [**ID2D1Device:: креатедевицеконтекст**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-154">Create an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pointer using the [**ID2D1Device::CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) method.</span></span>

## <a name="selecting-a-target"></a><span data-ttu-id="f7f6f-155">Выбор целевого объекта</span><span class="sxs-lookup"><span data-stu-id="f7f6f-155">Selecting a target</span></span>

<span data-ttu-id="f7f6f-156">В этом примере кода показано, как получить [**двухмерную текстуру Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) для буфера окна и создать цель точечного рисунка, ссылающуюся на эту текстуру, в которую визуализируется [**контекст устройства Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-156">The code here shows you how to get the [**2 dimensional Direct3D texture**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) for the window back buffer and create a bitmap target that links to this texture to which the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) renders.</span></span>


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



<span data-ttu-id="f7f6f-157">Давайте подробно рассмотрим шаги, описанные в предыдущем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-157">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="f7f6f-158">Выделите структуру [**\_ \_ \_ DESC1 цепочки подкачки**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) и определите параметры для [**цепочки**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)буферов.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-158">Allocate a [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and define the settings for the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

    <span data-ttu-id="f7f6f-159">Эти параметры показывают пример создания цепочки буферов, которую может использовать приложение Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-159">These settings show an example of how to create a swap chain that a Windows Store app can use.</span></span>

2.  <span data-ttu-id="f7f6f-160">Получите адаптер, на котором выполняется [**устройство Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) и [**Устройство DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) , и получите связанный с ними объект [**идксгифактори**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-160">Get the adapter that the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) are running on and get the [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) object associated with them.</span></span> <span data-ttu-id="f7f6f-161">Эту **фабрику DXGI** необходимо использовать, чтобы убедиться, что [**цепочка**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) буферов создана на том же адаптере.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-161">You must use this **DXGI factory** to ensure the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) is created on the same adapter.</span></span>

3.  <span data-ttu-id="f7f6f-162">Вызовите метод [**IDXGIFactory2:: креатесвапчаинфоркоревиндов**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) , чтобы создать цепочку буферов.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-162">Call the [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) method to create the swap chain.</span></span> <span data-ttu-id="f7f6f-163">Используйте класс [**Windows:: UI:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) для главного окна приложения Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-163">Use the [**Windows::UI::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) class for the main window of a Windows Store app.</span></span>

    <span data-ttu-id="f7f6f-164">Убедитесь, что для параметра Максимальная задержка кадра задано значение 1, что снизит энергопотребление.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-164">Make sure to set the maximum frame latency to 1 to minimize power consumption.</span></span>

    <span data-ttu-id="f7f6f-165">Если вы хотите визуализировать содержимое Direct2D в приложении для Магазина Windows, см. метод [**креатесвапчаинфоркомпоситион**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-165">If you want to render Direct2D content in a Windows Store app, see the [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method.</span></span>

4.  <span data-ttu-id="f7f6f-166">Получение заднего буфера из [**цепочки**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-166">Get the back buffer from the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span> <span data-ttu-id="f7f6f-167">Задний буфер предоставляет интерфейс [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , выделенный **цепочкой** буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-167">The back buffer exposes an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) interface allocated by the **swap chain**</span></span>

5.  <span data-ttu-id="f7f6f-168">Объявите структуру [**D2D1 \_ Bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) и задайте значения свойств.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-168">Declare a [**D2D1\_BITMAP\_PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct and set the property values.</span></span> <span data-ttu-id="f7f6f-169">Задайте формат пикселей BGRA, так как это формат [**устройства Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) и [**устройства DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-169">Set the pixel format to BGRA because this is the format the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) use.</span></span>

6.  <span data-ttu-id="f7f6f-170">Получите задний буфер в качестве [**идксгисурфаце**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) для передачи в Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-170">Get the back buffer as an [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) to pass to Direct2D.</span></span> <span data-ttu-id="f7f6f-171">Direct2D не принимает [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) напрямую.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-171">Direct2D doesn't accept an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directly.</span></span>

    <span data-ttu-id="f7f6f-172">Создайте объект [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) из заднего буфера с помощью метода [**ID2D1DeviceContext:: креатебитмапфромдксгисурфаце**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .</span><span class="sxs-lookup"><span data-stu-id="f7f6f-172">Create a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object from the back buffer using the [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method.</span></span>

7.  <span data-ttu-id="f7f6f-173">Теперь [**точечный рисунок Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) связан с задним буфером.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-173">Now the [**Direct2D bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is linked to the back buffer.</span></span> <span data-ttu-id="f7f6f-174">Задайте для целевого объекта в [**контексте устройства Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) **точечный рисунок**.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-174">Set the target on the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to the **bitmap**.</span></span>

## <a name="how-to-render-and-display"></a><span data-ttu-id="f7f6f-175">Как отобразить и отобразить</span><span class="sxs-lookup"><span data-stu-id="f7f6f-175">How to render and display</span></span>

<span data-ttu-id="f7f6f-176">Теперь, когда у вас есть целевой точечный рисунок, вы можете рисовать примитивы, изображения, эффекты изображения и текст с помощью [**контекста устройства Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span><span class="sxs-lookup"><span data-stu-id="f7f6f-176">Now that you have a target bitmap, you can draw primitives, images, image effects, and text to it using the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span> <span data-ttu-id="f7f6f-177">В коде показано, как нарисовать прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-177">The code here shows you how to draw a rectangle.</span></span>


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



<span data-ttu-id="f7f6f-178">Давайте подробно рассмотрим шаги, описанные в предыдущем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-178">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="f7f6f-179">Вызовите [**креатесолидколорбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , чтобы создать кисть для рисования прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-179">Call the [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) to create a brush to paint the rectangle.</span></span>
2.  <span data-ttu-id="f7f6f-180">Вызовите метод [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) перед выполнением любых команд рисования.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-180">Call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands.</span></span>
3.  <span data-ttu-id="f7f6f-181">Вызовите метод [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) , прямоугольник для рисования и кисть.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-181">Call the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method the rectangle to be drawn and the brush.</span></span>
4.  <span data-ttu-id="f7f6f-182">Вызовите метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) после завершения выдачи команд рисования.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-182">Call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span>
5.  <span data-ttu-id="f7f6f-183">Отобразите результат, вызвав метод [**идксгисвапчаин::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) повторной отправки.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-183">Display the result by calling the [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method.</span></span>

<span data-ttu-id="f7f6f-184">Теперь можно использовать [**контекст устройства Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) для рисования примитивов, изображений, эффектов изображения и текста на экране.</span><span class="sxs-lookup"><span data-stu-id="f7f6f-184">Now you can use the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) draw primitives, images, image effects, and text to the screen.</span></span>

 

 