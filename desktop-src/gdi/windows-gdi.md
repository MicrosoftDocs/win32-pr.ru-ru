---
description: Интерфейс графических устройств (GDI) Microsoft Windows позволяет приложениям использовать графику и форматированный текст как на экране видео, так и на принтере.
ms.assetid: b58ab70a-2071-4264-9d20-c0b0aaf8dc5c
title: Windows GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5fc6ba9f4eb99786b21daeff2e1c48b9ce09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985340"
---
# <a name="windows-gdi"></a><span data-ttu-id="1d0a2-103">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="1d0a2-103">Windows GDI</span></span>

## <a name="purpose"></a><span data-ttu-id="1d0a2-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="1d0a2-104">Purpose</span></span>

<span data-ttu-id="1d0a2-105">Интерфейс графических устройств (GDI) Microsoft Windows позволяет приложениям использовать графику и форматированный текст как на экране видео, так и на принтере.</span><span class="sxs-lookup"><span data-stu-id="1d0a2-105">The Microsoft Windows graphics device interface (GDI) enables applications to use graphics and formatted text on both the video display and the printer.</span></span> <span data-ttu-id="1d0a2-106">Приложения на основе Windows не обращаются к графическому оборудованию напрямую.</span><span class="sxs-lookup"><span data-stu-id="1d0a2-106">Windows-based applications do not access the graphics hardware directly.</span></span> <span data-ttu-id="1d0a2-107">Вместо этого GDI взаимодействует с драйверами устройств от имени приложений.</span><span class="sxs-lookup"><span data-stu-id="1d0a2-107">Instead, GDI interacts with device drivers on behalf of applications.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1d0a2-108">Где применимо</span><span class="sxs-lookup"><span data-stu-id="1d0a2-108">Where applicable</span></span>

<span data-ttu-id="1d0a2-109">GDI можно использовать во всех приложениях на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="1d0a2-109">GDI can be used in all Windows-based applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1d0a2-110">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="1d0a2-110">Developer audience</span></span>

<span data-ttu-id="1d0a2-111">Этот API предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="1d0a2-111">This API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="1d0a2-112">Знание [архитектуры, управляемой сообщениями](../learnwin32/window-messages.md) Windows, является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1d0a2-112">Familiarity with the Windows [message-driven architecture](../learnwin32/window-messages.md) is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1d0a2-113">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="1d0a2-113">Run-time requirements</span></span>

<span data-ttu-id="1d0a2-114">Сведения о том, какие операционные системы требуются для использования определенной функции, см. в разделе "требования" документации по функции.</span><span class="sxs-lookup"><span data-stu-id="1d0a2-114">For information on which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1d0a2-115">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="1d0a2-115">In this section</span></span>

-   [<span data-ttu-id="1d0a2-116">Растровые изображения</span><span class="sxs-lookup"><span data-stu-id="1d0a2-116">Bitmaps</span></span>](bitmaps.md)
-   [<span data-ttu-id="1d0a2-117">Кисти</span><span class="sxs-lookup"><span data-stu-id="1d0a2-117">Brushes</span></span>](brushes.md)
-   [<span data-ttu-id="1d0a2-118">Вырезая</span><span class="sxs-lookup"><span data-stu-id="1d0a2-118">Clipping</span></span>](clipping.md)
-   [<span data-ttu-id="1d0a2-119">Цвета</span><span class="sxs-lookup"><span data-stu-id="1d0a2-119">Colors</span></span>](colors.md)
-   [<span data-ttu-id="1d0a2-120">Координатные пространства и преобразования</span><span class="sxs-lookup"><span data-stu-id="1d0a2-120">Coordinate Spaces and Transformations</span></span>](coordinate-spaces-and-transformations.md)
-   [<span data-ttu-id="1d0a2-121">Контексты устройств</span><span class="sxs-lookup"><span data-stu-id="1d0a2-121">Device Contexts</span></span>](device-contexts.md)
-   [<span data-ttu-id="1d0a2-122">Заполненные фигуры</span><span class="sxs-lookup"><span data-stu-id="1d0a2-122">Filled Shapes</span></span>](filled-shapes.md)
-   [<span data-ttu-id="1d0a2-123">Шрифты и текст</span><span class="sxs-lookup"><span data-stu-id="1d0a2-123">Fonts and Text</span></span>](fonts-and-text.md)
-   [<span data-ttu-id="1d0a2-124">Линии и кривые</span><span class="sxs-lookup"><span data-stu-id="1d0a2-124">Lines and Curves</span></span>](lines-and-curves.md)
-   [<span data-ttu-id="1d0a2-125">Метафайлы</span><span class="sxs-lookup"><span data-stu-id="1d0a2-125">Metafiles</span></span>](metafiles.md)
-   [<span data-ttu-id="1d0a2-126">Несколько мониторов экрана</span><span class="sxs-lookup"><span data-stu-id="1d0a2-126">Multiple Display Monitors</span></span>](multiple-display-monitors.md)
-   [<span data-ttu-id="1d0a2-127">Рисование и рисование</span><span class="sxs-lookup"><span data-stu-id="1d0a2-127">Painting and Drawing</span></span>](painting-and-drawing.md)
-   [<span data-ttu-id="1d0a2-128">Пути</span><span class="sxs-lookup"><span data-stu-id="1d0a2-128">Paths</span></span>](paths.md)
-   [<span data-ttu-id="1d0a2-129">Перья</span><span class="sxs-lookup"><span data-stu-id="1d0a2-129">Pens</span></span>](pens.md)
-   <span data-ttu-id="1d0a2-130">[Диспетчер очереди печати и печати](/previous-versions//dd162860(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d0a2-130">[Printing and Print Spooler](/previous-versions//dd162860(v=vs.85))</span></span>
-   [<span data-ttu-id="1d0a2-131">Прямоугольники</span><span class="sxs-lookup"><span data-stu-id="1d0a2-131">Rectangles</span></span>](rectangles.md)
-   [<span data-ttu-id="1d0a2-132">Регионы</span><span class="sxs-lookup"><span data-stu-id="1d0a2-132">Regions</span></span>](regions.md)

## <a name="related-topics"></a><span data-ttu-id="1d0a2-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1d0a2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d0a2-134">DirectX</span><span class="sxs-lookup"><span data-stu-id="1d0a2-134">DirectX</span></span>](https://msdn.microsoft.com/library/aa302281.aspx)
</dt> <dt>

[<span data-ttu-id="1d0a2-135">GDI+</span><span class="sxs-lookup"><span data-stu-id="1d0a2-135">GDI+</span></span>](../gdiplus/-gdiplus-gdi-start.md)
</dt> <dt>

[<span data-ttu-id="1d0a2-136">OpenGL</span><span class="sxs-lookup"><span data-stu-id="1d0a2-136">OpenGL</span></span>](../opengl/opengl.md)
</dt> <dt>

[<span data-ttu-id="1d0a2-137">Получение образа Windows</span><span class="sxs-lookup"><span data-stu-id="1d0a2-137">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> </dl>

 

 
