---
title: Components
description: Компоненты
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL в Windows, компоненты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672121"
---
# <a name="components"></a><span data-ttu-id="f3f29-104">Компоненты</span><span class="sxs-lookup"><span data-stu-id="f3f29-104">Components</span></span>

<span data-ttu-id="f3f29-105">Реализация OpenGL в Windows в корпорации Майкрософт включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="f3f29-105">Microsoft's implementation of OpenGL in Windows includes the following components:</span></span>

-   <span data-ttu-id="f3f29-106">Полный набор текущих команд OpenGL</span><span class="sxs-lookup"><span data-stu-id="f3f29-106">The full set of current OpenGL commands</span></span>

    <span data-ttu-id="f3f29-107">OpenGL содержит библиотеку основных функций для трехмерных графических операций.</span><span class="sxs-lookup"><span data-stu-id="f3f29-107">OpenGL contains a library of core functions for 3-D graphics operations.</span></span> <span data-ttu-id="f3f29-108">Эти основные функции используются для управления описанием фигур объекта, преобразования матрицы, освещения, выделения цветом, текстуры, обрезки, точечных рисунков, тумана и сглаживания.</span><span class="sxs-lookup"><span data-stu-id="f3f29-108">These basic functions are used to manage object shape description, matrix transformation, lighting, coloring, texture, clipping, bitmaps, fog, and antialiasing.</span></span> <span data-ttu-id="f3f29-109">Имена этих основных функций имеют префикс "GL".</span><span class="sxs-lookup"><span data-stu-id="f3f29-109">The names for these core functions have a "gl" prefix.</span></span>

    <span data-ttu-id="f3f29-110">Многие команды OpenGL имеют несколько вариантов, которые отличаются числом и типом их параметров.</span><span class="sxs-lookup"><span data-stu-id="f3f29-110">Many of the OpenGL commands have several variants, which differ in the number and type of their parameters.</span></span> <span data-ttu-id="f3f29-111">Подсчета всех вариантов, имеется более 300 команд OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f3f29-111">Counting all the variants, there are more than 300 OpenGL commands.</span></span>

-   <span data-ttu-id="f3f29-112">Библиотека служебной программы OpenGL (GLU)</span><span class="sxs-lookup"><span data-stu-id="f3f29-112">The OpenGL Utility (GLU) library</span></span>

    <span data-ttu-id="f3f29-113">Эта библиотека вспомогательных функций дополняет основные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f3f29-113">This library of auxiliary functions complements the core OpenGL functions.</span></span> <span data-ttu-id="f3f29-114">Команды управляют поддержкой текстур, преобразования координат, тесселяции многоугольников, отрисовки шарик, цилиндров и дисков, НУРБС (неравномерные рациональные B-кривые) кривые и поверхности, а также обработку ошибок.</span><span class="sxs-lookup"><span data-stu-id="f3f29-114">The commands manage texture support, coordinate transformation, polygon tessellation, rendering spheres, cylinders and disks, NURBS (Non-Uniform Rational B-Spline) curves and surfaces, and error handling.</span></span>

-   <span data-ttu-id="f3f29-115">Вспомогательная библиотека по программированию OpenGL</span><span class="sxs-lookup"><span data-stu-id="f3f29-115">The OpenGL Programming Guide Auxiliary library</span></span>

    <span data-ttu-id="f3f29-116">Это простая, независимая от платформы библиотека функций для управления окнами, обработки событий ввода, рисования классических трехмерных объектов, управления фоновым процессом и выполнения программы.</span><span class="sxs-lookup"><span data-stu-id="f3f29-116">This is a simple, platform-independent library of functions for managing windows, handling input events, drawing classic 3-D objects, managing a background process, and running a program.</span></span> <span data-ttu-id="f3f29-117">Управление окнами и подпрограммы ввода обеспечивают базовый уровень функциональности, с помощью которого можно быстро приступить к программированию на OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f3f29-117">The window management and input routines provide a base level of functionality with which you can quickly get started programming in OpenGL.</span></span>

    <span data-ttu-id="f3f29-118">Однако не используйте их в рабочем приложении.</span><span class="sxs-lookup"><span data-stu-id="f3f29-118">Do not use them, however, in a production application.</span></span> <span data-ttu-id="f3f29-119">Ниже приведены некоторые причины этого предупреждения.</span><span class="sxs-lookup"><span data-stu-id="f3f29-119">Here are some reasons for this warning:</span></span>

    -   <span data-ttu-id="f3f29-120">Цикл обработки сообщений находится в коде библиотеки.</span><span class="sxs-lookup"><span data-stu-id="f3f29-120">The message loop is in the library code.</span></span>
    -   <span data-ttu-id="f3f29-121">Невозможно добавить обработчики для дополнительных \* сообщений WM.</span><span class="sxs-lookup"><span data-stu-id="f3f29-121">There is no way to add handlers for additional WM\* messages.</span></span>
    -   <span data-ttu-id="f3f29-122">Для логических палитр существует очень малая поддержка.</span><span class="sxs-lookup"><span data-stu-id="f3f29-122">There is very little support for logical palettes.</span></span>

    <span data-ttu-id="f3f29-123">Библиотека описана и используется в *справочном разделе по программированию OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="f3f29-123">The library is described and used in the *OpenGL Programming Guide*.</span></span>

-   <span data-ttu-id="f3f29-124">Функции ВГЛ</span><span class="sxs-lookup"><span data-stu-id="f3f29-124">The WGL functions</span></span>

    <span data-ttu-id="f3f29-125">Этот набор функций подключает OpenGL к системе окон Windows.</span><span class="sxs-lookup"><span data-stu-id="f3f29-125">This set of functions connects OpenGL to the Windows windowing system.</span></span> <span data-ttu-id="f3f29-126">Функции управляют контекстами отрисовки, списками отображения, функциями расширения и точечными рисунками шрифтов.</span><span class="sxs-lookup"><span data-stu-id="f3f29-126">The functions manage rendering contexts, display lists, extension functions, and font bitmaps.</span></span> <span data-ttu-id="f3f29-127">Функции ВГЛ аналогичны расширениям ГЛКС, которые подключают OpenGL к системе Window X.</span><span class="sxs-lookup"><span data-stu-id="f3f29-127">The WGL functions are analogous to the GLX extensions that connect OpenGL to the X Window System.</span></span> <span data-ttu-id="f3f29-128">Имена этих функций имеют префикс "вгл".</span><span class="sxs-lookup"><span data-stu-id="f3f29-128">The names for these functions have a "wgl" prefix.</span></span>

-   <span data-ttu-id="f3f29-129">Новые функции Windows для форматов пикселей и двойной буферизации</span><span class="sxs-lookup"><span data-stu-id="f3f29-129">New Windows functions for pixel formats and double buffering</span></span>

    <span data-ttu-id="f3f29-130">Эти функции поддерживают форматы пикселей для каждого окна и двойную буферизацию (для плавного изменения изображения) Windows.</span><span class="sxs-lookup"><span data-stu-id="f3f29-130">These functions support per-window pixel formats and double buffering (for smooth image changes) of windows.</span></span> <span data-ttu-id="f3f29-131">Эти новые функции применяются только к графическим окнам OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f3f29-131">These new functions apply only to OpenGL graphics windows.</span></span>

 

 




