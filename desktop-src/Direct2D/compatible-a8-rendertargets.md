---
title: Общие сведения о совместимых целевых объектах рендеринга A8
description: Описывает основы совместимых целевых объектов рендеринга A8 и предоставляет примеры их использования.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "103988056"
---
# <a name="compatible-a8-render-targets-overview"></a><span data-ttu-id="26910-103">Общие сведения о совместимых целевых объектах рендеринга A8</span><span class="sxs-lookup"><span data-stu-id="26910-103">Compatible A8 render targets overview</span></span>

<span data-ttu-id="26910-104">В этом разделе описаны основы совместимого целевого объекта рендеринга A8 и приведены примеры его использования.</span><span class="sxs-lookup"><span data-stu-id="26910-104">This topic describes the basics of a compatible A8 render target, and provides examples of how to use it.</span></span>

<span data-ttu-id="26910-105">Совместимый целевой объект рендеринга A8 — совместимый целевой объект отрисовки ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)), использующий формат пикселей A8 ( \_ Формат DXGI \_ a8 \_ UNORM).</span><span class="sxs-lookup"><span data-stu-id="26910-105">A compatible A8 render target is a compatible render target ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) that uses an A8 pixel format (DXGI\_FORMAT\_A8\_UNORM).</span></span> <span data-ttu-id="26910-106">Вы можете использовать совместимый целевой объект рендеринга A8, чтобы повысить производительность приложения и обеспечить более плавные переходы во время анимации текста.</span><span class="sxs-lookup"><span data-stu-id="26910-106">You can use a compatible A8 render target to improve the application's performance and provide smoother transitions during text animation.</span></span> <span data-ttu-id="26910-107">Совместимый целевой объект рендеринга A8 полезен при попытке улучшить следующее:</span><span class="sxs-lookup"><span data-stu-id="26910-107">A compatible A8 render target is particular useful when you try to improve the following:</span></span>

-   <span data-ttu-id="26910-108">Частота кадров приложения, которая визуализирует текст или сглаживание с помощью сглаживания, включающее только простые анимации, такие как перевод, вращение, масштабирование или изменение цвета.</span><span class="sxs-lookup"><span data-stu-id="26910-108">The frame rate of the application that renders text or anti-aliased geometry that includes only simple animations, such as translation, rotation, scale, or color changes.</span></span>

-   <span data-ttu-id="26910-109">Непрерывность визуального элемента приложения, которое растягивает и диминшес текст во время анимации.</span><span class="sxs-lookup"><span data-stu-id="26910-109">The visual continuity of the application that stretches and diminshes text during an animation.</span></span>

<span data-ttu-id="26910-110">Чтобы создать совместимый целевой объект рендеринга A8, используйте метод [**ID2D1RenderTarget:: креатекомпатиблерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) вместе с форматом DXGI \_ \_ a8 \_ UNORM пикселей и укажите возвращенный совместимый целевой объект рендеринга.</span><span class="sxs-lookup"><span data-stu-id="26910-110">To create a compatible A8 render target, use the [**ID2D1RenderTarget::CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) method together with the DXGI\_FORMAT\_A8\_UNORM pixel format, and specify a returned compatible render target.</span></span> <span data-ttu-id="26910-111">Дополнительные сведения о форматах пикселей см. в разделе [Поддерживаемые форматы пикселей и альфа-режимы](./supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="26910-111">For more information about pixel formats, see [Supported pixel formats and alpha modes](./supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="26910-112">Например, чтобы эффективно анимировать текст, показанный на следующем снимке экрана, используйте совместимый целевой объект рендеринга A8 для кэширования текста в качестве маски непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="26910-112">For example, to efficiently animate the text that is shown in the following screen shot, use a compatible A8 render target to cache the text as an opacity mask.</span></span> <span data-ttu-id="26910-113">Затем примените преобразования к маске непрозрачности для достижения быстрых результатов отрисовки.</span><span class="sxs-lookup"><span data-stu-id="26910-113">Then, apply transformations to the opacity mask to achieve fast rendering results.</span></span>

![снимок экрана с текстом для анимации](images/a8rendertarget.png)

<span data-ttu-id="26910-115">В следующем примере кода показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="26910-115">The following code shows how to do this.</span></span> <span data-ttu-id="26910-116">Он создает совместимый целевой объект рендеринга A8, извлекает из него битовую карту, а затем визуализирует растровое изображение с помощью [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md).</span><span class="sxs-lookup"><span data-stu-id="26910-116">It creates a compatible A8 render target, retrieves the bitmap from it, and then renders the bitmap by using [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).</span></span>

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a><span data-ttu-id="26910-117">См. также</span><span class="sxs-lookup"><span data-stu-id="26910-117">Related topics</span></span>

[<span data-ttu-id="26910-118">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="26910-118">Direct2D Reference</span></span>](reference.md)