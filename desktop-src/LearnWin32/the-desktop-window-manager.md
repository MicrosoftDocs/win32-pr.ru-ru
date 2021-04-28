---
title: диспетчер окон рабочего стола
description: диспетчер окон рабочего стола
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103902"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="1ad4c-103">диспетчер окон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="1ad4c-103">The Desktop Window Manager</span></span>

<span data-ttu-id="1ad4c-104">До выхода Windows Vista программа Windows будет нарисоваться непосредственно на экране.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="1ad4c-105">Иными словами, программа будет записывать данные непосредственно в буфер памяти, показанный видеоадаптером.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="1ad4c-106">Этот подход может вызвать визуальные артефакты, если окно неправильно перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="1ad4c-107">Например, если пользователь перетаскивает одно окно поверх другого окна, и окно под ним не перерисовывается достаточно быстро, то самое верхнее окно может оставить свой след:</span><span class="sxs-lookup"><span data-stu-id="1ad4c-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![снимок экрана, на котором показаны перерисовки артефактов.](images/graphics04.png)

<span data-ttu-id="1ad4c-109">Эта ошибка возникает из-за того, что Windows Paint работает в той же области памяти.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="1ad4c-110">При перетаскивании окна сверху окно должно быть перерисовано.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="1ad4c-111">Если перерисовка выполняется слишком долго, это приводит к тому, что артефакты показаны на предыдущем изображении.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="1ad4c-112">Windows Vista фундаментально изменила внешний вид Windows, представляя диспетчер окон рабочего стола (DWM).</span><span class="sxs-lookup"><span data-stu-id="1ad4c-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="1ad4c-113">Когда DWM включен, окно больше не рисуется непосредственно в буфере экрана.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="1ad4c-114">Вместо этого каждое окно рисуется в буфере памяти экрана, также называемом заданной *областью*.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="1ad4c-115">Затем DWM перекомбинирует эти поверхности на экран.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-115">The DWM then composites these surfaces to the screen.</span></span>

![Схема, показывающая, как DWM комбинирует Рабочий стол.](images/graphics05.png)

<span data-ttu-id="1ad4c-117">DWM предоставляет несколько преимуществ по сравнению со старой архитектурой графики.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="1ad4c-118">Меньшее количество перерисовок сообщений.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-118">Fewer repaint messages.</span></span> <span data-ttu-id="1ad4c-119">Когда окно ограничено другим окном, это окно не нуждается в перерисовке.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="1ad4c-120">Сокращенные артефакты.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-120">Reduced artifacts.</span></span> <span data-ttu-id="1ad4c-121">Ранее перетаскивание окна может создать визуальные артефакты, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="1ad4c-122">Визуальные эффекты.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-122">Visual effects.</span></span> <span data-ttu-id="1ad4c-123">Так как DWM отвечает за композицию экрана, он может отображать полупрозрачные и размытые области окна.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="1ad4c-124">Автоматическое масштабирование для высокого DPI.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="1ad4c-125">Хотя масштабирование не является идеальным способом для управления высоким разрешением, он является приемлемым вариантом для более старых приложений, которые не предназначены для настройки с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="1ad4c-126">(Мы вернемся к этому разделу позже, в разделе [dpi и Device-Independent пикселей](dpi-and-device-independent-pixels.md).)</span><span class="sxs-lookup"><span data-stu-id="1ad4c-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="1ad4c-127">Альтернативные представления.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-127">Alternative views.</span></span> <span data-ttu-id="1ad4c-128">DWM может использовать поверхностные области различными способами.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="1ad4c-129">Например, DWM — это технология, предназначенная для эргономичного пролистывания окон, эскизов и анимированных переходов.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="1ad4c-130">Однако обратите внимание, что не гарантируется, что DWM будет включен.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="1ad4c-131">Графическая карта может не поддерживать системные требования DWM, и пользователи могут отключить DWM с помощью панели управления " **Свойства системы** ".</span><span class="sxs-lookup"><span data-stu-id="1ad4c-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="1ad4c-132">Это означает, что программа не должна полагаться на поведение DWM в перерисовки.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="1ad4c-133">Протестируйте программу с помощью DWM Disabled, чтобы убедиться, что она правильно перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="1ad4c-134">Следующая</span><span class="sxs-lookup"><span data-stu-id="1ad4c-134">Next</span></span>

[<span data-ttu-id="1ad4c-135">Режим сохраняемости и режим интерпретации</span><span class="sxs-lookup"><span data-stu-id="1ad4c-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




