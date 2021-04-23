---
title: Общие сведения о целевых объектах рендеринга
description: Описывает различные типы целевых объектов рендеринга Direct2D и их использование.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, целевые объекты отрисовки
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987637"
---
# <a name="render-targets-overview"></a><span data-ttu-id="d7e64-104">Общие сведения о целевых объектах рендеринга</span><span class="sxs-lookup"><span data-stu-id="d7e64-104">Render Targets Overview</span></span>

<span data-ttu-id="d7e64-105">Целевой объект отрисовки — это ресурс, который наследует от интерфейса [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="d7e64-105">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="d7e64-106">Целевой объект прорисовки создает ресурсы для рисования и выполняет фактические операции рисования.</span><span class="sxs-lookup"><span data-stu-id="d7e64-106">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="d7e64-107">В этом разделе описываются различные типы целевых объектов рендеринга Direct2D и способы их использования.</span><span class="sxs-lookup"><span data-stu-id="d7e64-107">This topic describes the different types of Direct2D render targets and how to use them.</span></span>

-   [<span data-ttu-id="d7e64-108">Целевые объекты рендеринга</span><span class="sxs-lookup"><span data-stu-id="d7e64-108">Render Targets</span></span>](#render-targets-overview)
    -   [<span data-ttu-id="d7e64-109">Функции целевого объекта прорисовки</span><span class="sxs-lookup"><span data-stu-id="d7e64-109">Render Target Features</span></span>](#render-target-features)
    -   [<span data-ttu-id="d7e64-110">Целевые ресурсы рендеринга</span><span class="sxs-lookup"><span data-stu-id="d7e64-110">Render Target Resources</span></span>](#render-target-resources)
    -   [<span data-ttu-id="d7e64-111">Команды рисования</span><span class="sxs-lookup"><span data-stu-id="d7e64-111">Drawing Commands</span></span>](#drawing-commands)
    -   [<span data-ttu-id="d7e64-112">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="d7e64-112">Error Handling</span></span>](#error-handling)
-   [<span data-ttu-id="d7e64-113">Пример: отрисовка содержимого в окне</span><span class="sxs-lookup"><span data-stu-id="d7e64-113">Example: Render Content to a Window</span></span>](#example-render-content-to-a-window)

## <a name="render-targets"></a><span data-ttu-id="d7e64-114">Целевые объекты рендеринга</span><span class="sxs-lookup"><span data-stu-id="d7e64-114">Render Targets</span></span>

<span data-ttu-id="d7e64-115">Целевой объект отрисовки — это ресурс, который наследует от интерфейса [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="d7e64-115">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="d7e64-116">Целевой объект прорисовки создает ресурсы для рисования и выполняет фактические операции рисования.</span><span class="sxs-lookup"><span data-stu-id="d7e64-116">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="d7e64-117">Существует несколько видов целевых объектов отрисовки, которые можно использовать для визуализации графики следующими способами.</span><span class="sxs-lookup"><span data-stu-id="d7e64-117">There are several kinds of render targets that can be used to render graphics in the following ways:</span></span>

-   <span data-ttu-id="d7e64-118">Объекты [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) отображают содержимое в окне.</span><span class="sxs-lookup"><span data-stu-id="d7e64-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects render content to a window.</span></span>
-   <span data-ttu-id="d7e64-119">Объекты [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) отрисовывается в контексте устройства GDI.</span><span class="sxs-lookup"><span data-stu-id="d7e64-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) objects render to a GDI device context.</span></span>
-   <span data-ttu-id="d7e64-120">Целевые объекты прорисовки растрового изображения отображают содержимое на экран, расположенный на экране.</span><span class="sxs-lookup"><span data-stu-id="d7e64-120">Bitmap render target objects render content to an off-screen bitmap.</span></span>
-   <span data-ttu-id="d7e64-121">Объекты для визуализации объекта DXGI визуализируются на поверхности DXGI для использования с Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d7e64-121">DXGI render target objects render to a DXGI surface for use with Direct3D.</span></span>

<span data-ttu-id="d7e64-122">Так как целевой объект прорисовки связан с конкретным устройством отрисовки, это ресурс, зависящий от устройства, и прекращает работу при удалении устройства.</span><span class="sxs-lookup"><span data-stu-id="d7e64-122">Because a render target is associated with a particular rendering device, it is a device-dependent resource and ceases to function if the device is removed.</span></span>

### <a name="render-target-features"></a><span data-ttu-id="d7e64-123">Функции целевого объекта прорисовки</span><span class="sxs-lookup"><span data-stu-id="d7e64-123">Render Target Features</span></span>

<span data-ttu-id="d7e64-124">Можно указать, использует ли целевой объект прорисовки аппаратное ускорение и отображается ли удаленное отображение на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d7e64-124">You can specify whether a render target uses hardware acceleration and whether remote display is rendered by a local or a remote computer.</span></span> <span data-ttu-id="d7e64-125">Целевые объекты отрисовки могут быть настроены для отрисовки с псевдонимами или сглаженными.</span><span class="sxs-lookup"><span data-stu-id="d7e64-125">Render targets can be set up for aliased or antialiased rendering.</span></span> <span data-ttu-id="d7e64-126">Для визуализации сцен с большим количеством примитивов разработчик может также визуализировать плоскую графику в режиме с псевдонимами и использовать многовыборочную раскрывающий сглаживание для достижения большей масштабируемости.</span><span class="sxs-lookup"><span data-stu-id="d7e64-126">For rendering scenes with a large number of primitives, a developer can also render 2-D graphics in aliased mode and use D3D multisample antialiasing to achieve greater scalability.</span></span>

<span data-ttu-id="d7e64-127">Целевые объекты рендеринга также могут группировать операции рисования в слои, представленные интерфейсом [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) .</span><span class="sxs-lookup"><span data-stu-id="d7e64-127">Render targets can also group drawing operations into layers represented by the [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) interface.</span></span> <span data-ttu-id="d7e64-128">Слои удобно использовать для сбора операций рисования, объединяемых вместе при отрисовке кадра.</span><span class="sxs-lookup"><span data-stu-id="d7e64-128">Layers are useful for collecting drawing operations to be composited together when rendering a frame.</span></span> <span data-ttu-id="d7e64-129">В некоторых сценариях это может быть полезной альтернативой для подготовки к просмотру целевого объекта прорисовки изображения, а затем повторного использования содержимого растрового изображения, так как затраты на распределение для уровней ниже, чем для [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="d7e64-129">For some scenarios, this can be a useful alternative to rendering to a bitmap render target, and then reusing the bitmap contents, as allocation costs for layering are lower than for an [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span></span>

<span data-ttu-id="d7e64-130">Целевые объекты рендеринга могут создавать новые объекты рендеринга, совместимые с самими, что полезно для промежуточного отображения на экране, сохраняя различные свойства целевого объекта рендеринга, установленные в исходном объекте.</span><span class="sxs-lookup"><span data-stu-id="d7e64-130">Render targets can create new render targets that are compatible with themselves, which is useful for intermediate off-screen rendering while retaining the various render-target properties that were set on the original.</span></span>

<span data-ttu-id="d7e64-131">Также можно выполнить отрисовку с помощью GDI для целевого объекта отрисовки Direct2D, вызвав [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в целевом объекте прорисовки для [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), который содержит методы [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) и [**релеаседк**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) , которые можно использовать для получения контекста устройства GDI.</span><span class="sxs-lookup"><span data-stu-id="d7e64-131">It is also possible to render using GDI on a Direct2D render target by calling [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a render target for [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which has [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) and [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) methods on it that can be used to retrieve a GDI device context.</span></span> <span data-ttu-id="d7e64-132">Отрисовка через GDI возможна только в том случае, если целевой объект прорисовки был создан с установленным флагом [**D2D1 \_ рендеринга, \_ \_ \_ \_ совместимым с GDI**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) .</span><span class="sxs-lookup"><span data-stu-id="d7e64-132">Rendering via GDI is possible only if the render target was created with the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag set.</span></span> <span data-ttu-id="d7e64-133">Это полезно для приложений, которые в основном подготавливаются к работе с Direct2D, но имеют модель расширяемости или другое устаревшее содержимое, которое требует возможности отрисовки с помощью GDI.</span><span class="sxs-lookup"><span data-stu-id="d7e64-133">This is useful for applications that are primarily rendering with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span> <span data-ttu-id="d7e64-134">Дополнительные сведения см. в статье [Общие сведения о взаимооперациях Direct2D и GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d7e64-134">For more information, see the [Direct2D and GDI Interoperation Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

### <a name="render-target-resources"></a><span data-ttu-id="d7e64-135">Целевые ресурсы рендеринга</span><span class="sxs-lookup"><span data-stu-id="d7e64-135">Render Target Resources</span></span>

<span data-ttu-id="d7e64-136">Как и в случае с фабрикой, целевой объект отрисовки может создавать ресурсы рисования.</span><span class="sxs-lookup"><span data-stu-id="d7e64-136">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="d7e64-137">Все ресурсы, созданные целевым объектом рендеринга, — это ресурсы, зависящие от устройства (как и в целевом объекте прорисовки).</span><span class="sxs-lookup"><span data-stu-id="d7e64-137">Any resources created by a render target are device-dependent resources (just like the render target).</span></span> <span data-ttu-id="d7e64-138">Целевой объект прорисовки может создавать ресурсы следующих типов:</span><span class="sxs-lookup"><span data-stu-id="d7e64-138">A render target can create the following types of resources:</span></span>

-   <span data-ttu-id="d7e64-139">Растровые изображения</span><span class="sxs-lookup"><span data-stu-id="d7e64-139">Bitmaps</span></span>
-   <span data-ttu-id="d7e64-140">Кисти</span><span class="sxs-lookup"><span data-stu-id="d7e64-140">Brushes</span></span>
-   <span data-ttu-id="d7e64-141">Слои</span><span class="sxs-lookup"><span data-stu-id="d7e64-141">Layers</span></span>
-   <span data-ttu-id="d7e64-142">Сетки</span><span class="sxs-lookup"><span data-stu-id="d7e64-142">Meshes</span></span>

### <a name="drawing-commands"></a><span data-ttu-id="d7e64-143">Команды рисования</span><span class="sxs-lookup"><span data-stu-id="d7e64-143">Drawing Commands</span></span>

<span data-ttu-id="d7e64-144">Для отображения содержимого используются методы рисования целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="d7e64-144">To render content, you use the render target drawing methods.</span></span> <span data-ttu-id="d7e64-145">Перед началом рисования вызовите метод [**ID2D1RenderTarget:: бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) .</span><span class="sxs-lookup"><span data-stu-id="d7e64-145">Before you begin drawing, you call the [**ID2D1RenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method.</span></span> <span data-ttu-id="d7e64-146">После завершения рисования вызовите метод [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="d7e64-146">After you finished drawing, you call the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="d7e64-147">Между этими вызовами используются методы рисования и заливки для отрисовки ресурсов рисования.</span><span class="sxs-lookup"><span data-stu-id="d7e64-147">Between these calls, you use Draw and Fill methods to render drawing resources.</span></span> <span data-ttu-id="d7e64-148">Большинство методов рисования и заливки принимают фигуру (либо примитив, либо геометрию) и кисть для заполнения или структурирования фигуры.</span><span class="sxs-lookup"><span data-stu-id="d7e64-148">Most Draw and Fill methods take a shape (either a primitive or a geometry) and a brush for filling or outlining the shape.</span></span>

<span data-ttu-id="d7e64-149">Целевые объекты отрисовки предоставляют методы для обрезки, применения масок непрозрачности и преобразования пространства координат.</span><span class="sxs-lookup"><span data-stu-id="d7e64-149">Render targets provide methods for clipping, applying opacity masks, and transforming the coordinate space.</span></span>

<span data-ttu-id="d7e64-150">Direct2D использует левую систему координат: положительные значения оси x откладываются вправо, а положительные значения оси y — сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="d7e64-150">Direct2D uses a left-handed coordinate system: positive x-axis values proceed to the right and positive y-axis values proceed downward.</span></span>

### <a name="error-handling"></a><span data-ttu-id="d7e64-151">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="d7e64-151">Error Handling</span></span>

<span data-ttu-id="d7e64-152">Команды прорисовки целевого объекта не указывают, была ли запрошенная операция успешной.</span><span class="sxs-lookup"><span data-stu-id="d7e64-152">Render target drawing commands do not indicate whether the requested operation was successful.</span></span> <span data-ttu-id="d7e64-153">Чтобы определить, есть ли ошибки прорисовки, вызовите метод [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) целевого объекта Render или метод [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) для получения **значения HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d7e64-153">To find out whether there are drawing errors, call the render target [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method or [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method to obtain an **HRESULT**.</span></span>

## <a name="example-render-content-to-a-window"></a><span data-ttu-id="d7e64-154">Пример: отрисовка содержимого в окне</span><span class="sxs-lookup"><span data-stu-id="d7e64-154">Example: Render Content to a Window</span></span>

<span data-ttu-id="d7e64-155">В следующем примере используется метод [**креатехвндрендертаржет**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) для создания [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span><span class="sxs-lookup"><span data-stu-id="d7e64-155">The following example uses the [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) method to create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



<span data-ttu-id="d7e64-156">В следующем примере для рисования текста в окне используется [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="d7e64-156">The next example uses the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw text to the window.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="d7e64-157">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="d7e64-157">Code has been omitted from this example.</span></span>

 

 