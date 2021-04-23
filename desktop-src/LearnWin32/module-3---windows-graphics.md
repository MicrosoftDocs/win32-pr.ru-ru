---
title: Модуль 3. Графика Windows
description: В модуле 1 этой серии показано, как создать пустое окно.
ms.assetid: 02416d36-519e-49bd-8a52-bd3afde2be34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbe0e7afe882180a056f4c77d72de16df0ef943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067576"
---
# <a name="module-3-windows-graphics"></a><span data-ttu-id="1e8ec-104">Модуль 3.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-104">Module 3.</span></span> <span data-ttu-id="1e8ec-105">Графика Windows</span><span class="sxs-lookup"><span data-stu-id="1e8ec-105">Windows Graphics</span></span>

<span data-ttu-id="1e8ec-106">В [модуле 1](your-first-windows-program.md) этой серии показано, как создать пустое окно.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-106">[Module 1](your-first-windows-program.md) of this series showed how to create a blank window.</span></span> <span data-ttu-id="1e8ec-107">[Модуль 2](module-2--using-com-in-your-windows-program.md) занял небольшое изучение модели COM, что является основой для многих современных API Windows.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-107">[Module 2](module-2--using-com-in-your-windows-program.md) took a slight detour through the Component Object Model (COM), which is the foundation for many of the modern Windows APIs.</span></span> <span data-ttu-id="1e8ec-108">Теперь пришло время добавить графику в пустое окно, созданное в модуле 1.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-108">Now it is time to add graphics to the blank window that we created in Module 1.</span></span>

<span data-ttu-id="1e8ec-109">Этот модуль начинается с высокоуровневого обзора архитектуры графики Windows.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-109">This module starts with a high-level overview of the Windows graphics architecture.</span></span> <span data-ttu-id="1e8ec-110">Затем мы рассмотрим Direct2D — мощный графический API, который появился в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-110">We then look at Direct2D, a powerful graphics API that was introduced in Windows 7.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1e8ec-111">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="1e8ec-111">In this section</span></span>

-   [<span data-ttu-id="1e8ec-112">Обзор архитектуры графики Windows</span><span class="sxs-lookup"><span data-stu-id="1e8ec-112">Overview of the Windows Graphics Architecture</span></span>](overview-of-the-windows-graphics-architecture.md)
-   [<span data-ttu-id="1e8ec-113">диспетчер окон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="1e8ec-113">The Desktop Window Manager</span></span>](the-desktop-window-manager.md)
-   [<span data-ttu-id="1e8ec-114">Режим сохраняемости и режим интерпретации</span><span class="sxs-lookup"><span data-stu-id="1e8ec-114">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)
-   [<span data-ttu-id="1e8ec-115">Первая программа Direct2D</span><span class="sxs-lookup"><span data-stu-id="1e8ec-115">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)
-   [<span data-ttu-id="1e8ec-116">Отрисовка целевых объектов, устройств и ресурсов</span><span class="sxs-lookup"><span data-stu-id="1e8ec-116">Render Targets, Devices, and Resources</span></span>](render-targets--devices--and-resources.md)
-   [<span data-ttu-id="1e8ec-117">Рисование с использованием Direct2D</span><span class="sxs-lookup"><span data-stu-id="1e8ec-117">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)
-   [<span data-ttu-id="1e8ec-118">DPI и Device-Independent пикселей</span><span class="sxs-lookup"><span data-stu-id="1e8ec-118">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)
-   [<span data-ttu-id="1e8ec-119">Использование цвета в Direct2D</span><span class="sxs-lookup"><span data-stu-id="1e8ec-119">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)
-   [<span data-ttu-id="1e8ec-120">Применение преобразований в Direct2D</span><span class="sxs-lookup"><span data-stu-id="1e8ec-120">Applying Transforms in Direct2D</span></span>](applying-transforms-in-direct2d.md)
-   [<span data-ttu-id="1e8ec-121">Приложение. преобразования матрицы</span><span class="sxs-lookup"><span data-stu-id="1e8ec-121">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)

## <a name="related-topics"></a><span data-ttu-id="1e8ec-122">См. также</span><span class="sxs-lookup"><span data-stu-id="1e8ec-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e8ec-123">Знакомство с программой для Windows в C++</span><span class="sxs-lookup"><span data-stu-id="1e8ec-123">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 




