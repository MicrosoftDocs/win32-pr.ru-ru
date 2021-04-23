---
description: Режим интерполяции объекта Graphics влияет на способ масштабирования изображений Windows GDI+ (растяжения и сжатие).
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Использование режима интерполяции для управления качеством изображения во время масштабирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984425"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a><span data-ttu-id="e068d-103">Использование режима интерполяции для управления качеством изображения во время масштабирования</span><span class="sxs-lookup"><span data-stu-id="e068d-103">Using Interpolation Mode to Control Image Quality During Scaling</span></span>

<span data-ttu-id="e068d-104">Режим интерполяции объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) влияет на способ масштабирования изображений Windows GDI+ (растяжения и сжатие).</span><span class="sxs-lookup"><span data-stu-id="e068d-104">The interpolation mode of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object influences the way Windows GDI+ scales (stretches and shrinks) images.</span></span> <span data-ttu-id="e068d-105">Перечисление [**интерполатионмоде**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) в гдиплусенумс. h определяет несколько режимов интерполяции, некоторые из которых показаны в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="e068d-105">The [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration in Gdiplusenums.h defines several interpolation modes, some of which are shown in the following list:</span></span>

-   <span data-ttu-id="e068d-106">интерполатионмоденеарестнеигхбор</span><span class="sxs-lookup"><span data-stu-id="e068d-106">InterpolationModeNearestNeighbor</span></span>
-   <span data-ttu-id="e068d-107">интерполатионмодебилинеар</span><span class="sxs-lookup"><span data-stu-id="e068d-107">InterpolationModeBilinear</span></span>
-   <span data-ttu-id="e068d-108">интерполатионмодехигхкуалитибилинеар</span><span class="sxs-lookup"><span data-stu-id="e068d-108">InterpolationModeHighQualityBilinear</span></span>
-   <span data-ttu-id="e068d-109">интерполатионмодебикубик</span><span class="sxs-lookup"><span data-stu-id="e068d-109">InterpolationModeBicubic</span></span>
-   <span data-ttu-id="e068d-110">интерполатионмодехигхкуалитибикубик</span><span class="sxs-lookup"><span data-stu-id="e068d-110">InterpolationModeHighQualityBicubic</span></span>

<span data-ttu-id="e068d-111">Чтобы растянуть изображение, каждый пиксель в исходном изображении должен быть сопоставлен с группой пикселей в увеличенном изображении.</span><span class="sxs-lookup"><span data-stu-id="e068d-111">To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image.</span></span> <span data-ttu-id="e068d-112">Чтобы сжать изображение, группы пикселей в исходном изображении должны быть сопоставлены с отдельными пикселями в меньшем изображении.</span><span class="sxs-lookup"><span data-stu-id="e068d-112">To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image.</span></span> <span data-ttu-id="e068d-113">Эффективность алгоритмов, выполняющих эти сопоставления, определяет качество масштабируемого изображения.</span><span class="sxs-lookup"><span data-stu-id="e068d-113">The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image.</span></span> <span data-ttu-id="e068d-114">Алгоритмы, создающие масштабируемые изображения высокого качества, обычно занимают больше времени на обработку.</span><span class="sxs-lookup"><span data-stu-id="e068d-114">Algorithms that produce higher-quality scaled images tend to require more processing time.</span></span> <span data-ttu-id="e068d-115">В приведенном выше списке Интерполатионмоденеарестнеигхбор — это режим самого низкого качества, а Интерполатионмодехигхкуалитибикубик — режим самого высокого качества.</span><span class="sxs-lookup"><span data-stu-id="e068d-115">In the preceding list, InterpolationModeNearestNeighbor is the lowest-quality mode and InterpolationModeHighQualityBicubic is the highest-quality mode.</span></span>

<span data-ttu-id="e068d-116">Чтобы задать режим интерполяции, передайте один из членов перечисления [**интерполатионмоде**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) методу **сетинтерполатионмоде** объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="e068d-116">To set the interpolation mode, pass one of the members of the [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) enumeration to the **SetInterpolationMode** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="e068d-117">В следующем примере изображение рисуется, а затем сжимается с помощью трех различных режимов интерполяции:</span><span class="sxs-lookup"><span data-stu-id="e068d-117">The following example draws an image and then shrinks the image with three different interpolation modes:</span></span>


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



<span data-ttu-id="e068d-118">На следующем рисунке показано исходное изображение и три изображения меньшего размера.</span><span class="sxs-lookup"><span data-stu-id="e068d-118">The following illustration shows the original image and the three smaller images.</span></span>

![Иллюстрация с большим исходным изображением и тремя мелкими изображениями разного качества](images/grapes1.png)

 

 



