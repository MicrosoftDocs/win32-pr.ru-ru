---
title: Примеры анимации Windows
description: Разделы, содержащиеся в этом разделе, содержат сведения о примерах кода, которые поддерживают документацию по диспетчеру анимации Windows.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Анимация Windows, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331643"
---
# <a name="windows-animation-samples"></a><span data-ttu-id="6c11c-104">Примеры анимации Windows</span><span class="sxs-lookup"><span data-stu-id="6c11c-104">Windows Animation Samples</span></span>

<span data-ttu-id="6c11c-105">Разделы, содержащиеся в этом разделе, содержат сведения о примерах кода, которые поддерживают документацию по диспетчеру анимации Windows.</span><span class="sxs-lookup"><span data-stu-id="6c11c-105">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6c11c-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="6c11c-106">In this section</span></span>



| <span data-ttu-id="6c11c-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="6c11c-107">Topic</span></span>                                                                                     | <span data-ttu-id="6c11c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6c11c-108">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c11c-109">Пример анимации на основе приложений</span><span class="sxs-lookup"><span data-stu-id="6c11c-109">Application-Driven Animation Sample</span></span>](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [<span data-ttu-id="6c11c-110">Пример анимации на основе таймера</span><span class="sxs-lookup"><span data-stu-id="6c11c-110">Timer-Driven Animation Sample</span></span>](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [<span data-ttu-id="6c11c-111">Пользовательский пример интерполяции</span><span class="sxs-lookup"><span data-stu-id="6c11c-111">Custom Interpolator Sample</span></span>](custom-interpolator-sample.md)<br/>                   | <span data-ttu-id="6c11c-112">Показывает, как использовать анимацию Windows с собственным пользовательским интерполяцией с Direct2D, используемой для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6c11c-112">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <br/> |
| [<span data-ttu-id="6c11c-113">Образец макета сетки</span><span class="sxs-lookup"><span data-stu-id="6c11c-113">Grid Layout Sample</span></span>](grid-layout-sample.md)<br/>                                   | <span data-ttu-id="6c11c-114">Показывает, как использовать анимацию Windows с помощью Direct2D для анимации сетки изображений.</span><span class="sxs-lookup"><span data-stu-id="6c11c-114">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span> <br/>                         |
| [<span data-ttu-id="6c11c-115">Пример сравнения приоритетов</span><span class="sxs-lookup"><span data-stu-id="6c11c-115">Priority Comparison Sample</span></span>](priority-comparison-sample.md)<br/>                   | <span data-ttu-id="6c11c-116">Показывает, как использовать анимацию Windows с собственным сравнением приоритетов с помощью Direct2D для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="6c11c-116">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span><br/>      |



 

## <a name="sample-files"></a><span data-ttu-id="6c11c-117">Файлы образца</span><span class="sxs-lookup"><span data-stu-id="6c11c-117">Sample Files</span></span>

<span data-ttu-id="6c11c-118">Каждый пример содержит множество следующих файлов ключей:</span><span class="sxs-lookup"><span data-stu-id="6c11c-118">Each sample contains many of the following key files:</span></span>

<dl> <dt>

<span data-ttu-id="6c11c-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp</span><span class="sxs-lookup"><span data-stu-id="6c11c-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp</span></span>
</dt> <dd>

<span data-ttu-id="6c11c-120">Определяет точку входа приложения.</span><span class="sxs-lookup"><span data-stu-id="6c11c-120">Defines the application entry point.</span></span>

</dd> <dt>

<span data-ttu-id="6c11c-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h</span><span class="sxs-lookup"><span data-stu-id="6c11c-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h</span></span>
</dt> <dd>

<span data-ttu-id="6c11c-122">Объявляет класс Кмаинвиндов.</span><span class="sxs-lookup"><span data-stu-id="6c11c-122">Declares the CMainWindow class.</span></span>

</dd> <dt>

<span data-ttu-id="6c11c-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp</span><span class="sxs-lookup"><span data-stu-id="6c11c-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp</span></span>
</dt> <dd>

<span data-ttu-id="6c11c-124">Инициализирует компоненты анимации и графическую платформу, загружает изображения и готовит к просмотру клиентской области.</span><span class="sxs-lookup"><span data-stu-id="6c11c-124">Initializes the animation components and the graphics platform, loads images, and renders the client area.</span></span>

</dd> <dt>

<span data-ttu-id="6c11c-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>Лайаутманажер. h</span><span class="sxs-lookup"><span data-stu-id="6c11c-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h</span></span>
</dt> <dd>

<span data-ttu-id="6c11c-126">Объявляет класс Клайаутманажер.</span><span class="sxs-lookup"><span data-stu-id="6c11c-126">Declares the CLayoutManager class.</span></span>

</dd> <dt>

<span data-ttu-id="6c11c-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>Лайаутманажер. cpp</span><span class="sxs-lookup"><span data-stu-id="6c11c-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp</span></span>
</dt> <dd>

<span data-ttu-id="6c11c-128">Вычисляет макет изображений в главном окне, создает раскадровки, добавляет переходы в раскадровку и планирует раскадровку.</span><span class="sxs-lookup"><span data-stu-id="6c11c-128">Calculates the layout of images in the main window, creates storyboards, adds transitions to the storyboard, and schedules the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="6c11c-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail. h</span><span class="sxs-lookup"><span data-stu-id="6c11c-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h</span></span>
</dt> <dd>

<span data-ttu-id="6c11c-130">Объявляет класс Ксумбнаил.</span><span class="sxs-lookup"><span data-stu-id="6c11c-130">Declares the CThumbNail class.</span></span>

</dd> <dt>

<span data-ttu-id="6c11c-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Эскиз. cpp</span><span class="sxs-lookup"><span data-stu-id="6c11c-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp</span></span>
</dt> <dd>

<span data-ttu-id="6c11c-132">Создает переменные анимации и визуализирует эскизы.</span><span class="sxs-lookup"><span data-stu-id="6c11c-132">Creates animation variables and renders thumbnails.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6c11c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="6c11c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c11c-134">Руководством по разработке анимации Windows</span><span class="sxs-lookup"><span data-stu-id="6c11c-134">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)
</dt> <dt>

[<span data-ttu-id="6c11c-135">Справочник по анимации Windows</span><span class="sxs-lookup"><span data-stu-id="6c11c-135">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

 





