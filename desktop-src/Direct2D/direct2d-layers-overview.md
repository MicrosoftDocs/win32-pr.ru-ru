---
title: Общие сведения о слоях
description: Основные сведения о Direct2D слоях.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, слои
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ac68ba25d1e8f35c5a41daec4d7a5295235a5d98
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549189"
---
# <a name="layers-overview"></a><span data-ttu-id="07cd3-104">Общие сведения о слоях</span><span class="sxs-lookup"><span data-stu-id="07cd3-104">Layers Overview</span></span>

<span data-ttu-id="07cd3-105">В этом обзоре описываются основы использования Direct2D слоев.</span><span class="sxs-lookup"><span data-stu-id="07cd3-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="07cd3-106">В него входят следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="07cd3-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="07cd3-107">Что такое слои?</span><span class="sxs-lookup"><span data-stu-id="07cd3-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="07cd3-108">Слои в Windows 8 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="07cd3-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="07cd3-109">ID2D1DeviceContext и Пушлайер</span><span class="sxs-lookup"><span data-stu-id="07cd3-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="07cd3-110">D2D1 \_ Layer \_ PARAMETERS1 и D2D1 \_ Layer \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="07cd3-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="07cd3-111">Режимы смешения</span><span class="sxs-lookup"><span data-stu-id="07cd3-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="07cd3-112">Взаимодействия</span><span class="sxs-lookup"><span data-stu-id="07cd3-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="07cd3-113">Создание слоев</span><span class="sxs-lookup"><span data-stu-id="07cd3-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="07cd3-114">Границы содержимого</span><span class="sxs-lookup"><span data-stu-id="07cd3-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="07cd3-115">Геометрические маски</span><span class="sxs-lookup"><span data-stu-id="07cd3-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="07cd3-116">Маски непрозрачности</span><span class="sxs-lookup"><span data-stu-id="07cd3-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="07cd3-117">Альтернативы слоям</span><span class="sxs-lookup"><span data-stu-id="07cd3-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="07cd3-118">Обрезка произвольной фигуры</span><span class="sxs-lookup"><span data-stu-id="07cd3-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="07cd3-119">Выровняйте картинки по оси</span><span class="sxs-lookup"><span data-stu-id="07cd3-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="07cd3-120">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="07cd3-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="07cd3-121">Что такое слои?</span><span class="sxs-lookup"><span data-stu-id="07cd3-121">What Are Layers?</span></span>

<span data-ttu-id="07cd3-122">Уровни, представленные объектами [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , позволяют приложению управлять группой операций рисования.</span><span class="sxs-lookup"><span data-stu-id="07cd3-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="07cd3-123">Слой можно использовать, отправляя его в целевой объект прорисовки.</span><span class="sxs-lookup"><span data-stu-id="07cd3-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="07cd3-124">Последующие операции рисования, выполняемые целевым объектом отрисовки, направляются на слой.</span><span class="sxs-lookup"><span data-stu-id="07cd3-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="07cd3-125">Завершив работу с слоем, можно «присвоить» слой из целевого объекта прорисовки, который комбинирует содержимое слоя обратно в целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="07cd3-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="07cd3-126">Как и кисти, слои — это ресурсы, зависящие от устройства, созданные объектами прорисовки.</span><span class="sxs-lookup"><span data-stu-id="07cd3-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="07cd3-127">Слои можно использовать для любого целевого объекта отрисовки в том же домене ресурсов, который содержит целевой объект рендеринга, который ее создал.</span><span class="sxs-lookup"><span data-stu-id="07cd3-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="07cd3-128">Однако ресурс уровня может использоваться только одним целевым объектом отрисовки за раз.</span><span class="sxs-lookup"><span data-stu-id="07cd3-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="07cd3-129">Дополнительные сведения о ресурсах см. в разделе [Общие сведения о ресурсах](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="07cd3-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="07cd3-130">Хотя уровни предлагают мощный метод отрисовки для создания интересных эффектов, чрезмерное число слоев в приложении может негативно сказаться на его производительности, так как при управлении слоями и ресурсами слоя могут воздействовать различные затраты.</span><span class="sxs-lookup"><span data-stu-id="07cd3-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="07cd3-131">Например, есть затраты на заполнение или очистку слоя и его обратное смешение, особенно на более высоком оборудовании.</span><span class="sxs-lookup"><span data-stu-id="07cd3-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="07cd3-132">Затем есть затраты на управление ресурсами уровня.</span><span class="sxs-lookup"><span data-stu-id="07cd3-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="07cd3-133">Если вы перераспределяете их часто, то конечные остановки GPU будут самыми значительными проблемами.</span><span class="sxs-lookup"><span data-stu-id="07cd3-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="07cd3-134">При проектировании приложения попытайтесь максимально увеличить повторное использование ресурсов слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="07cd3-135">Слои в Windows 8 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="07cd3-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="07cd3-136">В Windows 8 появились новые API-интерфейсы, которые упрощают работу, улучшают производительность и добавляют компоненты к слоям.</span><span class="sxs-lookup"><span data-stu-id="07cd3-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="07cd3-137">ID2D1DeviceContext и Пушлайер</span><span class="sxs-lookup"><span data-stu-id="07cd3-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="07cd3-138">Интерфейс [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) является производным от интерфейса [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) и является ключом к отображению содержимого Direct2D в Windows 8. Дополнительные сведения об этом интерфейсе см. в разделе [устройства и контексты устройств](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="07cd3-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="07cd3-139">С помощью интерфейса контекста устройства можно пропустить вызов метода [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , а затем передать NULL методу [**ID2D1DeviceContext::P ушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="07cd3-140">Direct2D автоматически управляет ресурсом слоя и может совместно использовать ресурсы между слоями и графами эффектов.</span><span class="sxs-lookup"><span data-stu-id="07cd3-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="07cd3-141">D2D1 \_ Layer \_ PARAMETERS1 и D2D1 \_ Layer \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="07cd3-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="07cd3-142">Структура [**D2D1 \_ Layer \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) аналогична [**\_ \_ параметрам слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), за исключением того, что последний член структуры теперь является перечислением [**D2D1 \_ \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="07cd3-143">[**D2D1 \_ СЛОЙ \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) не имеет параметра ClearType и имеет два различных параметра, которые можно использовать для повышения производительности:</span><span class="sxs-lookup"><span data-stu-id="07cd3-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="07cd3-144">[**D2D1 \_ СЛОЙ \_ OPTIONS1 \_ инициализируется \_ из \_ фона**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D отображает примитивы на слой, не снимая его с прозрачным черным цветом.</span><span class="sxs-lookup"><span data-stu-id="07cd3-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="07cd3-145">Это не значение по умолчанию, но в большинстве случаев это приводит к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="07cd3-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="07cd3-146">[**D2D1 \_ СЛОЙ \_ OPTIONS1 \_ игнорировать \_ альфа**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)-канал: Если для базовой поверхности задан [**\_ режим D2D1 \_ Alpha \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), этот параметр позволяет Direct2D избежать изменения альфа-канала слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="07cd3-147">Не используйте его в других случаях.</span><span class="sxs-lookup"><span data-stu-id="07cd3-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="07cd3-148">Режимы смешения</span><span class="sxs-lookup"><span data-stu-id="07cd3-148">Blend Modes</span></span>

<span data-ttu-id="07cd3-149">Начиная с Windows 8, контекст устройства имеет [**простой режим смешения**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) , который определяет, как каждый примитив смешивается с целевой поверхностью.</span><span class="sxs-lookup"><span data-stu-id="07cd3-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="07cd3-150">Этот режим также применяется к слоям при вызове метода [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="07cd3-151">Например, если вы используете слой для обрезки примитивов с прозрачностью, для правильного результата задайте режим [**копирования D2D1- \_ примитивного \_ смешения \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="07cd3-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="07cd3-152">Режим копирования обеспечивает линейную интерполяцию контекста устройства: все 4 цветовые каналы, включая альфа-канал, каждого пикселя с содержимым целевой поверхности в соответствии с геометрической маской слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="07cd3-153">Взаимодействие</span><span class="sxs-lookup"><span data-stu-id="07cd3-153">Interoperation</span></span>

<span data-ttu-id="07cd3-154">Начиная с Windows 8, Direct2D поддерживает взаимодействие с Direct3D и GDI во время отправки слоя или клипа.</span><span class="sxs-lookup"><span data-stu-id="07cd3-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="07cd3-155">Метод [**ID2D1GdiInteropRenderTarget:: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) вызывается, пока слой передается для взаимодействия с GDI.</span><span class="sxs-lookup"><span data-stu-id="07cd3-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="07cd3-156">Вы вызываете [**ID2D1DeviceContext:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) , а затем готовитесь к просмотру на основной поверхности для взаимодействия с Direct3D.</span><span class="sxs-lookup"><span data-stu-id="07cd3-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="07cd3-157">Вы отвечаете за отображение внутри слоя или клипа с помощью Direct3D или GDI.</span><span class="sxs-lookup"><span data-stu-id="07cd3-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="07cd3-158">При попытке отображения за пределами слоя или клипа результаты не определены.</span><span class="sxs-lookup"><span data-stu-id="07cd3-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="07cd3-159">Создание слоев</span><span class="sxs-lookup"><span data-stu-id="07cd3-159">Creating Layers</span></span>

<span data-ttu-id="07cd3-160">Работа с слоями требует знакомства с методами [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , а также структурой [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , которая содержит набор данных параметрической, определяющих, как можно использовать слой.</span><span class="sxs-lookup"><span data-stu-id="07cd3-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="07cd3-161">В следующем списке описываются методы и структура.</span><span class="sxs-lookup"><span data-stu-id="07cd3-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="07cd3-162">Вызовите метод [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , чтобы создать ресурс слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="07cd3-163">Начиная с Windows 8, можно пропустить вызов метода [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , а затем передать NULL методу [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) в интерфейсе [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="07cd3-164">Это проще и позволяет Direct2D автоматически управлять ресурсом слоя и совместно использовать ресурсы между слоями и графами эффектов.</span><span class="sxs-lookup"><span data-stu-id="07cd3-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="07cd3-165">После того как целевой объект прорисовки начал Рисование (после вызова метода [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ), можно использовать метод [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="07cd3-166">Метод **пушлайер** добавляет указанный слой в целевой объект отрисовки, чтобы целевой объект получал все последующие операции рисования до вызова [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="07cd3-167">Этот метод принимает объект [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , возвращаемый путем вызова [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) и *Лайерпараметерс* в структуре [**\_ \_ параметров уровня D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="07cd3-168">В следующей таблице описаны поля структуры.</span><span class="sxs-lookup"><span data-stu-id="07cd3-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="07cd3-169">Поле</span><span class="sxs-lookup"><span data-stu-id="07cd3-169">Field</span></span>                 | <span data-ttu-id="07cd3-170">Описание</span><span class="sxs-lookup"><span data-stu-id="07cd3-170">Description</span></span>|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="07cd3-171">**контентбаундс**</span><span class="sxs-lookup"><span data-stu-id="07cd3-171">**contentBounds**</span></span>     | <span data-ttu-id="07cd3-172">Границы содержимого слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-172">The content bounds of the layer.</span></span> <span data-ttu-id="07cd3-173">Содержимое за пределами этих границ гарантированно не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="07cd3-173">Content outside these bounds is guaranteed not to render.</span></span> <span data-ttu-id="07cd3-174">По умолчанию этот параметр имеет значение [**инфинитерект**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span><span class="sxs-lookup"><span data-stu-id="07cd3-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="07cd3-175">Если используется значение по умолчанию, границы содержимого фактически передаются в качестве границ целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="07cd3-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |
    | <span data-ttu-id="07cd3-176">**жеометрикмаск**</span><span class="sxs-lookup"><span data-stu-id="07cd3-176">**geometricMask**</span></span>     | <span data-ttu-id="07cd3-177">Используемых Область, определяемая [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), в которую должен быть обрезан слой.</span><span class="sxs-lookup"><span data-stu-id="07cd3-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="07cd3-178">Задайте **значение NULL** , если слой не должен быть обрезан до геометрии.</span><span class="sxs-lookup"><span data-stu-id="07cd3-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span> |
    | <span data-ttu-id="07cd3-179">**маскантиалиасмоде**</span><span class="sxs-lookup"><span data-stu-id="07cd3-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="07cd3-180">Значение, указывающее режим сглаживания для геометрической маски, указанной в поле **жеометрикмаск** .</span><span class="sxs-lookup"><span data-stu-id="07cd3-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span> |
    | <span data-ttu-id="07cd3-181">**масктрансформ**</span><span class="sxs-lookup"><span data-stu-id="07cd3-181">**maskTransform**</span></span>     | <span data-ttu-id="07cd3-182">Значение, указывающее преобразование, применяемое к геометрической маске при создании слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="07cd3-183">Это относится к универсальному преобразованию.</span><span class="sxs-lookup"><span data-stu-id="07cd3-183">This is relative to the world transform.</span></span>  |
    | <span data-ttu-id="07cd3-184">**данной**</span><span class="sxs-lookup"><span data-stu-id="07cd3-184">**opacity**</span></span>           | <span data-ttu-id="07cd3-185">Значение прозрачности слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-185">The opacity value of the layer.</span></span> <span data-ttu-id="07cd3-186">Непрозрачность каждого ресурса слоя умножается на это значение при совмещении с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="07cd3-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>  |
    | <span data-ttu-id="07cd3-187">**опаЦитибруш**</span><span class="sxs-lookup"><span data-stu-id="07cd3-187">**opacityBrush**</span></span>      | <span data-ttu-id="07cd3-188">Используемых Кисть, используемая для изменения прозрачности слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="07cd3-189">Кисть сопоставляется с слоем, а альфа-канал каждого сопоставленного пикселя кисти умножается на соответствующий пиксель слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="07cd3-190">Задайте **значение NULL** , если слой не должен иметь маску непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="07cd3-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>   |
    | <span data-ttu-id="07cd3-191">**лайероптионс**</span><span class="sxs-lookup"><span data-stu-id="07cd3-191">**layerOptions**</span></span>      | <span data-ttu-id="07cd3-192">Значение, указывающее, будет ли слой вырисовывать текст с помощью сглаживания ClearType.</span><span class="sxs-lookup"><span data-stu-id="07cd3-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="07cd3-193">По умолчанию этот параметр имеет значение OFF.</span><span class="sxs-lookup"><span data-stu-id="07cd3-193">This parameter defaults to off.</span></span> <span data-ttu-id="07cd3-194">Если включить его, технология ClearType будет работать правильно, но это приводит к немного меньшей скорости рендеринга.</span><span class="sxs-lookup"><span data-stu-id="07cd3-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>    |

    

     

    > [!Note]  
    > <span data-ttu-id="07cd3-195">Начиная с Windows 8, нельзя визуализировать с помощью технологии ClearType в слое, поэтому параметр **лайероптионс** всегда должен иметь значение [**D2D1 \_ Layer \_ \_ None**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="07cd3-196">Для удобства Direct2D предоставляет метод [**D2D1:: лайерпараметерс**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) , помогающий создавать структуры [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="07cd3-197">Чтобы составить содержимое слоя в целевой объект рендеринга, вызовите метод [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="07cd3-198">Перед вызовом метода [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) необходимо вызвать метод **поплайер** .</span><span class="sxs-lookup"><span data-stu-id="07cd3-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="07cd3-199">В следующем примере показано, как использовать [**креателайер**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span><span class="sxs-lookup"><span data-stu-id="07cd3-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="07cd3-200">Для всех полей в [**структуре \_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) заданы значения по умолчанию, за исключением **опаЦитибруш**, для которого задано значение [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="07cd3-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



<span data-ttu-id="07cd3-201">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="07cd3-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="07cd3-202">Обратите внимание, что при вызове [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)убедитесь, что каждый **пушлайер** имеет соответствующий вызов **поплайер** .</span><span class="sxs-lookup"><span data-stu-id="07cd3-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="07cd3-203">Если количество вызовов **поплайер** превышает число вызовов **пушлайер** , то целевой объект прорисовки помещается в состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="07cd3-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="07cd3-204">Если функция [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) вызывается до того, как все необработанные слои будут извлечены, то целевой объект прорисовки помещается в состояние ошибки и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="07cd3-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="07cd3-205">Чтобы очистить состояние ошибки, используйте [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="07cd3-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="07cd3-206">Границы содержимого</span><span class="sxs-lookup"><span data-stu-id="07cd3-206">Content Bounds</span></span>

<span data-ttu-id="07cd3-207">**Контентбаундс** устанавливает предельный размер отображаемых данных слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="07cd3-208">Только те элементы, которые находятся в границах содержимого, являются составными для целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="07cd3-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="07cd3-209">В следующем примере показано, как задать **контентбаундс** , чтобы исходное изображение было обрезано с учетом содержимого в левом верхнем углу в точке (10, 108) и правом нижнем углу в (121, 177).</span><span class="sxs-lookup"><span data-stu-id="07cd3-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="07cd3-210">На следующем рисунке показано исходное изображение и результат обрезки изображения до границ содержимого.</span><span class="sxs-lookup"><span data-stu-id="07cd3-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![Иллюстрация границ содержимого на исходном изображении и полученное обрезанное изображение](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="07cd3-212">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="07cd3-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="07cd3-213">Полученное обрезанное изображение будет дополнительно затронуто при указании **жеометрикмаск**.</span><span class="sxs-lookup"><span data-stu-id="07cd3-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="07cd3-214">Дополнительные сведения см. в разделе [геометрические маски](#geometric-masks) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="07cd3-215">Геометрические маски</span><span class="sxs-lookup"><span data-stu-id="07cd3-215">Geometric Masks</span></span>

<span data-ttu-id="07cd3-216">Геометрическая маска — это клип или фрагмент, определяемый объектом [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , который маскирует слой при прорисовке объектом прорисовки.</span><span class="sxs-lookup"><span data-stu-id="07cd3-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="07cd3-217">Для маскирования результатов до геометрии можно использовать поле **жеометрикмаск** структуры [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="07cd3-218">Например, если нужно отобразить изображение, маскированное по блоку «A», можно сначала создать геометрию, представляющую блок-символ «A», и использовать эту геометрию в качестве геометрической маски для слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="07cd3-219">Затем, после того, как слой помещается, можно нарисовать изображение.</span><span class="sxs-lookup"><span data-stu-id="07cd3-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="07cd3-220">При извлечении слоя изображение обрезается по фигуре блока "A".</span><span class="sxs-lookup"><span data-stu-id="07cd3-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="07cd3-221">В следующем примере показано, как создать [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , содержащий форму Mountain, а затем передать геометрию пути в [**пушлайер**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="07cd3-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="07cd3-222">Затем он рисует растровое изображение и квадраты.</span><span class="sxs-lookup"><span data-stu-id="07cd3-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="07cd3-223">Если в слое для отрисовки имеется только точечный рисунок, для повышения эффективности используйте [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) с размытой растровой кистью.</span><span class="sxs-lookup"><span data-stu-id="07cd3-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="07cd3-224">На следующем рисунке показан результат выполнения этого примера.</span><span class="sxs-lookup"><span data-stu-id="07cd3-224">The following illustration shows the output from the example.</span></span>

![Иллюстрация изображения листа и полученного изображения после применения геометрической маски Mountain](images/layers-bitmapmask.png)

<span data-ttu-id="07cd3-226">В первом примере определяется геометрия, которая будет использоваться в качестве маски.</span><span class="sxs-lookup"><span data-stu-id="07cd3-226">The first example defines the geometry to be used as a mask.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



<span data-ttu-id="07cd3-227">В следующем примере геометрия используется в качестве маски для слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-227">The next example uses the geometry as a mask for the layer.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="07cd3-228">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="07cd3-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="07cd3-229">В общем случае при указании **жеометрикмаск** можно использовать значение по умолчанию [**инфинитерект**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)для **контентбаундс**.</span><span class="sxs-lookup"><span data-stu-id="07cd3-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="07cd3-230">Если **контентбаундс** имеет значение NULL и **жеометрикмаск** имеет значение, отличное от NULL, то границы содержимого фактически являются границами геометрической маски после применения преобразования маски.</span><span class="sxs-lookup"><span data-stu-id="07cd3-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="07cd3-231">Если **контентбаундс** имеет значение, отличное от NULL, а **жеометрикмаск** имеет значение, отличное от NULL, то преобразованная геометрическая маска фактически обрезается по границам содержимого, а границы содержимого считаются бесконечными.</span><span class="sxs-lookup"><span data-stu-id="07cd3-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="07cd3-232">Маски непрозрачности</span><span class="sxs-lookup"><span data-stu-id="07cd3-232">Opacity Masks</span></span>

<span data-ttu-id="07cd3-233">Маска непрозрачности — это маска, описываемая кистью или точечным рисунком, которая применяется к другому объекту, чтобы сделать этот объект частично или полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="07cd3-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="07cd3-234">Он позволяет использовать альфа-канал кисти для использования в качестве маски содержимого.</span><span class="sxs-lookup"><span data-stu-id="07cd3-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="07cd3-235">Например, можно определить кисть радиального градиента, которая отличается от непрозрачной и прозрачной для создания вигнеттеного действия.</span><span class="sxs-lookup"><span data-stu-id="07cd3-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="07cd3-236">В следующем примере используется [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ прадиалградиентбруш*) в качестве маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="07cd3-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="07cd3-237">Затем он рисует растровое изображение и квадраты.</span><span class="sxs-lookup"><span data-stu-id="07cd3-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="07cd3-238">Если в слое для отрисовки имеется только точечный рисунок, для повышения эффективности используйте [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) с размытой растровой кистью.</span><span class="sxs-lookup"><span data-stu-id="07cd3-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="07cd3-239">На следующем рисунке показаны выходные данные из этого примера.</span><span class="sxs-lookup"><span data-stu-id="07cd3-239">The following illustration shows the output from this example.</span></span>

![Иллюстрация изображения деревьев и полученного изображения после применения маски непрозрачности](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="07cd3-241">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="07cd3-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="07cd3-242">В этом примере используется слой для применения маски непрозрачности к одному объекту, чтобы максимально упростить пример.</span><span class="sxs-lookup"><span data-stu-id="07cd3-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="07cd3-243">При применении маски непрозрачности к одному объекту более эффективно использовать методы [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) или [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , а не слой.</span><span class="sxs-lookup"><span data-stu-id="07cd3-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="07cd3-244">Инструкции по применению маски непрозрачности без использования слоя см. в разделе [Общие сведения о масках непрозрачности](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="07cd3-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="07cd3-245">Альтернативы слоям</span><span class="sxs-lookup"><span data-stu-id="07cd3-245">Alternatives to Layers</span></span>

<span data-ttu-id="07cd3-246">Как упоминалось ранее, чрезмерное количество слоев может негативно сказаться на производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="07cd3-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="07cd3-247">Чтобы повысить производительность, старайтесь не использовать слои везде, где это возможно. Вместо этого используйте их альтернативы.</span><span class="sxs-lookup"><span data-stu-id="07cd3-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="07cd3-248">В следующем примере кода показано, как использовать [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) и [**попаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) для обрезки области в качестве альтернативы использованию слоя с границами содержимого.</span><span class="sxs-lookup"><span data-stu-id="07cd3-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="07cd3-249">Аналогично, используйте [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) с растровой кистью с маскированием в качестве альтернативы использованию слоя с маской непрозрачности, если в слое для отрисовки имеется только одно содержимое, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="07cd3-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="07cd3-250">В качестве альтернативы использованию слоя с геометрической маской можно использовать битовую маску для обрезки области, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="07cd3-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="07cd3-251">Наконец, если вы хотите применить непрозрачность к одному примитиву, необходимо умножить степень прозрачности на цвет кисти, а затем визуализировать примитив.</span><span class="sxs-lookup"><span data-stu-id="07cd3-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="07cd3-252">Не требуется слой или битовая карта маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="07cd3-252">You do not need a layer or an opacity mask bitmap.</span></span>


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="07cd3-253">Обрезка произвольной фигуры</span><span class="sxs-lookup"><span data-stu-id="07cd3-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="07cd3-254">На рисунке ниже показан результат применения клипа к изображению.</span><span class="sxs-lookup"><span data-stu-id="07cd3-254">The figure here shows the result of applying a clip to an image.</span></span>

![изображение, в котором показан пример изображения до и после клипа.](images/clip.png)

<span data-ttu-id="07cd3-256">Этот результат можно получить с помощью слоев с геометрической маской или методом [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) с кистью непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="07cd3-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="07cd3-257">Ниже приведен пример использования слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="07cd3-258">Ниже приведен пример использования метода [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :</span><span class="sxs-lookup"><span data-stu-id="07cd3-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



<span data-ttu-id="07cd3-259">В этом примере кода при вызове метода Пушлайер вы не передаетесь на слой, созданный приложением.</span><span class="sxs-lookup"><span data-stu-id="07cd3-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="07cd3-260">Direct2D создает слой для вас.</span><span class="sxs-lookup"><span data-stu-id="07cd3-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="07cd3-261">Direct2D может управлять выделением и уничтожением этого ресурса без участия в приложении.</span><span class="sxs-lookup"><span data-stu-id="07cd3-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="07cd3-262">Это позволяет Direct2D использовать слои внутренним образом и применять оптимизации управления ресурсами.</span><span class="sxs-lookup"><span data-stu-id="07cd3-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="07cd3-263">В Windows 8 многие оптимизации были применены к использованию уровней, и мы рекомендуем использовать API слоя вместо [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="07cd3-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="07cd3-264">Выровняйте картинки по оси</span><span class="sxs-lookup"><span data-stu-id="07cd3-264">Axis aligned clips</span></span>

<span data-ttu-id="07cd3-265">Если регион, который будет обрезан, вырезается по оси поверхности рисования, а не произвольно.</span><span class="sxs-lookup"><span data-stu-id="07cd3-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="07cd3-266">Этот вариант подходит для использования прямоугольника обрезки вместо слоя.</span><span class="sxs-lookup"><span data-stu-id="07cd3-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="07cd3-267">Повышение производительности — это больше для геометрических объектов, чем у сглаженных геометрических объектов.</span><span class="sxs-lookup"><span data-stu-id="07cd3-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="07cd3-268">Дополнительные сведения о выровняйте по оси клипов см. в разделе [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .</span><span class="sxs-lookup"><span data-stu-id="07cd3-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07cd3-269">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="07cd3-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07cd3-270">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="07cd3-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 