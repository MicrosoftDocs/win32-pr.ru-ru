---
title: Общие сведения о взаимодействии Direct2D и GDI
description: Описывает, как использовать Direct2D и GDI совместно.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, взаимодействие GDI
- Direct2D, взаимодействие
- взаимодействие, Direct2D
- Интерфейс графических устройств (GDI)
- GDI (интерфейс графических устройств)
- взаимодействие, интерфейс графических устройств (GDI)
- Direct3D, взаимодействие
- Direct3D, Direct2D взаимодействие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793398"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a><span data-ttu-id="73a5b-111">Общие сведения о взаимодействии Direct2D и GDI</span><span class="sxs-lookup"><span data-stu-id="73a5b-111">Direct2D and GDI Interoperability Overview</span></span>

<span data-ttu-id="73a5b-112">В этом разделе описывается, как использовать Direct2D и [GDI](/windows/desktop/gdi/windows-gdi) совместно.</span><span class="sxs-lookup"><span data-stu-id="73a5b-112">This topic describes how to use Direct2D and [GDI](/windows/desktop/gdi/windows-gdi) together.</span></span> <span data-ttu-id="73a5b-113">Существует два способа объединения Direct2D с GDI: вы можете записывать содержимое GDI в Direct2D-совместимый целевой объект прорисовки, а также записывать содержимое Direct2D в [контекст устройства GDI (DC)](/windows/desktop/gdi/device-contexts).</span><span class="sxs-lookup"><span data-stu-id="73a5b-113">There are two ways to combine Direct2D with GDI: you can write GDI content to a Direct2D GDI-compatible render target, or you can write Direct2D content to a [GDI Device Context (DC)](/windows/desktop/gdi/device-contexts).</span></span>

<span data-ttu-id="73a5b-114">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="73a5b-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="73a5b-115">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="73a5b-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="73a5b-116">Нарисуйте содержимое Direct2D в контексте устройства GDI</span><span class="sxs-lookup"><span data-stu-id="73a5b-116">Draw Direct2D Content to a GDI Device Context</span></span>](#draw-direct2d-content-to-a-gdi-device-context)
-   [<span data-ttu-id="73a5b-117">ID2D1DCRenderTargets, преобразования GDI и языковые сборки Windows с письмом справа налево</span><span class="sxs-lookup"><span data-stu-id="73a5b-117">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [<span data-ttu-id="73a5b-118">Прорисовка содержимого GDI в Direct2D GDI-Compatible рендеринга</span><span class="sxs-lookup"><span data-stu-id="73a5b-118">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [<span data-ttu-id="73a5b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="73a5b-119">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="73a5b-120">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="73a5b-120">Prerequisites</span></span>

<span data-ttu-id="73a5b-121">В этом обзоре предполагается, что вы знакомы с базовыми операциями рисования Direct2D.</span><span class="sxs-lookup"><span data-stu-id="73a5b-121">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="73a5b-122">Инструкции см. в [кратком](direct2d-quickstart.md)руководстве по Direct2D.</span><span class="sxs-lookup"><span data-stu-id="73a5b-122">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="73a5b-123">Также предполагается, что вы знакомы с операциями рисования GDI.</span><span class="sxs-lookup"><span data-stu-id="73a5b-123">It also assumes that you are familiar with GDI drawing operations.</span></span>

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a><span data-ttu-id="73a5b-124">Нарисуйте содержимое Direct2D в контексте устройства GDI</span><span class="sxs-lookup"><span data-stu-id="73a5b-124">Draw Direct2D Content to a GDI Device Context</span></span>

<span data-ttu-id="73a5b-125">Для рисования содержимого Direct2D в GDI DC используется [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="73a5b-125">To draw Direct2D content to a GDI DC, you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span> <span data-ttu-id="73a5b-126">Чтобы создать целевой объект прорисовки контроллера домена, используйте метод [**ID2D1Factory:: креатедкрендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="73a5b-126">To create a DC render target, you use the [**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) method.</span></span> <span data-ttu-id="73a5b-127">Этот метод принимает два параметра.</span><span class="sxs-lookup"><span data-stu-id="73a5b-127">This method takes two parameters.</span></span>

<span data-ttu-id="73a5b-128">Первый параметр, структура [**\_ \_ \_ свойств целевого объекта отрисовки D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , определяет отрисовку, удаленное взаимодействие, dpi, формат пикселей и сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="73a5b-128">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure, specifies rendering, remoting, DPI, pixel format, and usage information.</span></span> <span data-ttu-id="73a5b-129">Чтобы целевой объект прорисовки контроллера домена работал с GDI, установите формат DXGI в режиме [DXGI \_ \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , а режим Alpha — в режим D2D1 альфа, предварительно [**\_ \_ \_ умноженный**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) или **D2D1 альфа- \_ \_ режим \_ игнорируется**.</span><span class="sxs-lookup"><span data-stu-id="73a5b-129">To enable the DC render target to work with GDI, set the DXGI format to [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) and the alpha mode to [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="73a5b-130">Вторым параметром является адрес указателя, получающего ссылку на целевой объект прорисовки контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="73a5b-130">The second parameter is the address of the pointer that receive the DC render target reference.</span></span>

<span data-ttu-id="73a5b-131">Следующий код создает целевой объект прорисовки контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="73a5b-131">The following code creates a DC render target.</span></span>


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



<span data-ttu-id="73a5b-132">В приведенном выше коде *m \_ pD2DFactory* является указателем на [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), а *m \_ пдкрт* — указателем на [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="73a5b-132">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pDCRT* is a pointer to an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span>

<span data-ttu-id="73a5b-133">Прежде чем можно будет подготовиться к просмотру с помощью целевого объекта прорисовки контроллера домена, необходимо использовать метод [**бинддк**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) , чтобы связать его с контроллером GDI.</span><span class="sxs-lookup"><span data-stu-id="73a5b-133">Before you can render with the DC render target, you must use its [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method to associate it with a GDI DC.</span></span> <span data-ttu-id="73a5b-134">Это делается каждый раз, когда используется другой контроллер домена, или размер области, которую требуется нарисовать для изменения.</span><span class="sxs-lookup"><span data-stu-id="73a5b-134">You do this each time you use a different DC, or the size of the area you want to draw to changes.</span></span>

<span data-ttu-id="73a5b-135">Метод [**бинддк**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) принимает два параметра: *HDC* и *псубрект*.</span><span class="sxs-lookup"><span data-stu-id="73a5b-135">The [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method takes two parameters, *hDC* and *pSubRect*.</span></span> <span data-ttu-id="73a5b-136">Параметр *HDC* предоставляет маркер для контекста устройства, который получает выходные данные целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="73a5b-136">The *hDC* parameter provides a handle to the device context that receives the output of the render target.</span></span> <span data-ttu-id="73a5b-137">Параметр *псубрект* — это прямоугольник, описывающий часть контекста устройства, в которой отображается содержимое.</span><span class="sxs-lookup"><span data-stu-id="73a5b-137">The *pSubRect* parameter is a rectangle that describes the portion of the device context to which content is rendered.</span></span> <span data-ttu-id="73a5b-138">Целевой объект прорисовки контроллера домена обновляет свой размер в соответствии с областью контекста устройства, описанной в *псубрект*, при изменении размера.</span><span class="sxs-lookup"><span data-stu-id="73a5b-138">The DC render target updates its size to match the device context area described by *pSubRect*, should it change size.</span></span>

<span data-ttu-id="73a5b-139">Следующий код привязывает контроллер домена к целевому объекту прорисовки контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="73a5b-139">The following code binds a DC to a DC render target.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73a5b-140">C++</span><span class="sxs-lookup"><span data-stu-id="73a5b-140">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="73a5b-141">После того как вы свяжете целевой объект прорисовки контроллера домена с контроллером домена, его можно будет использовать для рисования.</span><span class="sxs-lookup"><span data-stu-id="73a5b-141">After you associate the DC render target with a DC, you can use it to draw.</span></span> <span data-ttu-id="73a5b-142">Следующий код демонстрирует создание содержимого Direct2D и GDI с помощью контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="73a5b-142">The following code draws Direct2D and GDI content using a DC.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="73a5b-143">Этот код создает выходные данные, как показано на следующем рисунке (добавлены выноски для выделения разницы между Direct2D и визуализацией GDI).</span><span class="sxs-lookup"><span data-stu-id="73a5b-143">This code produces outputs as shown in the following illustration (callouts have been added to highlight the difference between Direct2D and GDI rendering.)</span></span>

![Иллюстрация двух круговых диаграмм, отображаемых с помощью Direct2D и GDI](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a><span data-ttu-id="73a5b-145">ID2D1DCRenderTargets, преобразования GDI и языковые сборки Windows с письмом справа налево</span><span class="sxs-lookup"><span data-stu-id="73a5b-145">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>

<span data-ttu-id="73a5b-146">При использовании [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)он визуализирует содержимое Direct2D во внутреннее растровое изображение, а затем визуализирует его на контроллере домена с помощью GDI.</span><span class="sxs-lookup"><span data-stu-id="73a5b-146">When you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), it renders Direct2D content to an internal bitmap, and then renders the bitmap to the DC with GDI.</span></span>

<span data-ttu-id="73a5b-147">GDI может применить преобразование GDI (через метод [**сетворлдтрансформ**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) ) или другой результат к тому же контроллеру домена, который используется целевым объектом рендеринга. в этом случае GDI преобразует точечный рисунок, созданный Direct2D.</span><span class="sxs-lookup"><span data-stu-id="73a5b-147">It's possible for GDI to apply a GDI transform (through the [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) method) or other effect to the same DC used by the render target, in which case GDI transforms the bitmap produced by Direct2D.</span></span> <span data-ttu-id="73a5b-148">Использование преобразования GDI для преобразования содержимого Direct2D может привести к ухудшению визуального качества выходных данных, так как вы преобразуете точечный рисунок, для которого уже рассчитано сглаживание и позиционирование подпикселей.</span><span class="sxs-lookup"><span data-stu-id="73a5b-148">Using a GDI transform to transform the Direct2D content has the potential to degrade the visual quality of the output, because you're transforming a bitmap for which antialiasing and subpixel positioning have already been calculated.</span></span>

<span data-ttu-id="73a5b-149">Например, предположим, что используется целевой объект отрисовки для рисования сцены, содержащей сглаженные геометрические фигуры и текст.</span><span class="sxs-lookup"><span data-stu-id="73a5b-149">For example, suppose you use the render target to draw a scene that contains antialiased geometries and text.</span></span> <span data-ttu-id="73a5b-150">Если вы используете преобразование GDI, чтобы применить преобразование масштабирования к контроллеру домена и масштабировать сцену таким образом, чтобы его размер в 10 раз больше, вы увидите пиксельные и зубчатые края.</span><span class="sxs-lookup"><span data-stu-id="73a5b-150">If you use a GDI transform to apply a scale transform to the DC and scale the scene so that it's 10 times larger, you'll see pixelization and jagged edges.</span></span> <span data-ttu-id="73a5b-151">(Если же вы применили аналогичное преобразование с помощью Direct2D, визуальное качество сцены не будет снижено.)</span><span class="sxs-lookup"><span data-stu-id="73a5b-151">(If, however, you applied a similar transform using Direct2D, the visual quality of the scene would not be degraded.)</span></span>

<span data-ttu-id="73a5b-152">В некоторых случаях может не быть очевидно, что GDI выполняет дополнительную обработку, что может ухудшить качество содержимого Direct2D.</span><span class="sxs-lookup"><span data-stu-id="73a5b-152">In some cases, it might not be obvious that GDI is performing additional processing that might degrade the quality of the Direct2D content.</span></span> <span data-ttu-id="73a5b-153">Например, при сборке Windows с НАПРАВЛЕНИЕм справа налево содержимое, отображаемое [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) , может быть горизонтально инвертировано, когда GDI копирует его в место назначения.</span><span class="sxs-lookup"><span data-stu-id="73a5b-153">For example, on a right-to-left (RTL) build of Windows, content rendered by an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) might be horizontally inverted when GDI copies it to its destination.</span></span> <span data-ttu-id="73a5b-154">Фактическое переинвертирование содержимого зависит от текущих параметров контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="73a5b-154">Whether the content is actually inverted depends on the current settings of the DC.</span></span>

<span data-ttu-id="73a5b-155">В зависимости от типа отображаемого содержимого может потребоваться запретить инверсию.</span><span class="sxs-lookup"><span data-stu-id="73a5b-155">Depending on the type of content being rendered, you might want to prevent the inversion.</span></span> <span data-ttu-id="73a5b-156">Если содержимое Direct2D содержит текст ClearType, эта инверсия приведет к ухудшению качества текста.</span><span class="sxs-lookup"><span data-stu-id="73a5b-156">If the Direct2D content includes ClearType text, this inversion will degrade the quality of the text.</span></span>

<span data-ttu-id="73a5b-157">Поведением отрисовки справа налево можно управлять с помощью функции GDI [**сетлайаут**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) .</span><span class="sxs-lookup"><span data-stu-id="73a5b-157">You can control RTL rendering behavior by using the [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI function.</span></span> <span data-ttu-id="73a5b-158">Чтобы предотвратить зеркальное отображение, вызовите функцию GDI **сетлайаут** и укажите **Макет \_ битмапориентатионпресервед** в качестве единственного значения для второго параметра (не объединяйте его с **макетом \_ RTL**), как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="73a5b-158">To prevent the mirroring, call the **SetLayout** GDI function and specify **LAYOUT\_BITMAPORIENTATIONPRESERVED** as the only value for the second parameter (do not combine it with **LAYOUT\_RTL**), as shown in the following example:</span></span>


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a><span data-ttu-id="73a5b-159">Прорисовка содержимого GDI в Direct2D GDI-Compatible рендеринга</span><span class="sxs-lookup"><span data-stu-id="73a5b-159">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>

<span data-ttu-id="73a5b-160">В предыдущем разделе описано, как записать содержимое Direct2D в GDI DC.</span><span class="sxs-lookup"><span data-stu-id="73a5b-160">The previous section describes how to write Direct2D content to a GDI DC.</span></span> <span data-ttu-id="73a5b-161">Вы также можете записать содержимое GDI в Direct2D-совместимый целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="73a5b-161">You can also write GDI content to a Direct2D GDI-compatible render target.</span></span> <span data-ttu-id="73a5b-162">Этот подход полезен для приложений, которые в основном отображаются с помощью Direct2D, но имеют модель расширяемости или другое устаревшее содержимое, которое требует возможности отрисовки с помощью GDI.</span><span class="sxs-lookup"><span data-stu-id="73a5b-162">This approach is useful for applications that primarily render with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span>

<span data-ttu-id="73a5b-163">Для отрисовки содержимого GDI в Direct2D, совместимом с GDI, используйте [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), который предоставляет доступ к контексту устройства, который может принимать вызовы GDI.</span><span class="sxs-lookup"><span data-stu-id="73a5b-163">To render GDI content to a Direct2D GDI-compatible render target, use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which provides access to a device context that can accept GDI draw calls.</span></span> <span data-ttu-id="73a5b-164">В отличие от других интерфейсов, объект **ID2D1GdiInteropRenderTarget** не создается напрямую.</span><span class="sxs-lookup"><span data-stu-id="73a5b-164">Unlike other interfaces, an **ID2D1GdiInteropRenderTarget** object is not created directly.</span></span> <span data-ttu-id="73a5b-165">Вместо этого используйте метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) существующего целевого экземпляра прорисовки.</span><span class="sxs-lookup"><span data-stu-id="73a5b-165">Instead, use the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of an existing render target instance.</span></span> <span data-ttu-id="73a5b-166">В следующем коде показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="73a5b-166">The following code shows how to do this:</span></span>


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



<span data-ttu-id="73a5b-167">В приведенном выше коде *m \_ pD2DFactory* является указателем на [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), а *m \_ пгдирт* — указателем на [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span><span class="sxs-lookup"><span data-stu-id="73a5b-167">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pGDIRT* is a pointer to an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span></span>

<span data-ttu-id="73a5b-168">Обратите внимание, что при создании целевого объекта прорисовки, совместимого с GDI, задается флаг [**\_ \_ \_ \_ \_ совместимости с использованием целевого объекта визуализации D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) .</span><span class="sxs-lookup"><span data-stu-id="73a5b-168">Notice that the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag is specified when creating the Hwnd GDI-compatible render target.</span></span> <span data-ttu-id="73a5b-169">Если требуется формат пикселей, используйте [ \_ Формат DXGI \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="73a5b-169">If a pixel format is required, use [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="73a5b-170">Если требуется альфа-режим, используйте режим [**альфа D2D1 Alpha с предварительным \_ \_ \_ умножением**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) или **\_ \_ режим \_ альфа D2D1**.</span><span class="sxs-lookup"><span data-stu-id="73a5b-170">If an alpha mode is required, use [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="73a5b-171">Обратите внимание, что метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) всегда проходит успешный результат.</span><span class="sxs-lookup"><span data-stu-id="73a5b-171">Note that the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method always succeeds.</span></span> <span data-ttu-id="73a5b-172">Чтобы проверить, работают ли методы интерфейса [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) для данного целевого объекта рендеринга, создайте [**D2D1 \_ \_ целевые \_ Свойства прорисовки**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , определяющие совместимость GDI и соответствующий формат пикселей, а затем вызовите метод « [**неподдерживаемый**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) » целевого объекта отрисовки, чтобы определить, совместима ли цель отрисовки с GDI.</span><span class="sxs-lookup"><span data-stu-id="73a5b-172">To test whether the [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) interface's methods will work for a given render target, create a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) that specifies GDI compatibility and the appropriate pixel format, and then call the render target's [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) method to see whether the render target is GDI-compatible.</span></span>

<span data-ttu-id="73a5b-173">В следующем примере показано, как нарисовать круговую диаграмму (содержимое GDI) для целевого объекта прорисовки, совместимого с GDI.</span><span class="sxs-lookup"><span data-stu-id="73a5b-173">The following example shows how to draw a pie chart (GDI content) to the Hwnd GDI-compatible render target.</span></span>


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



<span data-ttu-id="73a5b-174">Код выводит диаграммы, как показано на следующем рисунке с выносками для выделения качества отрисовки.</span><span class="sxs-lookup"><span data-stu-id="73a5b-174">The code outputs charts as shown in the following illustration with callouts to highlight the rendering quality difference.</span></span> <span data-ttu-id="73a5b-175">Правая круговая диаграмма (содержимое GDI) имеет более низкое качество отрисовки, чем у левой круговой диаграммы (Direct2D содержимое).</span><span class="sxs-lookup"><span data-stu-id="73a5b-175">The right pie chart (GDI content) has lower rendering quality than the left pie chart (Direct2D content).</span></span> <span data-ttu-id="73a5b-176">Это обусловлено тем, что Direct2D может выполнять отрисовку с помощью сглаживания</span><span class="sxs-lookup"><span data-stu-id="73a5b-176">This is because Direct2D is capable of rendering with antialiasing</span></span>

![Иллюстрация двух кольцевых диаграмм, отображаемых в Direct2D-совместимом целевом объекте отрисовки](images/gdicontentind2d.png)

## <a name="related-topics"></a><span data-ttu-id="73a5b-178">См. также</span><span class="sxs-lookup"><span data-stu-id="73a5b-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73a5b-179">**ID2D1Factory:: Креатедкрендертаржет**</span><span class="sxs-lookup"><span data-stu-id="73a5b-179">**ID2D1Factory::CreateDCRenderTarget**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[<span data-ttu-id="73a5b-180">**ID2D1DCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="73a5b-180">**ID2D1DCRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[<span data-ttu-id="73a5b-181">**ID2D1GdiInteropRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="73a5b-181">**ID2D1GdiInteropRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[<span data-ttu-id="73a5b-182">**\_ \_ Свойства целевого объекта ПРОРИСОВКи D2D1 \_**</span><span class="sxs-lookup"><span data-stu-id="73a5b-182">**D2D1\_RENDER\_TARGET\_PROPERTIES**</span></span>](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[<span data-ttu-id="73a5b-183">Контексты устройств GDI</span><span class="sxs-lookup"><span data-stu-id="73a5b-183">GDI Device Contexts</span></span>](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[<span data-ttu-id="73a5b-184">ПАКЕТ SDK ДЛЯ GDI</span><span class="sxs-lookup"><span data-stu-id="73a5b-184">GDI SDK</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 