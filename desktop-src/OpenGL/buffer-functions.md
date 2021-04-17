---
title: Функции буфера
description: Чтобы скопировать содержимое буфера, который находится вне экрана, в буфер экрана, вызовите Свапбуфферс.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- Функции ВГЛ, buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105674519"
---
# <a name="buffer-functions"></a><span data-ttu-id="a2596-104">Функции буфера</span><span class="sxs-lookup"><span data-stu-id="a2596-104">Buffer Functions</span></span>

<span data-ttu-id="a2596-105">Чтобы скопировать содержимое буфера, который находится вне экрана, в буфер экрана, вызовите [**свапбуфферс**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="a2596-105">To copy the contents of an off-screen buffer to an on-screen buffer, call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="a2596-106">Функция **свапбуфферс** принимает Handle в контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="a2596-106">The **SwapBuffers** function takes a handle to a device context.</span></span> <span data-ttu-id="a2596-107">Текущий формат пикселей для указанного контекста устройства должен включать задний буфер.</span><span class="sxs-lookup"><span data-stu-id="a2596-107">The current pixel format for the specified device context must include a back buffer.</span></span> <span data-ttu-id="a2596-108">По умолчанию задний буфер находится за пределами экрана, а передний буфер — на экране.</span><span class="sxs-lookup"><span data-stu-id="a2596-108">By default, the back buffer is off-screen, and the front buffer is on-screen.</span></span>

> [!Note]  
> <span data-ttu-id="a2596-109">Функция **свапбуфферс** фактически не меняет местами содержимое двух буферов, а копирует содержимое одного буфера в другой.</span><span class="sxs-lookup"><span data-stu-id="a2596-109">The **SwapBuffers** function does not really swap the contents of the two buffers, but rather copies the contents of one buffer to another.</span></span> <span data-ttu-id="a2596-110">Содержимое буфера вне экрана не определено после вызова **свапбуфферс**.</span><span class="sxs-lookup"><span data-stu-id="a2596-110">The contents of the off-screen buffer are undefined after a call to **SwapBuffers**.</span></span> <span data-ttu-id="a2596-111">Таким образом, результат двух последовательных вызовов **свапбуфферс** не определен.</span><span class="sxs-lookup"><span data-stu-id="a2596-111">Thus, the result of two consecutive calls to **SwapBuffers** is undefined.</span></span>

 

<span data-ttu-id="a2596-112">На следующем рисунке показано, как копируются содержимое буферов при вызове **свапбуфферс**.</span><span class="sxs-lookup"><span data-stu-id="a2596-112">The following illustration shows how the contents of the buffers are copied when calling **SwapBuffers**.</span></span>

![Схема, показывающая неопределенные результаты последовательных вызовов функции Свапбуфферс.](images/opengl00.png)

<span data-ttu-id="a2596-114">Несколько основных функций OpenGL Core также управляют буферами.</span><span class="sxs-lookup"><span data-stu-id="a2596-114">Several OpenGL core functions also manage buffers.</span></span> <span data-ttu-id="a2596-115">Функция [**глдравбуффер**](gldrawbuffer.md) наиболее важна для двойной буферизации; Он указывает буфера кадров или буферы, в которые рисуется OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a2596-115">The [**glDrawBuffer**](gldrawbuffer.md) function is the one most relevant to double buffering; it specifies the framebuffer or buffers that OpenGL draws into.</span></span>

<span data-ttu-id="a2596-116">Следующие функции также влияют на буферы:</span><span class="sxs-lookup"><span data-stu-id="a2596-116">The following functions also affect buffers:</span></span>

-   [<span data-ttu-id="a2596-117">**глреадбуффер**</span><span class="sxs-lookup"><span data-stu-id="a2596-117">**glReadBuffer**</span></span>](glreadbuffer.md)
-   [<span data-ttu-id="a2596-118">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="a2596-118">**glReadPixels**</span></span>](glreadpixels.md)
-   [<span data-ttu-id="a2596-119">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="a2596-119">**glCopyPixels**</span></span>](glcopypixels.md)
-   [<span data-ttu-id="a2596-120">**глаккум**</span><span class="sxs-lookup"><span data-stu-id="a2596-120">**glAccum**</span></span>](glaccum.md)
-   [<span data-ttu-id="a2596-121">**глколормаск**</span><span class="sxs-lookup"><span data-stu-id="a2596-121">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="a2596-122">**глдепсмаск**</span><span class="sxs-lookup"><span data-stu-id="a2596-122">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="a2596-123">**глиндексмаск**</span><span class="sxs-lookup"><span data-stu-id="a2596-123">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="a2596-124">**глстенЦилмаск**</span><span class="sxs-lookup"><span data-stu-id="a2596-124">**glStencilMask**</span></span>](glstencilmask.md)
-   [<span data-ttu-id="a2596-125">**глклеараккум**</span><span class="sxs-lookup"><span data-stu-id="a2596-125">**glClearAccum**</span></span>](glclearaccum.md)
-   [<span data-ttu-id="a2596-126">**глклеарколор**</span><span class="sxs-lookup"><span data-stu-id="a2596-126">**glClearColor**</span></span>](glclearcolor.md)
-   [<span data-ttu-id="a2596-127">**глклеардепс**</span><span class="sxs-lookup"><span data-stu-id="a2596-127">**glClearDepth**</span></span>](glcleardepth.md)
-   [<span data-ttu-id="a2596-128">**глклеариндекс**</span><span class="sxs-lookup"><span data-stu-id="a2596-128">**glClearIndex**</span></span>](glclearindex.md)
-   [<span data-ttu-id="a2596-129">**глклеарстенЦил**</span><span class="sxs-lookup"><span data-stu-id="a2596-129">**glClearStencil**</span></span>](glclearstencil.md)

 

 




