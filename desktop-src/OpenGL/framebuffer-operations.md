---
title: Операции буфера кадров
description: Чтобы выбрать буфер, в который записываются значения цветов, используйте Глдравбуффер.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Конвейер обработки OpenGL, операции буфера кадров
- фрамебуфферс, операции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531982"
---
# <a name="framebuffer-operations"></a><span data-ttu-id="4380b-105">Операции буфера кадров</span><span class="sxs-lookup"><span data-stu-id="4380b-105">Framebuffer Operations</span></span>

<span data-ttu-id="4380b-106">Чтобы выбрать буфер, в который записываются значения цветов, используйте [**глдравбуффер**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="4380b-106">To select the buffer into which color values are written, use [**glDrawBuffer**](gldrawbuffer.md).</span></span> <span data-ttu-id="4380b-107">Вы используете четыре различные функции для маскирования записи битов на каждый из логических фрамебуфферс после выполнения всех операций по каждому фрагменту:</span><span class="sxs-lookup"><span data-stu-id="4380b-107">You use four different functions to mask the writing of bits to each of the logical framebuffers after all per-fragment operations have been performed:</span></span>

-   [<span data-ttu-id="4380b-108">**глиндексмаск**</span><span class="sxs-lookup"><span data-stu-id="4380b-108">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="4380b-109">**глколормаск**</span><span class="sxs-lookup"><span data-stu-id="4380b-109">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="4380b-110">**глдепсмаск**</span><span class="sxs-lookup"><span data-stu-id="4380b-110">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="4380b-111">**глстенЦилмаск**</span><span class="sxs-lookup"><span data-stu-id="4380b-111">**glStencilMask**</span></span>](glstencilmask.md)

<span data-ttu-id="4380b-112">Функция [**Глаккум**](glaccum.md) управляет операцией буфера накопления.</span><span class="sxs-lookup"><span data-stu-id="4380b-112">The [**glAccum**](glaccum.md) function controls the operation of the accumulation buffer.</span></span> <span data-ttu-id="4380b-113">Наконец, [**глклеар**](glclear.md) устанавливает каждый пиксель в заданном подмножестве буферов в значение, указанное в [**глклеарколор**](glclearcolor.md), [**глклеариндекс**](glclearindex.md), [**глклеардепс**](glcleardepth.md), [**глклеарстенЦил**](glclearstencil.md)или [**глклеараккум**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="4380b-113">Finally, [**glClear**](glclear.md) sets every pixel in a specified subset of the buffers to the value specified with [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), or [**glClearAccum**](glclearaccum.md).</span></span>

 

 




