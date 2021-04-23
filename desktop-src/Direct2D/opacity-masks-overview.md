---
title: Общие сведения о масках непрозрачности
description: В этом разделе описывается использование точечных рисунков и кистей для определения масок непрозрачности. В него входят следующие разделы.
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a4757a30247da465e0ae5226bd923219e3e665
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104561212"
---
# <a name="opacity-masks-overview"></a><span data-ttu-id="7b586-104">Общие сведения о масках непрозрачности</span><span class="sxs-lookup"><span data-stu-id="7b586-104">Opacity Masks Overview</span></span>

<span data-ttu-id="7b586-105">В этом разделе описывается использование точечных рисунков и кистей для определения масок непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-105">This topic describes how to use bitmaps and brushes to define opacity masks.</span></span> <span data-ttu-id="7b586-106">В него входят следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="7b586-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="7b586-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7b586-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="7b586-108">Что такое маска непрозрачности?</span><span class="sxs-lookup"><span data-stu-id="7b586-108">What Is an Opacity Mask?</span></span>](#what-is-an-opacity-mask)
-   [<span data-ttu-id="7b586-109">Использование точечного рисунка в качестве маски непрозрачности с помощью метода ФиллопаЦитимаск</span><span class="sxs-lookup"><span data-stu-id="7b586-109">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [<span data-ttu-id="7b586-110">Использование кисти в качестве маски непрозрачности с помощью метода Филлжеометри</span><span class="sxs-lookup"><span data-stu-id="7b586-110">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [<span data-ttu-id="7b586-111">Использование кисти линейного градиента в качестве маски непрозрачности</span><span class="sxs-lookup"><span data-stu-id="7b586-111">Use an Linear Gradient Brush as an Opacity Mask</span></span>](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [<span data-ttu-id="7b586-112">Использование кисти радиального градиента в качестве маски непрозрачности</span><span class="sxs-lookup"><span data-stu-id="7b586-112">Use a Radial Gradient Brush as an Opacity Mask</span></span>](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [<span data-ttu-id="7b586-113">Применение маски непрозрачности к слою</span><span class="sxs-lookup"><span data-stu-id="7b586-113">Apply an Opacity Mask to a Layer</span></span>](#apply-an-opacity-mask-to-a-layer)
-   [<span data-ttu-id="7b586-114">См. также</span><span class="sxs-lookup"><span data-stu-id="7b586-114">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="7b586-115">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7b586-115">Prerequisites</span></span>

<span data-ttu-id="7b586-116">В этом обзоре предполагается, что вы знакомы с базовыми операциями рисования Direct2D, как описано в пошаговом руководстве [Создание простого Direct2D приложения](direct2d-quickstart.md) .</span><span class="sxs-lookup"><span data-stu-id="7b586-116">This overview assumes that you are familiar with basic Direct2D drawing operations, as described in the [Creating a Simple Direct2D Application](direct2d-quickstart.md) walkthrough.</span></span> <span data-ttu-id="7b586-117">Также следует ознакомиться с различными типами кистей, как описано в [обзоре кистей](direct2d-brushes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7b586-117">You should also be familiar with the different types of brushes, as described in the [Brushes Overview](direct2d-brushes-overview.md).</span></span>

## <a name="what-is-an-opacity-mask"></a><span data-ttu-id="7b586-118">Что такое маска непрозрачности?</span><span class="sxs-lookup"><span data-stu-id="7b586-118">What Is an Opacity Mask?</span></span>

<span data-ttu-id="7b586-119">Маска непрозрачности — это маска, описываемая кистью или точечным рисунком, которая применяется к другому объекту, чтобы сделать этот объект частично или полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="7b586-119">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="7b586-120">Маска непрозрачности использует сведения о альфа-канале для указания того, как исходные пикселы объекта смешиваются в конечном целевом объекте назначения.</span><span class="sxs-lookup"><span data-stu-id="7b586-120">An opacity mask uses alpha channel information to specify how the source pixels of the object are blended into the final destination target.</span></span> <span data-ttu-id="7b586-121">Прозрачные части маски указывают области, в которых базовое изображение скрыто, а непрозрачные части маски указывают, где отображается маскированный объект.</span><span class="sxs-lookup"><span data-stu-id="7b586-121">The transparent portions of the mask indicate the areas where the underlying image is hidden, whereas the opaque portions of the mask indicate where the masked object is visible.</span></span>

<span data-ttu-id="7b586-122">Существует несколько способов применения маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-122">There are several ways to apply an opacity mask:</span></span>

-   <span data-ttu-id="7b586-123">Используйте метод [**ID2D1RenderTarget:: филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="7b586-123">Use the [**ID2D1RenderTarget::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method.</span></span> <span data-ttu-id="7b586-124">Метод **филлопаЦитимаск** закрашивает прямоугольную область целевого объекта прорисовки, а затем применяет маску непрозрачности, определенную точечным рисунком.</span><span class="sxs-lookup"><span data-stu-id="7b586-124">The **FillOpacityMask** method paints a rectangular region of a render target and then applies an opacity mask, defined by a bitmap.</span></span> <span data-ttu-id="7b586-125">Используйте этот метод, если маска непрозрачности является точечным рисунком и требуется заполнить прямоугольную область.</span><span class="sxs-lookup"><span data-stu-id="7b586-125">Use this method when your opacity mask is a bitmap and you want to fill a rectangular region.</span></span>
-   <span data-ttu-id="7b586-126">Используйте метод [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="7b586-126">Use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="7b586-127">Метод **филлжеометри** Закрашивает внутреннюю часть геометрии с указанным [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), а затем применяет маску непрозрачности, определенную кистью.</span><span class="sxs-lookup"><span data-stu-id="7b586-127">The **FillGeometry** method paints the interior of geometry with the specified [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), then applies an opacity mask, defined by a brush.</span></span> <span data-ttu-id="7b586-128">Используйте этот метод, если необходимо применить маску непрозрачности к геометрии или вы хотите использовать кисть в качестве маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-128">Use this method when you want to apply an opacity mask to a geometry or you want to use a brush as an opacity mask.</span></span>
-   <span data-ttu-id="7b586-129">Используйте [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , чтобы применить маску непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-129">Use an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) to apply an opacity mask.</span></span> <span data-ttu-id="7b586-130">Используйте этот подход, если необходимо применить маску непрозрачности к группе содержимого рисунка, а не только к одной фигуре или изображению.</span><span class="sxs-lookup"><span data-stu-id="7b586-130">Use this approach when you want to apply an opacity mask to a group of drawing content, not just a single shape or image.</span></span> <span data-ttu-id="7b586-131">Дополнительные сведения см. в разделе [Общие сведения о слоях](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7b586-131">For details, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a><span data-ttu-id="7b586-132">Использование точечного рисунка в качестве маски непрозрачности с помощью метода ФиллопаЦитимаск</span><span class="sxs-lookup"><span data-stu-id="7b586-132">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>

<span data-ttu-id="7b586-133">Метод [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) закрашивает прямоугольную область целевого объекта прорисовки, а затем применяет маску непрозрачности, определенную [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="7b586-133">The [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method paints a rectangular region of a render target and then applies an opacity mask, defined by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="7b586-134">Используйте этот метод при наличии точечного рисунка, который необходимо использовать в качестве маски непрозрачности для прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="7b586-134">Use this method when you have a bitmap that you want to use as an opacity mask for a rectangular region.</span></span>

<span data-ttu-id="7b586-135">На следующей схеме показан результат применения маски непрозрачности ( [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) с изображением цветок) к [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) с изображением Ферн растения.</span><span class="sxs-lookup"><span data-stu-id="7b586-135">The following diagram shows an effect of applying the opacity mask (an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with an image of a flower) to an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with an image of a fern plant.</span></span> <span data-ttu-id="7b586-136">Полученный рисунок является растровым изображением растения, обрезанным на фигурном цветок.</span><span class="sxs-lookup"><span data-stu-id="7b586-136">The resulting image is a bitmap of a plant clipped to the flower shape.</span></span>

![Схема точечного рисунка цвета, используемого в качестве маски непрозрачности на изображении Ферн растения](images/brushes-ovw-bitmapopacity.png)

<span data-ttu-id="7b586-138">В следующем примере кода показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="7b586-138">The following code examples shows how this is accomplished.</span></span>

<span data-ttu-id="7b586-139">В первом примере загружается следующий точечный рисунок *m \_ пбитмапмаск* для использования в качестве маски точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="7b586-139">The first example loads the following bitmap, *m\_pBitmapMask*, for use as a bitmap mask.</span></span> <span data-ttu-id="7b586-140">На следующем рисунке показан полученный результат.</span><span class="sxs-lookup"><span data-stu-id="7b586-140">The following illustration shows the output that is produced.</span></span> <span data-ttu-id="7b586-141">Обратите внимание, что хотя непрозрачная часть точечного рисунка отображается черным цветом, сведения о цвете в растровом изображении не влияют на маску непрозрачности. используется только информация о непрозрачности каждого пикселя в точечном рисунке.</span><span class="sxs-lookup"><span data-stu-id="7b586-141">Note that, although the opaque portion of the bitmap appears black, the color information in the bitmap has no effect on the opacity mask; only the opacity information of each pixel in the bitmap is used.</span></span> <span data-ttu-id="7b586-142">Полностью непрозрачные Пиксели в этом точечном рисунке окрашены черным цветом только в целях наглядности.</span><span class="sxs-lookup"><span data-stu-id="7b586-142">The fully opaque pixels in this bitmap have been colored black for illustrative purposes only.</span></span>

![Иллюстрация маски точечного рисунка цветок](images/bitmapmask.png)

<span data-ttu-id="7b586-144">В этом примере [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) загружается вспомогательным методом лоадресаурцебитмап, который определен в любом расположении в образце.</span><span class="sxs-lookup"><span data-stu-id="7b586-144">In this example, the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is loaded by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



<span data-ttu-id="7b586-145">В следующем примере определяется кисть *m \_ пфернбитмапбруш*, к которой применяется маска непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-145">The next example defines the brush, *m\_pFernBitmapBrush*, to which the opacity mask is applied.</span></span> <span data-ttu-id="7b586-146">В этом примере используется [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , содержащий изображение Ферн, но вместо него можно использовать [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)или [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="7b586-146">This example uses an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that contains an image of a fern, but you could use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) instead.</span></span> <span data-ttu-id="7b586-147">На следующем рисунке показан полученный результат.</span><span class="sxs-lookup"><span data-stu-id="7b586-147">The following illustration shows the output that is produced.</span></span>

![Иллюстрация точечного рисунка, используемого растровой кистью](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





<span data-ttu-id="7b586-149">Теперь, когда определена маска непрозрачности и кисть, можно использовать метод [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) в методе отрисовки приложения.</span><span class="sxs-lookup"><span data-stu-id="7b586-149">Now that opacity mask and the brush are defined, you can use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method in your application's rendering method.</span></span> <span data-ttu-id="7b586-150">При вызове метода **филлопаЦитимаск** необходимо указать тип маски непрозрачности, которую вы используете: D2D1, **\_ \_ \_ содержимое \_** маски непрозрачности, **\_ текст непрозрачности D2D1, \_ \_ \_ \_ естественное**, а также **\_ \_ \_ \_ \_ \_ совместимый с содержимым GDI содержимое маски непрозрачности Text**.</span><span class="sxs-lookup"><span data-stu-id="7b586-150">When you call the **FillOpacityMask** method, you must specify the type of opacity mask you are using: **D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**, **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_NATURAL**, and **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_GDI\_COMPATIBLE**.</span></span> <span data-ttu-id="7b586-151">Значения этих трех типов см. в разделе [**\_ \_ \_ содержимое маски непрозрачности D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span><span class="sxs-lookup"><span data-stu-id="7b586-151">For the meanings of these three types, see [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span></span>

> [!Note]  
> <span data-ttu-id="7b586-152">Начиная с Windows 8, [**\_ \_ \_ содержимое маски непрозрачности D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) не требуется.</span><span class="sxs-lookup"><span data-stu-id="7b586-152">Starting with Windows 8, the [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) is not required.</span></span> <span data-ttu-id="7b586-153">См. метод [**ID2D1DeviceContext:: филлопаЦитимаск**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) , у которого нет **параметра \_ \_ \_ содержимого маски непрозрачности D2D1** .</span><span class="sxs-lookup"><span data-stu-id="7b586-153">See the [**ID2D1DeviceContext::FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) method, which has no **D2D1\_OPACITY\_MASK\_CONTENT** parameter.</span></span>

 

<span data-ttu-id="7b586-154">В следующем примере задается режим сглаживания целевого объекта отрисовки в [**D2D1 \_ \_ режим сглаживания с \_ псевдонимами**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) , чтобы маска непрозрачности работала правильно.</span><span class="sxs-lookup"><span data-stu-id="7b586-154">The next example sets the render target's antialiasing mode to [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) so that the opacity mask will work properly.</span></span> <span data-ttu-id="7b586-155">Затем он вызывает метод [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) и передает ему маску непрозрачности (*m \_ пбитмапмаск*), кисть, к которой применяется маска непрозрачности (*m \_ пфернбитмапбруш*), тип содержимого внутри маски непрозрачности [**( \_ \_ \_ \_ график содержимого маски непрозрачности D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) и область для рисования.</span><span class="sxs-lookup"><span data-stu-id="7b586-155">It then calls the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method and passes it the opacity mask (*m\_pBitmapMask*), the brush to which the opacity mask is applied (*m\_pFernBitmapBrush*), the type of content inside the opacity mask ([**D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)), and the area to paint.</span></span> <span data-ttu-id="7b586-156">На следующем рисунке показан полученный результат.</span><span class="sxs-lookup"><span data-stu-id="7b586-156">The following illustration shows the output that is produced.</span></span>

![Иллюстрация изображения Ферн на предприятии с примененной маской непрозрачности](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





<span data-ttu-id="7b586-158">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="7b586-158">Code has been omitted from this example.</span></span>

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a><span data-ttu-id="7b586-159">Использование кисти в качестве маски непрозрачности с помощью метода Филлжеометри</span><span class="sxs-lookup"><span data-stu-id="7b586-159">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>

<span data-ttu-id="7b586-160">В предыдущем разделе описано, как использовать [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) в качестве маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-160">The preceding section described how to use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) as an opacity mask.</span></span> <span data-ttu-id="7b586-161">Direct2D также предоставляет метод [**ID2D1RenderTarget:: филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , который позволяет при необходимости указать кисть в качестве маски непрозрачности при заполнении [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span><span class="sxs-lookup"><span data-stu-id="7b586-161">Direct2D also provides the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, which enables you to optionally specify brush as an opacity mask when you fill an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span></span> <span data-ttu-id="7b586-162">Это позволяет создавать маски непрозрачности на основе градиентов (с помощью [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) или [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) и точечных рисунков (с помощью **ID2D1Bitmap**).</span><span class="sxs-lookup"><span data-stu-id="7b586-162">This enables you to create opacity masks from gradients (using [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) and bitmaps (using **ID2D1Bitmap**).</span></span>

<span data-ttu-id="7b586-163">Метод [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) принимает три параметра:</span><span class="sxs-lookup"><span data-stu-id="7b586-163">The [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method takes three parameters:</span></span>

-   <span data-ttu-id="7b586-164">Первый параметр, [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), определяет фигуру для рисования.</span><span class="sxs-lookup"><span data-stu-id="7b586-164">The first parameter, an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), defines the shape to paint.</span></span>
-   <span data-ttu-id="7b586-165">Второй параметр, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), указывает кисть, используемую для рисования геометрии.</span><span class="sxs-lookup"><span data-stu-id="7b586-165">The second parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies the brush used to paint the geometry.</span></span> <span data-ttu-id="7b586-166">Этот параметр должен быть [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , для которого в качестве режимов расширения x и y задано значение [**D2D1 в качестве \_ \_ \_ зажима режима расширения**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="7b586-166">This parameter must be an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that has its x- and y-extend modes set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>
-   <span data-ttu-id="7b586-167">Третий параметр, [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), задает кисть для использования в качестве маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-167">The third parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies a brush to use as the opacity mask.</span></span> <span data-ttu-id="7b586-168">Эта кисть может быть [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)или [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="7b586-168">This brush may be an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), or an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span> <span data-ttu-id="7b586-169">(Технически вы можете использовать [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), но использование сплошной цветовой кисти в качестве маски непрозрачности не дает интересных результатов.)</span><span class="sxs-lookup"><span data-stu-id="7b586-169">(Technically, you may use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), but using a solid color brush as an opacity mask doesn't produce interesting results.)</span></span>

<span data-ttu-id="7b586-170">В следующих разделах описывается использование объектов [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) и [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) в качестве масок непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-170">The following sections describe how to use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) and [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) objects as opacity masks.</span></span>

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="7b586-171">Использование кисти линейного градиента в качестве маски непрозрачности</span><span class="sxs-lookup"><span data-stu-id="7b586-171">Use an Linear Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="7b586-172">На следующей диаграмме показан результат применения кисти линейного градиента к прямоугольнику, который заполняется растровым изображением цветов.</span><span class="sxs-lookup"><span data-stu-id="7b586-172">The following diagram shows the effect of applying a linear gradient brush to a rectangle that is filled with a bitmap of flowers.</span></span>

![Схема точечного рисунка цветок с примененной кистью линейного градиента](images/brushes-ovw-lineargradient-opacitymask.png)

<span data-ttu-id="7b586-174">В следующих шагах описывается, как повторно создать этот результат.</span><span class="sxs-lookup"><span data-stu-id="7b586-174">The steps that follow describe how to re-create this effect.</span></span>

1.  <span data-ttu-id="7b586-175">Определяет содержимое для маскирования.</span><span class="sxs-lookup"><span data-stu-id="7b586-175">Define the content to be masked.</span></span> <span data-ttu-id="7b586-176">В следующем примере создается [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ плинеарфадефловерсбитмап*.</span><span class="sxs-lookup"><span data-stu-id="7b586-176">The following example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pLinearFadeFlowersBitmap*.</span></span> <span data-ttu-id="7b586-177">В режиме расширения x и y для *m \_ плинеарфадефловерсбитмап* устанавливается значение D2D1 в качестве маскирующего [**\_ \_ режима \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) , чтобы его можно было использовать с маской непрозрачности методом [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="7b586-177">The extend mode x- and y- for *m\_pLinearFadeFlowersBitmap* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) so that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="7b586-178">C++</span><span class="sxs-lookup"><span data-stu-id="7b586-178">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="7b586-179">C++</span><span class="sxs-lookup"><span data-stu-id="7b586-179">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  <span data-ttu-id="7b586-180">Определите маску непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-180">Define the opacity mask.</span></span> <span data-ttu-id="7b586-181">В следующем примере кода создается кисть диагонального линейного градиента (*m \_ плинеарградиентбруш*), которая плавно исчезает от полностью непрозрачного черного в позиции 0 до полностью прозрачного белого в позиции 1.</span><span class="sxs-lookup"><span data-stu-id="7b586-181">The next code example creates a diagonal linear gradient brush (*m\_pLinearGradientBrush*) that fades from fully opaque black at position 0 to completely transparent white at position 1.</span></span>
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  <span data-ttu-id="7b586-182">Используйте метод [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="7b586-182">Use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="7b586-183">В последнем примере метод **филлжеометри** используется в качестве кисти содержимого для заполнения [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ пректжео*) на [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ плинеарфадефловерсбитмап*) и применяет маску непрозрачности (*m \_ плинеарградиентбруш*).</span><span class="sxs-lookup"><span data-stu-id="7b586-183">The final example uses the **FillGeometry** method to the content brush to fill a [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*) with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pLinearFadeFlowersBitmap*) and applies an opacity mask (*m\_pLinearGradientBrush*).</span></span>
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

<span data-ttu-id="7b586-184">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="7b586-184">Code has been omitted from this example.</span></span>

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="7b586-185">Использование кисти радиального градиента в качестве маски непрозрачности</span><span class="sxs-lookup"><span data-stu-id="7b586-185">Use a Radial Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="7b586-186">На следующей диаграмме показан визуальный результат применения кисти радиального градиента к прямоугольнику, который заполняется растровым изображением фолиаже.</span><span class="sxs-lookup"><span data-stu-id="7b586-186">The following diagram shows the visual effect of applying a radial gradient brush to a rectangle that is filled with a bitmap of foliage.</span></span>

![Схема точечного рисунка фолиаже с примененной кистью радиального градиента](images/brushes-ovw-radialgradient-opacitymask.png)

<span data-ttu-id="7b586-188">В первом примере создается [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ прадиалфадефловерсбитмапбруш*.</span><span class="sxs-lookup"><span data-stu-id="7b586-188">The first example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pRadialFadeFlowersBitmapBrush*.</span></span> <span data-ttu-id="7b586-189">Чтобы его можно было использовать с маской непрозрачности с помощью метода [**филлжеометри**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , в качестве режима расширения x и y для *m \_ прадиалфадефловерсбитмапбруш* устанавливается значение [**D2D1 в \_ \_ режиме расширения \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="7b586-189">So that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, the extend mode x- and y- for *m\_pRadialFadeFlowersBitmapBrush* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b586-190">C++</span><span class="sxs-lookup"><span data-stu-id="7b586-190">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b586-191">C++</span><span class="sxs-lookup"><span data-stu-id="7b586-191">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7b586-192">В следующем примере определяется кисть радиального градиента, которая будет использоваться в качестве маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-192">The next example defines the radial gradient brush that will be used as the opacity mask.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





<span data-ttu-id="7b586-193">В окончательном примере кода используется [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ прадиалфадефловерсбитмапбруш*) и маска непрозрачности (*m \_ прадиалградиентбруш*) для заполнения [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ пректжео*).</span><span class="sxs-lookup"><span data-stu-id="7b586-193">The final code example uses the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pRadialFadeFlowersBitmapBrush*) and the opacity mask (*m\_pRadialGradientBrush*) to fill an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*).</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



<span data-ttu-id="7b586-194">В этом примере код пропущен.</span><span class="sxs-lookup"><span data-stu-id="7b586-194">Code has been omitted from this example.</span></span>

## <a name="apply-an-opacity-mask-to-a-layer"></a><span data-ttu-id="7b586-195">Применение маски непрозрачности к слою</span><span class="sxs-lookup"><span data-stu-id="7b586-195">Apply an Opacity Mask to a Layer</span></span>

<span data-ttu-id="7b586-196">При вызове [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) для отправки [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) на целевой объект прорисовки можно использовать структуру [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , чтобы применить кисть в качестве маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-196">When you call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) to push an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) onto an render target, you can use the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to apply a brush as an opacity mask.</span></span> <span data-ttu-id="7b586-197">В следующем примере кода используется [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) в качестве маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="7b586-197">The following code example uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) as an opacity mask.</span></span>


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



<span data-ttu-id="7b586-198">Дополнительные сведения об использовании слоев см. в разделе [Общие сведения о слоях](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7b586-198">For more information about using layers, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b586-199">См. также</span><span class="sxs-lookup"><span data-stu-id="7b586-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b586-200">Обзор кистей</span><span class="sxs-lookup"><span data-stu-id="7b586-200">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="7b586-201">Общие сведения о слоях</span><span class="sxs-lookup"><span data-stu-id="7b586-201">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

 

 