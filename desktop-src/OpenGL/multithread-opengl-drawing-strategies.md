---
title: Многопотоковые стратегии рисования OpenGL
description: GDI не поддерживает несколько потоков.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL в Windows, многопотоковое Рисование
- многопоточный графический стандарт OpenGL Drawing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329504"
---
# <a name="multithread-opengl-drawing-strategies"></a><span data-ttu-id="64ad2-105">Многопотоковые стратегии рисования OpenGL</span><span class="sxs-lookup"><span data-stu-id="64ad2-105">Multithread OpenGL Drawing Strategies</span></span>

<span data-ttu-id="64ad2-106">GDI не поддерживает несколько потоков.</span><span class="sxs-lookup"><span data-stu-id="64ad2-106">The GDI does not support multiple threads.</span></span> <span data-ttu-id="64ad2-107">Для каждого потока необходимо использовать отдельный контекст устройства и отдельный контекст отрисовки.</span><span class="sxs-lookup"><span data-stu-id="64ad2-107">You must use a distinct device context and a distinct rendering context for each thread.</span></span> <span data-ttu-id="64ad2-108">Это, как правило, ограничивает производительность при использовании нескольких потоков с однопроцессорными системами, работающими с приложениями OpenGL.</span><span class="sxs-lookup"><span data-stu-id="64ad2-108">This tends to limit the performance advantages of using multiple threads with single-processor systems running OpenGL applications.</span></span> <span data-ttu-id="64ad2-109">Однако существуют способы использования потоков с одной системой процессора для значительного повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="64ad2-109">However, there are ways to use threads with a single processor system to greatly increase performance.</span></span> <span data-ttu-id="64ad2-110">Например, можно использовать отдельный поток для передачи вызовов отрисовки OpenGL на выделенное трехмерное оборудование.</span><span class="sxs-lookup"><span data-stu-id="64ad2-110">For example, you can use a separate thread to pass OpenGL rendering calls to dedicated 3-D hardware.</span></span>

<span data-ttu-id="64ad2-111">В системах с симметричной многопроцессорной обработкой (SMP) можно значительно повысить эффективность использования нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="64ad2-111">Symmetric multiprocessing (SMP) systems can greatly benefit from using multiple threads.</span></span> <span data-ttu-id="64ad2-112">Очевидной стратегией является использование отдельного потока для каждого процессора для обработки отрисовки OpenGL в отдельных окнах.</span><span class="sxs-lookup"><span data-stu-id="64ad2-112">An obvious strategy is to use a separate thread for each processor to handle OpenGL rendering in separate windows.</span></span> <span data-ttu-id="64ad2-113">Например, в приложении для имитации полета можно использовать отдельные процессоры и потоки для отображения внешних, задних и боковых представлений.</span><span class="sxs-lookup"><span data-stu-id="64ad2-113">For example, in a flight-simulation application you could use separate processors and threads to render the front, back, and side views.</span></span>

<span data-ttu-id="64ad2-114">Поток может иметь только один текущий активный контекст визуализации.</span><span class="sxs-lookup"><span data-stu-id="64ad2-114">A thread can have only one current, active rendering context.</span></span> <span data-ttu-id="64ad2-115">При использовании нескольких потоков и нескольких контекстов отрисовки необходимо тщательно синхронизировать их использование.</span><span class="sxs-lookup"><span data-stu-id="64ad2-115">When you use multiple threads and multiple rendering contexts, you must be careful to synchronize their use.</span></span> <span data-ttu-id="64ad2-116">Например, используйте один поток только для вызова [**свапбуфферс**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) после завершения рисования всеми потоками.</span><span class="sxs-lookup"><span data-stu-id="64ad2-116">For example, use one thread only to call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) after all threads finish drawing.</span></span>

 

 




