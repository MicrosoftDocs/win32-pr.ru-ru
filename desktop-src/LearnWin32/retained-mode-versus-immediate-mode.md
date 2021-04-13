---
title: Режим сохраняемости и режим интерпретации
description: Интерфейсы API графики можно разделить на API-интерфейсы с сохраняемым режимом и API-интерфейсы немедленного режима.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104564563"
---
# <a name="retained-mode-versus-immediate-mode"></a><span data-ttu-id="cf083-103">Режим сохраняемости и режим интерпретации</span><span class="sxs-lookup"><span data-stu-id="cf083-103">Retained Mode Versus Immediate Mode</span></span>

<span data-ttu-id="cf083-104">Интерфейсы API графики можно разделить на API *-интерфейсы с сохраняемым режимом* и API *-интерфейсы немедленного режима* .</span><span class="sxs-lookup"><span data-stu-id="cf083-104">Graphics APIs can be divided into *retained-mode* APIs and *immediate-mode* APIs.</span></span> <span data-ttu-id="cf083-105">Direct2D — это API немедленного режима.</span><span class="sxs-lookup"><span data-stu-id="cf083-105">Direct2D is an immediate-mode API.</span></span> <span data-ttu-id="cf083-106">Windows Presentation Foundation (WPF) — это пример API-интерфейса с сохраняемым режимом.</span><span class="sxs-lookup"><span data-stu-id="cf083-106">Windows Presentation Foundation (WPF) is an example of a retained-mode API.</span></span>

<span data-ttu-id="cf083-107">API-интерфейс с сохраняемым режимом является декларативным.</span><span class="sxs-lookup"><span data-stu-id="cf083-107">A retained-mode API is declarative.</span></span> <span data-ttu-id="cf083-108">Приложение конструирует сцену на основе графических примитивов, таких как фигуры и линии.</span><span class="sxs-lookup"><span data-stu-id="cf083-108">The application constructs a scene from graphics primitives, such as shapes and lines.</span></span> <span data-ttu-id="cf083-109">Библиотека графики хранит модель сцены в памяти.</span><span class="sxs-lookup"><span data-stu-id="cf083-109">The graphics library stores a model of the scene in memory.</span></span> <span data-ttu-id="cf083-110">Чтобы нарисовать кадр, Библиотека графики преобразует сцену в набор команд рисования.</span><span class="sxs-lookup"><span data-stu-id="cf083-110">To draw a frame, the graphics library transforms the scene into a set of drawing commands.</span></span> <span data-ttu-id="cf083-111">Между кадрами графическая библиотека сохраняет сцену в памяти.</span><span class="sxs-lookup"><span data-stu-id="cf083-111">Between frames, the graphics library keeps the scene in memory.</span></span> <span data-ttu-id="cf083-112">Чтобы изменить отображаемый объект, приложение выдает команду для обновления сцены, например для добавления или удаления фигуры.</span><span class="sxs-lookup"><span data-stu-id="cf083-112">To change what is rendered, the application issues a command to update the scene—for example, to add or remove a shape.</span></span> <span data-ttu-id="cf083-113">Затем библиотека отвечает за перерисовку сцены.</span><span class="sxs-lookup"><span data-stu-id="cf083-113">The library is then responsible for redrawing the scene.</span></span>

![Диаграмма, на которой показаны графические изображения в постоянном режиме.](images/graphics06.png)

<span data-ttu-id="cf083-115">API немедленного режима — это процедура.</span><span class="sxs-lookup"><span data-stu-id="cf083-115">An immediate-mode API is procedural.</span></span> <span data-ttu-id="cf083-116">Каждый раз при прорисовке нового кадра приложение непосредственно выдает команды рисования.</span><span class="sxs-lookup"><span data-stu-id="cf083-116">Each time a new frame is drawn, the application directly issues the drawing commands.</span></span> <span data-ttu-id="cf083-117">Библиотека графики не сохраняет модель сцены между кадрами.</span><span class="sxs-lookup"><span data-stu-id="cf083-117">The graphics library does not store a scene model between frames.</span></span> <span data-ttu-id="cf083-118">Вместо этого приложение отслеживает сцену.</span><span class="sxs-lookup"><span data-stu-id="cf083-118">Instead, the application keeps track of the scene.</span></span>

![Диаграмма, отображающая графические изображения в режиме интерпретации.](images/graphics07.png)

<span data-ttu-id="cf083-120">API-интерфейсы с сохранением режима могут быть проще в использовании, так как API выполняет больше работы, например инициализацию, Обслуживание состояния и очистку.</span><span class="sxs-lookup"><span data-stu-id="cf083-120">Retained-mode APIs can be simpler to use, because the API does more of the work for you, such as initialization, state maintenance, and cleanup.</span></span> <span data-ttu-id="cf083-121">С другой стороны, они часто менее гибкие, так как API накладывает собственную модель сцены.</span><span class="sxs-lookup"><span data-stu-id="cf083-121">On the other hand, they are often less flexible, because the API imposes its own scene model.</span></span> <span data-ttu-id="cf083-122">Кроме того, API-интерфейс со строгим режимом может иметь более высокие требования к памяти, поскольку ему необходимо предоставить модель сцены общего назначения.</span><span class="sxs-lookup"><span data-stu-id="cf083-122">Also, a retained-mode API can have higher memory requirements, because it needs to provide a general-purpose scene model.</span></span> <span data-ttu-id="cf083-123">С помощью API немедленного режима можно реализовать целевые оптимизации.</span><span class="sxs-lookup"><span data-stu-id="cf083-123">With an immediate-mode API, you can implement targeted optimizations.</span></span>

## <a name="next"></a><span data-ttu-id="cf083-124">Следующая</span><span class="sxs-lookup"><span data-stu-id="cf083-124">Next</span></span>

[<span data-ttu-id="cf083-125">Первая программа Direct2D</span><span class="sxs-lookup"><span data-stu-id="cf083-125">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)

 

 




