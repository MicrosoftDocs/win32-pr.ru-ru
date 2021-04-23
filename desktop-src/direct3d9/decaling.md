---
description: В приложениях Direct3D пользователи с помощью переводных картинок контролируют, какие пиксели из определенного изображения-примитива рисуются на поверхность однобуферной прорисовки. Приложения применяют переводные картинки к изображениям примитивов для правильной отрисовки многоугольников.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Декалинг (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139570"
---
# <a name="decaling-direct3d-9"></a><span data-ttu-id="3b287-104">Декалинг (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3b287-104">Decaling (Direct3D 9)</span></span>

<span data-ttu-id="3b287-105">В приложениях Direct3D пользователи с помощью переводных картинок контролируют, какие пиксели из определенного изображения-примитива рисуются на поверхность однобуферной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="3b287-105">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="3b287-106">Приложения применяют переводные картинки к изображениям примитивов для правильной отрисовки многоугольников.</span><span class="sxs-lookup"><span data-stu-id="3b287-106">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="3b287-107">Например, следы шин и желтая дорожная разметка должны отображаться непосредственно на поверхности дороги.</span><span class="sxs-lookup"><span data-stu-id="3b287-107">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="3b287-108">Однако значения разметки и дорожной поверхности по оси Z совпадают.</span><span class="sxs-lookup"><span data-stu-id="3b287-108">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="3b287-109">Поэтому велика вероятность нечеткого разделения этих сущностей буфером глубины.</span><span class="sxs-lookup"><span data-stu-id="3b287-109">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="3b287-110">Некоторые пиксели в примитиве заднего вида могут отображаться поверх пикселей в примитиве переднего вида, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="3b287-110">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="3b287-111">В результате изображение может дрожать при смене кадра.</span><span class="sxs-lookup"><span data-stu-id="3b287-111">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="3b287-112">Этот результат называется « *борьба за z»* или « *флиммеринг*».</span><span class="sxs-lookup"><span data-stu-id="3b287-112">This effect is called *z-fighting* or *flimmering*.</span></span>

<span data-ttu-id="3b287-113">Чтобы решить эту проблему, используйте трафарет для маскировки раздела примитива заднего вида, в котором будет отображаться переводная картинка.</span><span class="sxs-lookup"><span data-stu-id="3b287-113">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="3b287-114">Выключите Z-буферизацию и отрисуйте изображение примитива переднего обзора в замаскированной области поверхности однобуферной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="3b287-114">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="3b287-115">Хоть эту проблему и можно решить наложением нескольких текстур, но такой подход ограничит число других спецэффектов в приложении.</span><span class="sxs-lookup"><span data-stu-id="3b287-115">Although multiple texture blending can be used to solve this problem, doing so limits the number of other special effects that your application can produce.</span></span> <span data-ttu-id="3b287-116">Применение буфера трафарета для наложения декалей освобождает этапы наложения текстур для других эффектов.</span><span class="sxs-lookup"><span data-stu-id="3b287-116">Using the stencil buffer to apply decals frees up texture blending stages for other effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b287-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3b287-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b287-118">Методы буфера шаблона</span><span class="sxs-lookup"><span data-stu-id="3b287-118">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



