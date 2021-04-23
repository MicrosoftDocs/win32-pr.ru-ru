---
title: Краткое руководство по Direct2D
description: Содержит сводку действий, необходимых для рисования с помощью Direct2D, а также пример кода.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, пример кода рисования прямоугольника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133927"
---
# <a name="direct2d-quickstart"></a><span data-ttu-id="9bc9b-104">Краткое руководство по Direct2D</span><span class="sxs-lookup"><span data-stu-id="9bc9b-104">Direct2D QuickStart</span></span>

<span data-ttu-id="9bc9b-105">Direct2D — это API неуправляемого кода с непосредственным режимом, предназначенный для создания двухмерной графики.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="9bc9b-106">В этом разделе показано, как использовать Direct2D в обычном приложении Win32 для рисования в **HWND**.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-106">This topic illustrates how to use Direct2D within a typical Win32 application to draw to an **HWND**.</span></span>

> [!Note]  
> <span data-ttu-id="9bc9b-107">Если вы хотите создать приложение для Магазина Windows, использующее Direct2D, см. раздел [Краткое руководство по Direct2D для Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc9b-107">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="9bc9b-108">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="9bc9b-109">Рисование простого прямоугольника</span><span class="sxs-lookup"><span data-stu-id="9bc9b-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="9bc9b-110">Шаг 1. включение заголовка Direct2D</span><span class="sxs-lookup"><span data-stu-id="9bc9b-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="9bc9b-111">Шаг 2. Создание ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="9bc9b-111">Step 2: Create an ID2D1Factory</span></span>](#step-2-create-an-id2d1factory)
-   [<span data-ttu-id="9bc9b-112">Шаг 3. Создание ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="9bc9b-112">Step 3: Create an ID2D1HwndRenderTarget</span></span>](#step-3-create-an-id2d1hwndrendertarget)
-   [<span data-ttu-id="9bc9b-113">Шаг 4. Создание кисти</span><span class="sxs-lookup"><span data-stu-id="9bc9b-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="9bc9b-114">Шаг 5. Рисование прямоугольника</span><span class="sxs-lookup"><span data-stu-id="9bc9b-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="9bc9b-115">Шаг 6. освобождение ресурсов</span><span class="sxs-lookup"><span data-stu-id="9bc9b-115">Step 6: Release Resources</span></span>](#step-6-release-resources)
-   [<span data-ttu-id="9bc9b-116">Создание простого приложения Direct2D</span><span class="sxs-lookup"><span data-stu-id="9bc9b-116">Create a Simple Direct2D Application</span></span>](#create-a-simple-direct2d-application)
-   [<span data-ttu-id="9bc9b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="9bc9b-117">Related topics</span></span>](#related-topics)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="9bc9b-118">Рисование простого прямоугольника</span><span class="sxs-lookup"><span data-stu-id="9bc9b-118">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="9bc9b-119">Чтобы нарисовать прямоугольник с помощью [GDI](/windows/desktop/gdi/windows-gdi), можно обрабатывать сообщение [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-119">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="9bc9b-120">Код для рисования того же прямоугольника с Direct2D аналогичен: он создает ресурсы для рисования, описывает фигуру для рисования, рисует фигуру, а затем освобождает ресурсы рисования.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-120">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="9bc9b-121">В последующих разделах подробно описывается каждый из этих шагов.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-121">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="9bc9b-122">Шаг 1. включение заголовка Direct2D</span><span class="sxs-lookup"><span data-stu-id="9bc9b-122">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="9bc9b-123">Помимо заголовков, необходимых для приложения Win32, включите заголовок D2D1. h.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-123">In addition to the headers required for a Win32 application, include the d2d1.h header.</span></span>

## <a name="step-2-create-an-id2d1factory"></a><span data-ttu-id="9bc9b-124">Шаг 2. Создание ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="9bc9b-124">Step 2: Create an ID2D1Factory</span></span>

<span data-ttu-id="9bc9b-125">Одно из первых действий в любом Direct2D примере — создание [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="9bc9b-125">One of the first things that any Direct2D example does is create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



<span data-ttu-id="9bc9b-126">Интерфейс [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) является отправной точкой для использования Direct2D; Используйте **ID2D1Factory** для создания ресурсов Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-126">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface is the starting point for using Direct2D; use an **ID2D1Factory** to create Direct2D resources.</span></span>

<span data-ttu-id="9bc9b-127">При создании фабрики можно указать, является ли он многопотоковым или многопоточным.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-127">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="9bc9b-128">(Дополнительные сведения о многопоточных фабриках см. в примечаниях на [**странице справки ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) В этом примере создается однопотоковая фабрика.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-128">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="9bc9b-129">Как правило, приложение должно создавать фабрику один раз и хранить ее в течение жизненного цикла приложения.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-129">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1hwndrendertarget"></a><span data-ttu-id="9bc9b-130">Шаг 3. Создание ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="9bc9b-130">Step 3: Create an ID2D1HwndRenderTarget</span></span>

<span data-ttu-id="9bc9b-131">После создания фабрики используйте ее для создания целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-131">After you create a factory, use it to create a render target.</span></span>


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



<span data-ttu-id="9bc9b-132">Целевой объект отрисовки — это устройство, которое может выполнять операции рисования и создавать аппаратно-зависимые ресурсы рисования, такие как кисти.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-132">A render target is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="9bc9b-133">Различные типы целевых объектов отрисовки отображаются на разных устройствах.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-133">Different types of render targets render to different devices.</span></span> <span data-ttu-id="9bc9b-134">В предыдущем примере используется [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), который подготавливается к просмотру в части экрана.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-134">The preceding example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), which renders to a portion of the screen.</span></span>

<span data-ttu-id="9bc9b-135">По возможности целевой модуль прорисовки использует GPU для ускорения операций отрисовки и создания ресурсов рисования.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-135">When possible, a render target uses the GPU to accelerate rendering operations and create drawing resources.</span></span> <span data-ttu-id="9bc9b-136">В противном случае целевой объект прорисовки использует ЦП для обработки инструкций по отрисовке и создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-136">Otherwise, the render target uses the CPU to process rendering instructions and create resources.</span></span> <span data-ttu-id="9bc9b-137">(Это поведение можно изменить с помощью флагов [**\_ \_ \_ типа целевого объекта прорисовки D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) при создании целевого объекта рендеринга.)</span><span class="sxs-lookup"><span data-stu-id="9bc9b-137">(You can modify this behavior by using the [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) flags when you create the render target.)</span></span>

<span data-ttu-id="9bc9b-138">Метод [**креатехвндрендертаржет**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) принимает три параметра.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-138">The [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method takes three parameters.</span></span> <span data-ttu-id="9bc9b-139">Первый параметр, структура [**\_ \_ \_ свойств целевого объекта отрисовки D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , задает параметры удаленного отображения, следует ли принудительно подготавливать целевой объект отрисовки к программному или аппаратному обеспечению и dpi.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-139">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) struct, specifies remote display options, whether to force the render target to render to software or hardware, and the DPI.</span></span> <span data-ttu-id="9bc9b-140">Код в этом примере использует вспомогательную функцию [**D2D1:: рендертаржетпропертиес**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) для принятия свойств целевого объекта рендеринга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-140">The code in this example uses the [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper function to accept default render target properties.</span></span>

<span data-ttu-id="9bc9b-141">Второй параметр, [**D2D1 HWND для \_ \_ визуализации \_ целевых \_ свойств**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) структура, указывает **HWND** , для которого отображается содержимое, начальный размер целевого объекта отрисовки (в пикселях) и [**Параметры представления**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span><span class="sxs-lookup"><span data-stu-id="9bc9b-141">The second parameter, a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) struct, specifies the **HWND** to which content is rendered, the initial size of the render target (in pixels), and its [**presentation options**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span></span> <span data-ttu-id="9bc9b-142">В этом примере используется вспомогательная функция [**D2D1:: хвндрендертаржетпропертиес**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) для указания HWND и начального размера.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-142">This example uses the [**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper function to specify an HWND and initial size.</span></span> <span data-ttu-id="9bc9b-143">Он использует параметры представления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-143">It uses default presentation options.</span></span>

<span data-ttu-id="9bc9b-144">Третий параметр является адресом указателя, получающего ссылку на целевой объект прорисовки.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-144">The third parameter is the address of the pointer that receives the render target reference.</span></span>

<span data-ttu-id="9bc9b-145">При создании целевого объекта рендеринга и возможности аппаратного ускорения выделяются ресурсы на GPU компьютера.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-145">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="9bc9b-146">Создавая целевой объект рендеринга один раз и постоянно сохраняющий его, вы получаете выигрыш в производительности.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-146">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="9bc9b-147">Приложение должно создавать целевые объекты прорисовки один раз и удерживать их в течение жизненного цикла приложения или до тех пор, пока не будет получено сообщение об ошибке [**\_ повторного создания \_ D2DERR**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc9b-147">Your application should create render targets once and hold on to them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="9bc9b-148">При возникновении этой ошибки необходимо повторно создать целевой объект рендеринга (и все созданные им ресурсы).</span><span class="sxs-lookup"><span data-stu-id="9bc9b-148">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="step-4-create-a-brush"></a><span data-ttu-id="9bc9b-149">Шаг 4. Создание кисти</span><span class="sxs-lookup"><span data-stu-id="9bc9b-149">Step 4: Create a Brush</span></span>

<span data-ttu-id="9bc9b-150">Как и в случае с фабрикой, целевой объект отрисовки может создавать ресурсы рисования.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-150">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="9bc9b-151">В этом примере целевой объект прорисовки создает кисть.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-151">In this example, the render target creates a brush.</span></span>


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



<span data-ttu-id="9bc9b-152">Кисть — это объект, который закрашивает область, например штрих фигуры или заливку геометрии.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-152">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="9bc9b-153">Кисть в этом примере закрашивает область стандартным сплошным цветом, черным.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-153">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="9bc9b-154">Direct2D также предоставляет другие типы кистей: градиентные кисти для рисования линейных и радиальных градиентов, а также растровую кисть для рисования с помощью точечных рисунков и шаблонов.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-154">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, and a bitmap brush for painting with bitmaps and patterns.</span></span>

<span data-ttu-id="9bc9b-155">Некоторые API-интерфейсы рисования предоставляют перья для рисования контуров и кистей для заливки фигур.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-155">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="9bc9b-156">Direct2D отличается: он не предоставляет объект Pen, но использует кисть для рисования контуров и заливки фигур.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-156">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="9bc9b-157">При рисовании контуров используйте интерфейс [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) с кистью для управления операциями обводки пути.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-157">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface with a brush to control path stroking operations.</span></span>

<span data-ttu-id="9bc9b-158">Кисть можно использовать только с целевым объектом рендеринга, который ее создал, и с другими целевыми объектами отрисовки в том же домене ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-158">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="9bc9b-159">Как правило, необходимо создавать кисти один раз и хранить их в течение жизненного цикла целевого объекта рендеринга, который их создал.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-159">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="9bc9b-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) — это одиночное исключение; так как создание **ID2D1SolidColorBrush** является сравнительно недорогым, можно создать его каждый раз при рисовании кадра без заметного попадания в производительность.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="9bc9b-161">Можно также использовать один **ID2D1SolidColorBrush** и изменять его цвет при каждом его использовании.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-161">You can also use a single **ID2D1SolidColorBrush** and just change its color every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="9bc9b-162">Шаг 5. Рисование прямоугольника</span><span class="sxs-lookup"><span data-stu-id="9bc9b-162">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="9bc9b-163">Затем используйте целевой объект рендеринга для рисования прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-163">Next, use the render target to draw the rectangle.</span></span>


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



<span data-ttu-id="9bc9b-164">Метод [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) принимает два параметра: прямоугольник для рисования и кисть, используемую для рисования контура прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-164">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="9bc9b-165">При необходимости можно также указать ширину штриха, шаблон штриха, соединение строки и параметры конца.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-165">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="9bc9b-166">Перед выдачей команд рисования необходимо вызвать метод [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) , а после завершения выдачи команд рисования необходимо вызвать метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="9bc9b-166">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="9bc9b-167">Метод **EndDraw** возвращает **значение HRESULT** , указывающее, были ли команды рисования успешными.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-167">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span>

## <a name="step-6-release-resources"></a><span data-ttu-id="9bc9b-168">Шаг 6. освобождение ресурсов</span><span class="sxs-lookup"><span data-stu-id="9bc9b-168">Step 6: Release Resources</span></span>

<span data-ttu-id="9bc9b-169">Если для рисования больше нет кадров или получено [**D2DERR \_ повторного создания \_ целевой**](direct2d-error-codes.md) ошибки, освободите целевой объект рендеринга и все созданные им устройства.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-169">When there are no more frames to draw, or when you receive the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error, release the render target and any devices it created.</span></span>


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



<span data-ttu-id="9bc9b-170">Когда приложение завершит использование ресурсов Direct2D (например, когда он собирается завершить работу), освободите фабрику Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-170">When your application has finished using Direct2D resources (such as when it is about to exit), release the Direct2D factory.</span></span>


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a><span data-ttu-id="9bc9b-171">Создание простого приложения Direct2D</span><span class="sxs-lookup"><span data-stu-id="9bc9b-171">Create a Simple Direct2D Application</span></span>

<span data-ttu-id="9bc9b-172">В коде этого раздела показаны основные элементы приложения Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-172">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="9bc9b-173">Для краткости в разделе опущена платформа приложений и код обработки ошибок, который является характеристикой хорошо написанного приложения.</span><span class="sxs-lookup"><span data-stu-id="9bc9b-173">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span> <span data-ttu-id="9bc9b-174">Более подробное пошаговое руководство содержит полный код для создания простого приложения Direct2D и демонстрирует лучшие методики проектирования, см. раздел [Создание простого приложения Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="9bc9b-174">For a more detailed walk-through that shows the complete code for creating a simple Direct2D application and demonstrates best design practices, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bc9b-175">См. также</span><span class="sxs-lookup"><span data-stu-id="9bc9b-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bc9b-176">Создание простого приложения Direct2D</span><span class="sxs-lookup"><span data-stu-id="9bc9b-176">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

 