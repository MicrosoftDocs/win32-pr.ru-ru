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
ms.openlocfilehash: cf7cfa41c3decc964492258dad9c6a3a497f504b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089192"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a><span data-ttu-id="8e9c4-111">Общие сведения о взаимодействии Direct2D и Direct3D</span><span class="sxs-lookup"><span data-stu-id="8e9c4-111">Direct2D and Direct3D Interoperability Overview</span></span>

<span data-ttu-id="8e9c4-112">Высокопроизводительные и трехмерные графики с аппаратным ускорением все чаще становятся частью приложений, не являющихся играми, и большинство игровых приложений используют Двумерные графики в виде меню и Heads-Up отображения (Худс).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-112">Hardware accelerated 2-D and 3-D graphics are increasingly becoming a part of non-gaming applications, and most gaming applications use 2-D graphics in the form of menus and Heads-Up Displays (HUDs).</span></span> <span data-ttu-id="8e9c4-113">Существует множество значений, которые можно добавить, включив традиционную плоскую отрисовку для эффективного использования при визуализации Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-113">There is lots of value that can be added by enabling traditional 2-D rendering to be mixed with Direct3D rendering in an efficient manner.</span></span>

<span data-ttu-id="8e9c4-114">В этом разделе описывается интеграция двухмерной и трехмерной графики с помощью Direct2D и [Direct3D](../graphics-and-multimedia.md).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-114">This topic describes how to integrate 2-D and 3-D graphics by using Direct2D and [Direct3D](../graphics-and-multimedia.md).</span></span>

<span data-ttu-id="8e9c4-115">В него входят следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-115">It contains the following sections.</span></span>

-   [<span data-ttu-id="8e9c4-116">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="8e9c4-116">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="8e9c4-117">Поддерживаемые версии Direct3D</span><span class="sxs-lookup"><span data-stu-id="8e9c4-117">Supported Direct3D Versions</span></span>](#supported-direct3d-versions)
-   [<span data-ttu-id="8e9c4-118">Взаимодействие через DXGI</span><span class="sxs-lookup"><span data-stu-id="8e9c4-118">Interoperability Through DXGI</span></span>](#interoperability-through-dxgi)
-   [<span data-ttu-id="8e9c4-119">Запись в поверхность Direct3D с целевым объектом отрисовки поверхности DXGI</span><span class="sxs-lookup"><span data-stu-id="8e9c4-119">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [<span data-ttu-id="8e9c4-120">Создание поверхности DXGI</span><span class="sxs-lookup"><span data-stu-id="8e9c4-120">Creating a DXGI Surface</span></span>](#creating-a-dxgi-surface)
-   [<span data-ttu-id="8e9c4-121">Запись содержимого Direct2D в буфер цепочки подкачки</span><span class="sxs-lookup"><span data-stu-id="8e9c4-121">Writing Direct2D Content to a Swap Chain Buffer</span></span>](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [<span data-ttu-id="8e9c4-122">Пример: Рисование двухмерного фона</span><span class="sxs-lookup"><span data-stu-id="8e9c4-122">Example: Draw a 2-D Background</span></span>](#example-draw-a-2-d-background)
-   [<span data-ttu-id="8e9c4-123">Использование содержимого Direct2D в качестве текстуры</span><span class="sxs-lookup"><span data-stu-id="8e9c4-123">Using Direct2D Content as a Texture</span></span>](#using-direct2d-content-as-a-texture)
    -   [<span data-ttu-id="8e9c4-124">Пример. использование содержимого Direct2D в качестве текстуры</span><span class="sxs-lookup"><span data-stu-id="8e9c4-124">Example: Use Direct2D Content as a Texture</span></span>](#example-use-direct2d-content-as-a-texture)
-   [<span data-ttu-id="8e9c4-125">Изменение размера целевого объекта отрисовки поверхности DXGI</span><span class="sxs-lookup"><span data-stu-id="8e9c4-125">Resizing a DXGI Surface Render Target</span></span>](#resizing-a-dxgi-surface-render-target)
-   [<span data-ttu-id="8e9c4-126">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="8e9c4-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="8e9c4-127">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="8e9c4-127">Prerequisites</span></span>

<span data-ttu-id="8e9c4-128">В этом обзоре предполагается, что вы знакомы с базовыми операциями рисования Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-128">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="8e9c4-129">Инструкции см. в [кратком](direct2d-quickstart.md)руководстве по Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-129">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="8e9c4-130">Также предполагается, что вы можете программировать с помощью [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-130">It also assumes that you can program by using [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

## <a name="supported-direct3d-versions"></a><span data-ttu-id="8e9c4-131">Поддерживаемые версии Direct3D</span><span class="sxs-lookup"><span data-stu-id="8e9c4-131">Supported Direct3D Versions</span></span>

<span data-ttu-id="8e9c4-132">В DirectX 11,0 Direct2D поддерживает взаимодействие только с устройствами Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-132">With DirectX 11.0, Direct2D supports interoperability with Direct3D 10.1 devices only.</span></span> <span data-ttu-id="8e9c4-133">В DirectX 11,1 или более поздней версии Direct2D поддерживает взаимодействие с Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-133">With DirectX 11.1 or later, Direct2D supports interoperability with Direct3D 11 as well.</span></span>

## <a name="interoperability-through-dxgi"></a><span data-ttu-id="8e9c4-134">Взаимодействие через DXGI</span><span class="sxs-lookup"><span data-stu-id="8e9c4-134">Interoperability Through DXGI</span></span>

<span data-ttu-id="8e9c4-135">Начиная с Direct3D 10, среда выполнения Direct3D использует [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) для управления ресурсами.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-135">As of Direct3D 10, the Direct3D runtime uses [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) for resource management.</span></span> <span data-ttu-id="8e9c4-136">Уровень среды выполнения DXGI обеспечивает межпроцессное совместное использование поверхностей видеопамяти и служит основой для других платформ среды выполнения на основе видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-136">The DXGI runtime layer provides cross-process sharing of video memory surfaces and serves as the foundation for other video memory-based runtime platforms.</span></span> <span data-ttu-id="8e9c4-137">Direct2D использует DXGI для взаимодействия с Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-137">Direct2D uses DXGI to interoperate with Direct3D.</span></span>

<span data-ttu-id="8e9c4-138">Существует два основных способа совместного использования Direct2D и Direct3D:</span><span class="sxs-lookup"><span data-stu-id="8e9c4-138">There are two primary ways to use Direct2D and Direct3D together:</span></span>

-   <span data-ttu-id="8e9c4-139">Вы можете записать содержимое Direct2D на поверхность Direct3D, получив [**идксгисурфаце**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) и используя его с [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) , чтобы создать [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-139">You can write Direct2D content to a Direct3D surface by obtaining an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and using it with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="8e9c4-140">Затем можно использовать целевой объект отрисовки для добавления двумерного интерфейса или фона к трехмерной графике или использовать Direct2D рисунок в качестве текстуры для трехмерного объекта.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-140">You can then use the render target to add a two-dimensional interface or background to three-dimensional graphics, or use a Direct2D drawing as a texture for a three dimensional object.</span></span>
-   <span data-ttu-id="8e9c4-141">Используя [**креатешаредбитмап**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) для создания [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) из [**Идксгисурфаце**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), можно записать сцену Direct3D в растровое изображение и визуализировать ее с помощью Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-141">By using [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) from an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), you can write a Direct3D scene to a bitmap and render it with Direct2D.</span></span>

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a><span data-ttu-id="8e9c4-142">Запись в поверхность Direct3D с целевым объектом отрисовки поверхности DXGI</span><span class="sxs-lookup"><span data-stu-id="8e9c4-142">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>

<span data-ttu-id="8e9c4-143">Для записи в поверхность Direct3D вы получаете [**идксгисурфаце**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) и передаете его методу [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) для создания целевого объекта отрисовки поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-143">To write to a Direct3D surface, you obtain an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and pass it to the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create a DXGI surface render target.</span></span> <span data-ttu-id="8e9c4-144">Затем можно использовать целевой объект прорисовки поверхности DXGI для рисования двухмерного содержимого на поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-144">You can then use the DXGI surface render target to draw 2-D content to the DXGI surface.</span></span>

<span data-ttu-id="8e9c4-145">Целевой объект отрисовки поверхности DXGI — это разновидность [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-145">A DXGI surface render target is a kind of [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="8e9c4-146">Как и другие целевые объекты рендеринга Direct2D, их можно использовать для создания ресурсов и выполнения команд рисования.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-146">Like other Direct2D render targets, you can use it to create resources and issue drawing commands.</span></span>

<span data-ttu-id="8e9c4-147">Целевой объект прорисовки поверхности DXGI и поверхность DXGI должны использовать один и тот же формат DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-147">The DXGI surface render target and the DXGI surface must use the same DXGI format.</span></span> <span data-ttu-id="8e9c4-148">Если при создании целевого объекта рендеринга указать формат неизвестного формата DXGI, он будет автоматически использовать формат поверхности. [**\_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="8e9c4-148">If you specify the [**DXGI\_FORMAT\_UNKOWN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format when you create the render target, it will automatically use the surface's format.</span></span>

<span data-ttu-id="8e9c4-149">Целевой объект прорисовки поверхности DXGI не выполняет синхронизацию рабочей области DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-149">The DXGI surface render target does not perform DXGI surface synchronization.</span></span>

### <a name="creating-a-dxgi-surface"></a><span data-ttu-id="8e9c4-150">Создание поверхности DXGI</span><span class="sxs-lookup"><span data-stu-id="8e9c4-150">Creating a DXGI Surface</span></span>

<span data-ttu-id="8e9c4-151">С помощью Direct3D 10 существует несколько способов получить поверхность DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-151">With Direct3D 10, there are several ways to obtain a DXGI surface.</span></span> <span data-ttu-id="8e9c4-152">Вы можете создать [**идксгисвапчаин**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) для устройства, а затем использовать метод метода цепочки [**буферов**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) для получения поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-152">You can create an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) for a device, then use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span> <span data-ttu-id="8e9c4-153">Вы также можете использовать устройство для создания текстуры, а затем использовать эту текстуру в качестве поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-153">Or, you can use a device to create a texture, then use that texture as a DXGI surface.</span></span>

<span data-ttu-id="8e9c4-154">Независимо от того, как вы создаете поверхность DXGI, поверхность должна использовать один из форматов DXGI, поддерживаемых объектами рендеринга поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-154">Regardless of how you create the DXGI surface, the surface must use one of the DXGI formats supported by DXGI surface render targets.</span></span> <span data-ttu-id="8e9c4-155">Список см. в разделе [Поддерживаемые форматы пикселей и альфа-режимы](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-155">For a list, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="8e9c4-156">Кроме того, [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) , связанный с ПОВЕРХНОСТЬю DXGI, должен поддерживать форматы BGRA DXGI, чтобы поверхность работала с Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-156">Additionally, the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the DXGI surface must support BGRA DXGI formats for the surface to work with Direct2D.</span></span> <span data-ttu-id="8e9c4-157">Чтобы обеспечить эту поддержку, используйте флаг [**D3D10 \_ Create \_ Device \_ BGRA \_ support**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) при вызове метода [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) для создания устройства.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-157">To ensure this support, use the [**D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag when you call the [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) method to create the device.</span></span>

<span data-ttu-id="8e9c4-158">В следующем коде определяется метод, создающий [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-158">The following code defines a method that creates an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span></span> <span data-ttu-id="8e9c4-159">Он выбирает оптимальный уровень функций и возвращается к [платформе Windows Advanced растеризации (деформация)](./installing-the-direct2d-debug-layer.md) , если аппаратная отрисовка недоступна.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-159">It selects the best feature level available and falls back to [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) when hardware rendering is not available.</span></span>


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



<span data-ttu-id="8e9c4-160">В следующем примере кода используется `CreateD3DDevice` метод, показанный в предыдущем примере, для создания устройства Direct3D, которое может создавать поверхности DXGI для использования с Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-160">The next code example uses the `CreateD3DDevice` method shown in the previous example to create a Direct3D device that can create DXGI surfaces for use with Direct2D.</span></span>


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



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a><span data-ttu-id="8e9c4-161">Запись содержимого Direct2D в буфер цепочки подкачки</span><span class="sxs-lookup"><span data-stu-id="8e9c4-161">Writing Direct2D Content to a Swap Chain Buffer</span></span>

<span data-ttu-id="8e9c4-162">Самый простой способ добавить Direct2D содержимое в сцену Direct3D — использовать [**метод метода**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) [**идксгисвапчаин**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) для получения поверхности DXGI, а затем использовать поверхность с методом [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) для создания [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) , с помощью которого будет нарисовано трехмерное содержимое.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-162">The simplest way to add Direct2D content to a Direct3D scene is to use the [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method of an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) to obtain a DXGI surface, then use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) with which to draw your 2-D content.</span></span>

<span data-ttu-id="8e9c4-163">Этот подход не отображает содержимое в трех измерениях. Он не будет иметь перспективу или глубину.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-163">This approach does not render your content in three dimensions; it will not have perspective or depth.</span></span> <span data-ttu-id="8e9c4-164">Однако это полезно для нескольких распространенных задач:</span><span class="sxs-lookup"><span data-stu-id="8e9c4-164">However, it is useful for several common tasks:</span></span>

-   <span data-ttu-id="8e9c4-165">Создание двухмерного фона для трехмерной сцены.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-165">Creating a 2-D background for a 3-D scene.</span></span>
-   <span data-ttu-id="8e9c4-166">Создание двухмерного интерфейса перед трехмерной сценой.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-166">Creating a 2-D interface in front of a 3-D scene.</span></span>
-   <span data-ttu-id="8e9c4-167">Использование множественной выборки Direct3D при отрисовке содержимого Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-167">Using Direct3D multisampling when rendering Direct2D content.</span></span>

<span data-ttu-id="8e9c4-168">В следующем разделе показано, как создать двумерной фон для трехмерной сцены.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-168">The next section shows how to create a 2-D background for a 3-D scene.</span></span>

### <a name="example-draw-a-2-d-background"></a><span data-ttu-id="8e9c4-169">Пример: Рисование двухмерного фона</span><span class="sxs-lookup"><span data-stu-id="8e9c4-169">Example: Draw a 2-D Background</span></span>

<span data-ttu-id="8e9c4-170">В следующих шагах описывается создание целевого объекта отрисовки поверхности DXGI и его использование для рисования градиентного фона.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-170">The following steps describe how to create a DXGI surface render target and use it to draw a gradient background.</span></span>

1.  <span data-ttu-id="8e9c4-171">Используйте метод [**креатесвапчаин**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) для создания цепочки буферов для [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (переменная *\_ пдевице m* ).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-171">Use the [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) method to create a swap chain for an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (the *m\_pDevice* variable).</span></span> <span data-ttu-id="8e9c4-172">Цепочка буферов обмена использует формат DXGI [**\_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, один из форматов DXGI, поддерживаемых Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-172">The swap chain uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

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

    

2.  <span data-ttu-id="8e9c4-173">Используйте метод метода buffer цепочки [**буферов**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) для получения поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-173">Use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span>

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  <span data-ttu-id="8e9c4-174">Используйте поверхность DXGI для создания целевого объекта отрисовки DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-174">Use the DXGI surface to create a DXGI render target.</span></span>
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



    

4.  <span data-ttu-id="8e9c4-175">Чтобы нарисовать градиентный фон, используйте целевой объект рендеринга.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-175">Use the render target to draw a gradient background.</span></span>

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



    

<span data-ttu-id="8e9c4-176">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-176">Code is omitted from this sample.</span></span>

## <a name="using-direct2d-content-as-a-texture"></a><span data-ttu-id="8e9c4-177">Использование содержимого Direct2D в качестве текстуры</span><span class="sxs-lookup"><span data-stu-id="8e9c4-177">Using Direct2D Content as a Texture</span></span>

<span data-ttu-id="8e9c4-178">Другим способом использования Direct2D содержимого с помощью Direct3D является использование Direct2D для создания двухмерной текстуры, а затем применение текстуры к трехмерной модели.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-178">Another way to use Direct2D content with Direct3D is to use Direct2D to generate a 2-D texture and then apply that texture to a 3-D model.</span></span> <span data-ttu-id="8e9c4-179">Это делается путем создания [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), получения поверхности DXGI из текстуры и последующего использования поверхности для создания целевого объекта отрисовки поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-179">You do this by creating an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtaining a DXGI surface from the texture, and then using the surface to create a DXGI surface render target.</span></span> <span data-ttu-id="8e9c4-180">Поверхность **ID3D10Texture2D** должна использовать флаг привязки [**\_ \_ \_ целевого объекта ПРОРИСОВКи D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) и использовать формат DXGI, поддерживаемый целями рендеринга поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-180">The **ID3D10Texture2D** surface must use the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) bind flag and use a DXGI format supported by DXGI surface render targets.</span></span> <span data-ttu-id="8e9c4-181">Список поддерживаемых форматов DXGI см. в разделе [Поддерживаемые форматы пикселей и альфа-режимы](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-181">For a list of supported DXGI formats, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

### <a name="example-use-direct2d-content-as-a-texture"></a><span data-ttu-id="8e9c4-182">Пример. использование содержимого Direct2D в качестве текстуры</span><span class="sxs-lookup"><span data-stu-id="8e9c4-182">Example: Use Direct2D Content as a Texture</span></span>

<span data-ttu-id="8e9c4-183">В следующих примерах показано, как создать целевой объект отрисовки поверхности DXGI, который визуализируется в двумерной текстуре (представленной [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span><span class="sxs-lookup"><span data-stu-id="8e9c4-183">The following examples show how to create a DXGI surface render target that renders to a 2-D texture (represented by an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span></span>

1.  <span data-ttu-id="8e9c4-184">Во-первых, используйте устройство Direct3D для создания двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-184">First, use a Direct3D device to create a 2-D texture.</span></span> <span data-ttu-id="8e9c4-185">Текстура использует [**\_ \_ \_ целевой объект прорисовки привязки D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) и флаги привязки **D3D10 \_ привязки \_ \_ ресурса шейдера** и использует [**Формат DXGI \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI, один из форматов DXGI, поддерживаемых Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-185">The texture uses the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) and **D3D10\_BIND\_SHADER\_RESOURCE** bind flags, and it uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

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

    

2.  <span data-ttu-id="8e9c4-186">Используйте текстуру для получения поверхности DXGI.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-186">Use the texture to obtain a DXGI surface.</span></span>

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  <span data-ttu-id="8e9c4-187">Используйте поверхность с методом [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) , чтобы получить целевой объект прорисовки Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-187">Use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to obtain a Direct2D render target.</span></span>

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



    

<span data-ttu-id="8e9c4-188">Теперь, когда вы получили целевой объект рендеринга Direct2D и со его с текстурой Direct3D, вы можете использовать целевой объект рендеринга для рисования содержимого Direct2D в этой текстуре, и вы можете применить эту текстуру к примитивам Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-188">Now that you have obtained a Direct2D render target and associated it with a Direct3D texture, you can use the render target to draw Direct2D content to that texture, and you can apply that texture to Direct3D primitives.</span></span>

<span data-ttu-id="8e9c4-189">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-189">Code is omitted from this sample.</span></span>

## <a name="resizing-a-dxgi-surface-render-target"></a><span data-ttu-id="8e9c4-190">Изменение размера целевого объекта отрисовки поверхности DXGI</span><span class="sxs-lookup"><span data-stu-id="8e9c4-190">Resizing a DXGI Surface Render Target</span></span>

<span data-ttu-id="8e9c4-191">Целевые объекты прорисовки поверхности DXGI не поддерживают метод [**ID2D1RenderTarget:: resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) .</span><span class="sxs-lookup"><span data-stu-id="8e9c4-191">DXGI surface render targets do not support the [**ID2D1RenderTarget::Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) method.</span></span> <span data-ttu-id="8e9c4-192">Чтобы изменить размер целевого объекта рендеринга для поверхности DXGI, приложение должно освободить и создать его повторно.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-192">To resize a DXGI surface render target, the application must release and re-create it.</span></span>

<span data-ttu-id="8e9c4-193">Эта операция потенциально может привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-193">This operation can potentially create performance issues.</span></span> <span data-ttu-id="8e9c4-194">Целью отрисовки может быть последний активный ресурс Direct2D, который хранит ссылку на [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) , связанный с поверхностью DXGI целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-194">The render target might be the last active Direct2D resource that keeps a reference to the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the render target's DXGI surface.</span></span> <span data-ttu-id="8e9c4-195">Если приложение освобождает целевой объект отрисовки, а ссылка **ID3D10Device1** уничтожается, новый объект должен быть создан заново.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-195">If the application releases the render target and the **ID3D10Device1** reference is destroyed, a new one must be recreated.</span></span>

<span data-ttu-id="8e9c4-196">Эту потенциально дорогостоящую операцию можно избежать, сохранив по крайней мере один ресурс Direct2D, созданный целевым объектом рендеринга, при повторном создании этого целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-196">You can avoid this potentially expensive operation by keeping at least one Direct2D resource that was created by the render target while you re-create that render target.</span></span> <span data-ttu-id="8e9c4-197">Ниже приведены некоторые Direct2D ресурсы, которые подходят для этого подхода:</span><span class="sxs-lookup"><span data-stu-id="8e9c4-197">The following are some Direct2D resources that work for this approach:</span></span>

-   <span data-ttu-id="8e9c4-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (который может храниться косвенно [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span><span class="sxs-lookup"><span data-stu-id="8e9c4-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (which may be held indirectly by an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span></span>
-   [<span data-ttu-id="8e9c4-199">**ID2D1Layer**</span><span class="sxs-lookup"><span data-stu-id="8e9c4-199">**ID2D1Layer**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [<span data-ttu-id="8e9c4-200">**ID2D1Mesh**</span><span class="sxs-lookup"><span data-stu-id="8e9c4-200">**ID2D1Mesh**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

<span data-ttu-id="8e9c4-201">Для реализации этого подхода метод изменения размера должен проверить, доступно ли устройство Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-201">To accommodate this approach, your resize method should test to see whether the Direct3D device is available.</span></span> <span data-ttu-id="8e9c4-202">Если она доступна, выпустите и повторно создайте целевые объекты отрисовки для поверхности DXGI, но сохраните все созданные ранее ресурсы и используйте их повторно.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-202">If it is available, release and re-create your DXGI surface render targets, but keep all the resources that they created previously and reuse them.</span></span> <span data-ttu-id="8e9c4-203">Это работает потому, что, как описано в [обзоре ресурсов](resources-and-resource-domains.md), ресурсы, созданные двумя целевыми объектами рендеринга, совместимы, если обе цели рендеринга связаны с одним и тем же устройством Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8e9c4-203">This works because, as described in the [Resources Overview](resources-and-resource-domains.md), resources created by two render targets are compatible when both render targets are associated with the same Direct3D device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e9c4-204">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="8e9c4-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e9c4-205">Поддерживаемые форматы пикселей и режимы альфа-канала</span><span class="sxs-lookup"><span data-stu-id="8e9c4-205">Supported Pixel Formats and Alpha Modes</span></span>](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

<span data-ttu-id="8e9c4-206">[**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="8e9c4-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span></span>
</dt> <dt>

[<span data-ttu-id="8e9c4-207">Графическая система Windows DirectX</span><span class="sxs-lookup"><span data-stu-id="8e9c4-207">Windows DirectX Graphics</span></span>](../graphics-and-multimedia.md)
</dt> </dl>

 

 
