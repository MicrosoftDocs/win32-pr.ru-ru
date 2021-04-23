---
title: Краткое руководство по Direct2D для Windows 8
description: Содержит сводку действий, необходимых для рисования с помощью Direct2D, а также пример кода.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, пример кода рисования прямоугольника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e5cfbbf4e63e129a43bec783a64203e20e30a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654325"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="eee1a-104">Краткое руководство по Direct2D для Windows 8</span><span class="sxs-lookup"><span data-stu-id="eee1a-104">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="eee1a-105">Direct2D — это API неуправляемого кода с непосредственным режимом, предназначенный для создания двухмерной графики.</span><span class="sxs-lookup"><span data-stu-id="eee1a-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="eee1a-106">В этом разделе показано, как использовать Direct2D для рисования в [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="eee1a-106">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="eee1a-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="eee1a-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="eee1a-108">Рисование простого прямоугольника</span><span class="sxs-lookup"><span data-stu-id="eee1a-108">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="eee1a-109">Шаг 1. включение заголовка Direct2D</span><span class="sxs-lookup"><span data-stu-id="eee1a-109">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="eee1a-110">Шаг 2. Создание ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="eee1a-110">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="eee1a-111">Шаг 3. Создание ID2D1Device и ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="eee1a-111">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="eee1a-112">Шаг 4. Создание кисти</span><span class="sxs-lookup"><span data-stu-id="eee1a-112">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="eee1a-113">Шаг 5. Рисование прямоугольника</span><span class="sxs-lookup"><span data-stu-id="eee1a-113">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="eee1a-114">Пример кода</span><span class="sxs-lookup"><span data-stu-id="eee1a-114">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="eee1a-115">Рисование простого прямоугольника</span><span class="sxs-lookup"><span data-stu-id="eee1a-115">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="eee1a-116">Чтобы нарисовать прямоугольник с помощью [GDI](/windows/desktop/gdi/windows-gdi), можно обрабатывать сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="eee1a-116">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



<span data-ttu-id="eee1a-117">Код для рисования того же прямоугольника с Direct2D аналогичен: он создает ресурсы для рисования, описывает фигуру для рисования, рисует фигуру, а затем освобождает ресурсы рисования.</span><span class="sxs-lookup"><span data-stu-id="eee1a-117">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="eee1a-118">В последующих разделах подробно описывается каждый из этих шагов.</span><span class="sxs-lookup"><span data-stu-id="eee1a-118">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="eee1a-119">Шаг 1. включение заголовка Direct2D</span><span class="sxs-lookup"><span data-stu-id="eee1a-119">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="eee1a-120">Помимо заголовков, необходимых для приложения, включите заголовки D2D1. h и D2D1 \_ 1. h.</span><span class="sxs-lookup"><span data-stu-id="eee1a-120">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="eee1a-121">Шаг 2. Создание ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="eee1a-121">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="eee1a-122">Одно из первых действий в любом Direct2D примере — создание [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span><span class="sxs-lookup"><span data-stu-id="eee1a-122">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



<span data-ttu-id="eee1a-123">Интерфейс [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) является отправной точкой для использования Direct2D; Используйте **ID2D1Factory1** для создания ресурсов Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eee1a-123">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="eee1a-124">При создании фабрики можно указать, является ли он многопотоковым или многопоточным.</span><span class="sxs-lookup"><span data-stu-id="eee1a-124">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="eee1a-125">(Дополнительные сведения о многопоточных фабриках см. в примечаниях на [**странице справки ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) В этом примере создается однопотоковая фабрика.</span><span class="sxs-lookup"><span data-stu-id="eee1a-125">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="eee1a-126">Как правило, приложение должно создавать фабрику один раз и хранить ее в течение жизненного цикла приложения.</span><span class="sxs-lookup"><span data-stu-id="eee1a-126">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="eee1a-127">Шаг 3. Создание ID2D1Device и ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="eee1a-127">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="eee1a-128">После создания фабрики используйте ее для создания устройства Direct2D, а затем используйте устройство для создания контекста устройства Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eee1a-128">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="eee1a-129">Чтобы создать эти объекты Direct2D, необходимо иметь [**устройство Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , [**Устройство DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)и [**цепочку подкачки DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="eee1a-129">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="eee1a-130">Сведения о создании необходимых компонентов см. в разделе [устройства и контексты устройств](devices-and-device-contexts.md) .</span><span class="sxs-lookup"><span data-stu-id="eee1a-130">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="eee1a-131">Контекст устройства — это устройство, которое может выполнять операции рисования и создавать аппаратно-зависимые ресурсы рисования, такие как кисти.</span><span class="sxs-lookup"><span data-stu-id="eee1a-131">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="eee1a-132">Вы также используете контекст устройства, чтобы связать [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) с поверхностью DXGI для использования в качестве целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="eee1a-132">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="eee1a-133">Контекст устройства может быть отображен в разные типы целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="eee1a-133">The device context can render to different types of targets.</span></span>

<span data-ttu-id="eee1a-134">В этом примере кода объявляются свойства точечного рисунка, ссылающегося на цепочку подкачки DXGI, которая подготавливается к [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="eee1a-134">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="eee1a-135">Метод [**ID2D1DeviceContext:: креатебитмапфромдксгисурфаце**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) получает поверхность Direct2D из поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="eee1a-135">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="eee1a-136">Это делает его таким образом, чтобы все содержимое, отображаемое в целевой [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , отображалось на поверхности цепочки буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="eee1a-136">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="eee1a-137">Получив поверхность Direct2D, используйте метод [**ID2D1DeviceContext:: сеттаржет**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) , чтобы задать его в качестве активного целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="eee1a-137">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
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

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a><span data-ttu-id="eee1a-138">Шаг 4. Создание кисти</span><span class="sxs-lookup"><span data-stu-id="eee1a-138">Step 4: Create a Brush</span></span>

<span data-ttu-id="eee1a-139">Как и в случае с фабрикой, контекст устройства может создавать ресурсы рисования.</span><span class="sxs-lookup"><span data-stu-id="eee1a-139">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="eee1a-140">В этом примере контекст устройства создает кисть.</span><span class="sxs-lookup"><span data-stu-id="eee1a-140">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="eee1a-141">Кисть — это объект, который закрашивает область, например штрих фигуры или заливку геометрии.</span><span class="sxs-lookup"><span data-stu-id="eee1a-141">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="eee1a-142">Кисть в этом примере закрашивает область стандартным сплошным цветом, черным.</span><span class="sxs-lookup"><span data-stu-id="eee1a-142">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="eee1a-143">Direct2D также предоставляет другие типы кистей: градиентные кисти для рисования линейных и радиальных градиентов, [**растровую кисть**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) для рисования с помощью точечных рисунков и узоров, а также начиная с Windows 8 — [**кисть изображения**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) для рисования с помощью подготовленного изображения.</span><span class="sxs-lookup"><span data-stu-id="eee1a-143">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="eee1a-144">Некоторые API-интерфейсы рисования предоставляют перья для рисования контуров и кистей для заливки фигур.</span><span class="sxs-lookup"><span data-stu-id="eee1a-144">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="eee1a-145">Direct2D отличается: он не предоставляет объект Pen, но использует кисть для рисования контуров и заливки фигур.</span><span class="sxs-lookup"><span data-stu-id="eee1a-145">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="eee1a-146">При рисовании контуров используйте интерфейс [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) или начиная с Windows 8 интерфейс [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) с кистью для управления обводками пути.</span><span class="sxs-lookup"><span data-stu-id="eee1a-146">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="eee1a-147">Кисть можно использовать только с целевым объектом рендеринга, который ее создал, и с другими целевыми объектами отрисовки в том же домене ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eee1a-147">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="eee1a-148">Как правило, необходимо создавать кисти один раз и хранить их в течение жизненного цикла целевого объекта рендеринга, который их создал.</span><span class="sxs-lookup"><span data-stu-id="eee1a-148">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="eee1a-149">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) — это одиночное исключение; так как создание **ID2D1SolidColorBrush** является сравнительно недорогым, можно создать его каждый раз при рисовании кадра без заметного попадания в производительность.</span><span class="sxs-lookup"><span data-stu-id="eee1a-149">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="eee1a-150">Можно также использовать один **ID2D1SolidColorBrush** и изменять его цвет или непрозрачность каждый раз, когда вы его используете.</span><span class="sxs-lookup"><span data-stu-id="eee1a-150">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="eee1a-151">Шаг 5. Рисование прямоугольника</span><span class="sxs-lookup"><span data-stu-id="eee1a-151">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="eee1a-152">Затем используйте контекст устройства для рисования прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="eee1a-152">Next, use the device context to draw the rectangle.</span></span>


```C++
 
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



<span data-ttu-id="eee1a-153">Метод [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) принимает два параметра: прямоугольник для рисования и кисть, используемую для рисования контура прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="eee1a-153">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="eee1a-154">При необходимости можно также указать ширину штриха, шаблон штриха, соединение строки и параметры конца.</span><span class="sxs-lookup"><span data-stu-id="eee1a-154">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="eee1a-155">Перед выдачей команд рисования необходимо вызвать метод [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) , а после завершения выдачи команд рисования необходимо вызвать метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="eee1a-155">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="eee1a-156">Метод **EndDraw** возвращает **значение HRESULT** , указывающее, были ли команды рисования успешными.</span><span class="sxs-lookup"><span data-stu-id="eee1a-156">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="eee1a-157">Если это не удалось, вспомогательная функция Сровиффаилед выдаст исключение.</span><span class="sxs-lookup"><span data-stu-id="eee1a-157">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="eee1a-158">Метод повторной отправки [**идксгисвапчаин::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) перемещает поверхность буфера на экран на поверхности экрана для отображения результата.</span><span class="sxs-lookup"><span data-stu-id="eee1a-158">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="eee1a-159">пример кода</span><span class="sxs-lookup"><span data-stu-id="eee1a-159">Example code</span></span>

<span data-ttu-id="eee1a-160">В коде этого раздела показаны основные элементы приложения Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eee1a-160">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="eee1a-161">Для краткости в разделе опущена платформа приложений и код обработки ошибок, который является характеристикой хорошо написанного приложения.</span><span class="sxs-lookup"><span data-stu-id="eee1a-161">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 