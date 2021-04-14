---
title: Обрезка с помощью Axis-Alignedного прямоугольника
description: Показывает, как обрезать область с помощью прямоугольника с выровняйтем по осям.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104568736"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a><span data-ttu-id="af5b0-103">Обрезка с помощью Axis-Alignedного прямоугольника</span><span class="sxs-lookup"><span data-stu-id="af5b0-103">How to Clip with an Axis-Aligned Clip Rectangle</span></span>

<span data-ttu-id="af5b0-104">В этом разделе описывается, как обрезать изображение с помощью прямоугольника, ориентированного на оси.</span><span class="sxs-lookup"><span data-stu-id="af5b0-104">This topic describes how to clip an image with an axis-aligned clip rectangle.</span></span> <span data-ttu-id="af5b0-105">Этот подход создает только прямоугольные клипы, так как границы содержимого вычисляются по осям прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="af5b0-105">This approach produces only rectangular clips, because the content bounds are aligned to the axis of the rectangle.</span></span> <span data-ttu-id="af5b0-106">Этот подход более эффективен, чем использование слоев с границами содержимого.</span><span class="sxs-lookup"><span data-stu-id="af5b0-106">This approach is more efficient than using layers with the content bounds.</span></span> <span data-ttu-id="af5b0-107">Дополнительные сведения см. в разделе[Общие сведения о слоях](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="af5b0-107">For more information, see[Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="af5b0-108">**Обрезка с помощью прямоугольника обрезки, ориентированного на оси**</span><span class="sxs-lookup"><span data-stu-id="af5b0-108">**To clip with an axis-aligned clip rectangle**</span></span>

1.  <span data-ttu-id="af5b0-109">Загрузка исходного изображения из ресурса.</span><span class="sxs-lookup"><span data-stu-id="af5b0-109">Load the original image from a resource.</span></span> <span data-ttu-id="af5b0-110">Сведения о загрузке точечного рисунка см. в разделе [Загрузка растрового изображения из ресурса](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="af5b0-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="af5b0-111">Вызовите [**ID2D1RenderTarget::P ушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) , чтобы указать прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="af5b0-111">Call [**ID2D1RenderTarget::PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) to specify a rectangle.</span></span> <span data-ttu-id="af5b0-112">Команды отрисовки обрезаются до прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="af5b0-112">The rendering commands are clipped to the rectangle.</span></span>

3.  <span data-ttu-id="af5b0-113">Закрашивание исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="af5b0-113">Paint the original image.</span></span>
4.  <span data-ttu-id="af5b0-114">Вызовите [**ID2D1RenderTarget::P опаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) , чтобы удалить последний обрезанный по оси клип из целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="af5b0-114">Call [**ID2D1RenderTarget::PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the last axis-aligned clip from the render target.</span></span>

<span data-ttu-id="af5b0-115">Например, на следующем рисунке исходное растровое изображение слева составляет 200 \* 130 пикселей.</span><span class="sxs-lookup"><span data-stu-id="af5b0-115">For example, in the following illustration, the original bitmap on the left is 200\*130 pixels.</span></span> <span data-ttu-id="af5b0-116">Точечный рисунок справа является исходным точечным рисунком, обрезанным по оси с выкрашенным по осям прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="af5b0-116">The bitmap on the right is the original bitmap clipped to the axis-aligned clip rectangle.</span></span> <span data-ttu-id="af5b0-117">Размеры (от 20 до 20) до (100, 100).</span><span class="sxs-lookup"><span data-stu-id="af5b0-117">The dimensions are (20, 20) to (100, 100).</span></span>

![Иллюстрация точечного рисунка Голдфиш до и после усечения растрового изображения](images/cliparegion-axisalignedclip.png)

<span data-ttu-id="af5b0-119">Чтобы создать обрезанное изображение, создайте прямоугольную структуру в качестве области обрезки.</span><span class="sxs-lookup"><span data-stu-id="af5b0-119">To create the clipped image, create a rectangle structure as the clipping area.</span></span> <span data-ttu-id="af5b0-120">Вызовите [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) с областью обрезки и закрасьте исходное изображение.</span><span class="sxs-lookup"><span data-stu-id="af5b0-120">Call [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) with the clipping area and paint the original image.</span></span> <span data-ttu-id="af5b0-121">Вызовите [**попаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) , чтобы удалить клип из целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="af5b0-121">Call [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the clip from the render target.</span></span> <span data-ttu-id="af5b0-122">В следующем примере кода показано, как это сделать:</span><span class="sxs-lookup"><span data-stu-id="af5b0-122">The following code shows how to do this.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a><span data-ttu-id="af5b0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="af5b0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af5b0-124">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="af5b0-124">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 