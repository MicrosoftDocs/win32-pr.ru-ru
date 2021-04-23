---
title: Общие сведения о взаимодействии
description: Содержит сводку по различным технологиям, которые можно использовать с Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, взаимодействие GDI
- Direct2D, взаимодействие GDI+
- Direct2D, взаимодействие
- Direct2D, DirectWrite, взаимодействие
- взаимодействие, Direct2D
- взаимодействие, Direct3D
- Интерфейс графических устройств (GDI)
- GDI (интерфейс графических устройств)
- взаимодействие, интерфейс графических устройств (GDI)
- взаимодействие, GDI+
- Взаимодействие DirectWrite
- взаимодействие, DirectWrite
- Компонент обработки изображений Windows (WIC)
- WIC (компонент Windows Imaging)
- взаимодействие, компонент Windows Imaging Component (WIC)
- Direct2D, взаимодействие с WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413135"
---
# <a name="interoperability-overview"></a><span data-ttu-id="5366b-119">Общие сведения о взаимодействии</span><span class="sxs-lookup"><span data-stu-id="5366b-119">Interoperability Overview</span></span>

<span data-ttu-id="5366b-120">Одна из Direct2D's ключевых функций заключается в обеспечении взаимодействия между Direct2D и другими платформами отрисовки, чтобы разработчики могли использовать определенные сильные стороны каждой платформы, не беспокоясь о компрометации, выбрав одну платформу для всех нужд.</span><span class="sxs-lookup"><span data-stu-id="5366b-120">One of Direct2D's key features is enabling interoperability between Direct2D and other rendering platforms so that developers can use the specific strengths of each platform without being forced into compromises by choosing one platform for all needs.</span></span> <span data-ttu-id="5366b-121">В этом разделе перечислены различные платформы, с которыми взаимодействуют Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5366b-121">This topic summarizes the different platforms with which Direct2D is interoperable.</span></span> <span data-ttu-id="5366b-122">В него входят следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="5366b-122">It contains the following sections.</span></span>

-   [<span data-ttu-id="5366b-123">Взаимодействие GDI</span><span class="sxs-lookup"><span data-stu-id="5366b-123">GDI Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="5366b-124">Взаимодействие GDI+</span><span class="sxs-lookup"><span data-stu-id="5366b-124">GDI+ Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="5366b-125">Совместимость с Direct3D</span><span class="sxs-lookup"><span data-stu-id="5366b-125">Direct3D Interoperability</span></span>](#direct3d-interoperability)
-   [<span data-ttu-id="5366b-126">Взаимодействие DirectWrite</span><span class="sxs-lookup"><span data-stu-id="5366b-126">DirectWrite Interoperability</span></span>](#directwrite-interoperability)
-   [<span data-ttu-id="5366b-127">Взаимодействие компонента работы с образами Windows (WIC)</span><span class="sxs-lookup"><span data-stu-id="5366b-127">Windows Imaging Component (WIC) Interoperability</span></span>](#windows-imaging-component-wic-interoperability)
-   [<span data-ttu-id="5366b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5366b-128">Related topics</span></span>](#related-topics)

<span data-ttu-id="5366b-129">На следующей диаграмме показаны различные платформы, с которыми Direct2D взаимозаменяемыми, и перечислены некоторые методы и интерфейсы, обеспечивающие взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="5366b-129">The following diagram summarizes the different platforms with which Direct2D is interoperable and lists some methods and interfaces that provide interoperability.</span></span>

![Схема платформ, Direct2D взаимодействующих с, включая Direct3D 10,1, DirectWrite, WIC, GDI+ и GDI.](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a><span data-ttu-id="5366b-131">Взаимодействие GDI</span><span class="sxs-lookup"><span data-stu-id="5366b-131">GDI Interoperability</span></span>

<span data-ttu-id="5366b-132">Direct2D обеспечивает двухстороннее взаимодействие с GDI.</span><span class="sxs-lookup"><span data-stu-id="5366b-132">Direct2D enables two-way interoperability with GDI.</span></span> <span data-ttu-id="5366b-133">Вы можете использовать [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) для записи содержимого Direct2D в [контекст устройства](/windows/desktop/gdi/device-contexts) GDI (DC) или использовать [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) для получения представления контроллера домена для целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="5366b-133">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to a GDI [device context](/windows/desktop/gdi/device-contexts) (DC), or you can use [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to obtain a DC representation of a render target.</span></span>

<span data-ttu-id="5366b-134">Дополнительные сведения и примеры см. в статье [Общие сведения о взаимодействии Direct2D и GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5366b-134">For more information and examples, see the [Direct2D and GDI Interoperability Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="5366b-135">Взаимодействие GDI+</span><span class="sxs-lookup"><span data-stu-id="5366b-135">GDI+ Interoperability</span></span>

<span data-ttu-id="5366b-136">GDI+ с Direct2D можно использовать так же, как и GDI.</span><span class="sxs-lookup"><span data-stu-id="5366b-136">You can use GDI+ with Direct2D in the same manner as GDI.</span></span> <span data-ttu-id="5366b-137">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) можно использовать для записи содержимого Direct2D на тот же контроллер домена, что и содержимое GDI+.</span><span class="sxs-lookup"><span data-stu-id="5366b-137">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to the same DC as your GDI+ content.</span></span> <span data-ttu-id="5366b-138">Такой подход позволяет приступить к добавлению содержимого Direct2D в приложения, которые в основном отображаются с помощью GDI+.</span><span class="sxs-lookup"><span data-stu-id="5366b-138">This approach enables you to start adding Direct2D content to applications that primarily render by using GDI+.</span></span>

<span data-ttu-id="5366b-139">Можно также использовать [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) для предоставления доступа к контроллеру домена GDI, записывающему с помощью Direct2D, а затем использовать метод [**фромхдк**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="5366b-139">You can also use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to provide access to a GDI DC that writes by using Direct2D, and then use the [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) method to create a object.</span></span> <span data-ttu-id="5366b-140">Этот подход удобен для приложений, которые в основном отображаются с помощью Direct2D, но имеют модель расширяемости или другое устаревшее содержимое, которое требует возможности визуализации с помощью GDI+.</span><span class="sxs-lookup"><span data-stu-id="5366b-140">This approach is useful for applications that primarily render with Direct2D, but have an extensibility model or other legacy content that requires the ability to render with GDI+.</span></span>

## <a name="direct3d-interoperability"></a><span data-ttu-id="5366b-141">Совместимость с Direct3D</span><span class="sxs-lookup"><span data-stu-id="5366b-141">Direct3D Interoperability</span></span>

<span data-ttu-id="5366b-142">Direct2D может использовать целевой объект отрисовки поверхности DXGI (созданный методом [**креатедксгисурфацерендер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) для записи в [идксгисурфаце](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span><span class="sxs-lookup"><span data-stu-id="5366b-142">Direct2D can use a DXGI surface render target (created by the [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method) to write to an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span></span> <span data-ttu-id="5366b-143">Это действие позволяет добавлять двумерные фоны и интерфейсы в трехмерные сцены и использовать содержимое Direct2D в качестве текстуры для трехмерной модели.</span><span class="sxs-lookup"><span data-stu-id="5366b-143">This action enables you to add 2-D backgrounds and interfaces to 3-D scenes and use Direct2D content as a texture for a 3-D model.</span></span> <span data-ttu-id="5366b-144">Direct2D также может взять [идксгисурфаце](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) и использовать метод [**креатешаредбитмап**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) для создания растрового представления.</span><span class="sxs-lookup"><span data-stu-id="5366b-144">Direct2D can also take an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) and use the [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method to create a bitmap representation.</span></span>

<span data-ttu-id="5366b-145">Дополнительные сведения и примеры см. в статье [Общие сведения о взаимодействии Direct2D и Direct3D](direct2d-and-direct3d-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5366b-145">For more information and examples, see the [Direct2D and Direct3D Interoperability Overview](direct2d-and-direct3d-interoperation-overview.md).</span></span>

## <a name="directwrite-interoperability"></a><span data-ttu-id="5366b-146">Взаимодействие DirectWrite</span><span class="sxs-lookup"><span data-stu-id="5366b-146">DirectWrite Interoperability</span></span>

<span data-ttu-id="5366b-147">Direct2D тесно интегрирован с DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="5366b-147">Direct2D is tightly integrated with DirectWrite.</span></span> <span data-ttu-id="5366b-148">Direct2D упрощает визуализацию содержимого DirectWrite, предоставляя методы [**DrawText**](id2d1rendertarget-drawtext.md), [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)и [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="5366b-148">Direct2D makes it easy to render DirectWrite content by providing the [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), and [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) methods.</span></span>

## <a name="windows-imaging-component-wic-interoperability"></a><span data-ttu-id="5366b-149">Взаимодействие компонента работы с образами Windows (WIC)</span><span class="sxs-lookup"><span data-stu-id="5366b-149">Windows Imaging Component (WIC) Interoperability</span></span>

<span data-ttu-id="5366b-150">Direct2D предоставляет методы [**креатебитмапфромвикбитмап**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**креатешаредбитмап**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)и [**креатевикбитмапрендертаржет**](id2d1factory-createwicbitmaprendertarget.md) для управления точечными рисунками WIC.</span><span class="sxs-lookup"><span data-stu-id="5366b-150">Direct2D provides the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap), and [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) methods for manipulating WIC bitmaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5366b-151">См. также</span><span class="sxs-lookup"><span data-stu-id="5366b-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5366b-152">Общие сведения о взаимодействии Direct2D и GDI</span><span class="sxs-lookup"><span data-stu-id="5366b-152">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[<span data-ttu-id="5366b-153">Общие сведения о взаимодействии Direct2D и Direct3D</span><span class="sxs-lookup"><span data-stu-id="5366b-153">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 