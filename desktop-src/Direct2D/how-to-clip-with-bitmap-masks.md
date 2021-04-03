---
title: Использование точечного рисунка в качестве маски непрозрачности
description: Показывает, как обрезать область с растровыми масками.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987754"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a><span data-ttu-id="30481-103">Использование точечного рисунка в качестве маски непрозрачности</span><span class="sxs-lookup"><span data-stu-id="30481-103">How to Use a Bitmap as an Opacity Mask</span></span>

<span data-ttu-id="30481-104">В этом разделе описывается использование точечного рисунка в качестве маски опакти путем вызова метода [**ID2D1Factory:: филлопаЦитимаск**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) .</span><span class="sxs-lookup"><span data-stu-id="30481-104">This topic describes how to use a bitmap as an opacty mask by calling the [**ID2D1Factory::FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) method.</span></span> <span data-ttu-id="30481-105">Маска непрозрачности — это битовая карта, которая предоставляет сведения о покрытии, представленные альфа-каналом, который управляет прозрачностью отображаемого содержимого.</span><span class="sxs-lookup"><span data-stu-id="30481-105">The opacity mask is a bitmap that supplies the coverage information that is represented by the alpha channel, which controls the transparency of the content that is rendered.</span></span> <span data-ttu-id="30481-106">Этот подход более эффективен, чем использование слоев с маской непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="30481-106">This approach is more efficient than using layers with an opacity mask.</span></span> <span data-ttu-id="30481-107">Дополнительные сведения см. в разделе [Общие сведения о слоях](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="30481-107">For more information, see [Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="30481-108">**Обрезка области**</span><span class="sxs-lookup"><span data-stu-id="30481-108">**To clip a region**</span></span>

1.  <span data-ttu-id="30481-109">Загрузка исходного растрового изображения из ресурса.</span><span class="sxs-lookup"><span data-stu-id="30481-109">Load the original bitmap from a resource.</span></span> <span data-ttu-id="30481-110">Сведения о загрузке точечного рисунка см. в разделе [Загрузка растрового изображения из ресурса](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="30481-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="30481-111">Загрузка маски точечного рисунка из ресурса.</span><span class="sxs-lookup"><span data-stu-id="30481-111">Load the bitmap mask from a resource.</span></span>
3.  <span data-ttu-id="30481-112">Создайте растровую кисть с исходным точечным рисунком.</span><span class="sxs-lookup"><span data-stu-id="30481-112">Create a bitmap brush with the original bitmap.</span></span> <span data-ttu-id="30481-113">Сведения о том, как создать растровую кисть, см. в разделе [Создание растровой кисти](how-to-create-a-bitmap-brush.md).</span><span class="sxs-lookup"><span data-stu-id="30481-113">For information on how to create a bitmap brush, see [How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).</span></span>
4.  <span data-ttu-id="30481-114">Вызовите [**ID2D1Factory:: сетантиалиасмоде**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) , чтобы установить режим сглаживания для целевого объекта прорисовки в \_ режим сглаживания D2D1, \_ \_ псевдоним для [**ID2D1Factory:: филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) для работы.</span><span class="sxs-lookup"><span data-stu-id="30481-114">Call [**ID2D1Factory::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set antialias mode on the render target to D2D1\_ANTIALIAS\_MODE\_ALIASED for [**ID2D1Factory::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) to work.</span></span>
5.  <span data-ttu-id="30481-115">Вызовите [**филлопаЦитимаск**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) , используя битовую маску и растровую кисть на целевом объекте прорисовки для заполнения клипа.</span><span class="sxs-lookup"><span data-stu-id="30481-115">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) with the bitmap mask and the bitmap brush on the render target to fill the clip.</span></span>

<span data-ttu-id="30481-116">На следующем рисунке показана исходная битовая карта слева, битовая маска в центре и битовая карта, обрезанная до маски справа.</span><span class="sxs-lookup"><span data-stu-id="30481-116">The following illustration shows the original bitmap on the left, the bitmap mask in the center, and the bitmap clipped to the mask on the right.</span></span>

![Иллюстрация точечного рисунка Голдфиш, маски в форме рыбы, созданной из растрового изображения, и итогового точечного рисунка в форме рыбы после маски](images/cliparegion-opacitymask.png)

<span data-ttu-id="30481-118">В следующем коде показано, как обрезать область с маской, показанной на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="30481-118">The following code shows how to clip the region with the mask shown in the preceding illustration.</span></span> <span data-ttu-id="30481-119">Сначала загружается исходное растровое изображение и битовая маска.</span><span class="sxs-lookup"><span data-stu-id="30481-119">It first loads the original bitmap and the bitmap mask.</span></span> <span data-ttu-id="30481-120">А затем создает растровую кисть с исходным точечным рисунком.</span><span class="sxs-lookup"><span data-stu-id="30481-120">And then creates a bitmap brush with the original bitmap.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



<span data-ttu-id="30481-121">Затем он вызывает [**сетантиалиасмоде**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) для установки режима сглаживания.</span><span class="sxs-lookup"><span data-stu-id="30481-121">It then calls [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set the antialias mode.</span></span> <span data-ttu-id="30481-122">Вызовите [**филлопаЦитимаск**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) , чтобы использовать битовую маску для обрезки исходного точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="30481-122">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) to use a bitmap mask to clip the original bitmap.</span></span>


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



<span data-ttu-id="30481-123">Дополнительные сведения о масках непрозрачности см. в статье [Общие сведения о масках непрозрачности](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="30481-123">For more information about opacity masks, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30481-124">См. также</span><span class="sxs-lookup"><span data-stu-id="30481-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30481-125">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="30481-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 