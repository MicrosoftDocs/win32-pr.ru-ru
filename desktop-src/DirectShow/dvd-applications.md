---
description: DVD-приложения
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: DVD-приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341852"
---
# <a name="dvd-applications"></a><span data-ttu-id="5630a-103">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="5630a-103">DVD Applications</span></span>

<span data-ttu-id="5630a-104">DirectShow предоставляет компонент, называемый фильтром источника « [DVD Navigator](dvd-navigator-filter.md) », который упрощает задачи навигации по DVD в C++.</span><span class="sxs-lookup"><span data-stu-id="5630a-104">DirectShow provides a component called the [DVD Navigator](dvd-navigator-filter.md) source filter which simplifies DVD navigation tasks in C++.</span></span> <span data-ttu-id="5630a-105">DVD-навигатор содержит все возможности, которые можно найти на полнофункциональном автономном DVD-проигрывателе, а также дополнительные возможности для воспроизведения DVD-дисков на персональных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="5630a-105">The DVD Navigator has all the capabilities that you find on a full-featured stand-alone DVD player, plus additional capabilities specific to playing DVDs on personal computers.</span></span> <span data-ttu-id="5630a-106">С помощью DVD Navigator, C++ и разработчиков сценариев можно создавать полнофункциональные DVD-приложения, не обращаясь к спецификации DVD.</span><span class="sxs-lookup"><span data-stu-id="5630a-106">Using the DVD Navigator, C++ and scripting developers can create full-featured DVD applications without referring to the DVD specification.</span></span> <span data-ttu-id="5630a-107">Навигатор DVD, в координации с фильтрами декодера, также управляет региональным управлением и защитой авторских прав (CSS и аналоговая защита от копирования), изолируя разработчиков приложений от этих сведений.</span><span class="sxs-lookup"><span data-stu-id="5630a-107">The DVD Navigator, in coordination with the decoder filters, also handles regional management and copyright protection (CSS and analog copy protection), isolating application developers from these details.</span></span>

<span data-ttu-id="5630a-108">Фильтр "Навигатор DVD" работает во всем DVD-Video том, который состоит из файлов в \_ каталоге Video TS.</span><span class="sxs-lookup"><span data-stu-id="5630a-108">The DVD Navigator filter works across an entire DVD-Video volume, which consists of the files in the VIDEO\_TS directory.</span></span> <span data-ttu-id="5630a-109">В отличие от большинства фильтров источника DirectShow, работающих с отдельными потоками или файлами, Навигатор DVD использует DVD-Video структуру заголовков, глав и кодов времени.</span><span class="sxs-lookup"><span data-stu-id="5630a-109">Unlike most DirectShow source filters that work with individual streams or files, the DVD Navigator uses the DVD-Video structure of titles, chapters, and time codes.</span></span> <span data-ttu-id="5630a-110">Разработчики, желающие воспроизвести отдельные файлы MPEG-2 в DirectShow, должны использовать [демультиплексор MPEG-2](mpeg-2-demultiplexer.md) вместо фильтра DVD Navigator.</span><span class="sxs-lookup"><span data-stu-id="5630a-110">Developers wishing to play individual MPEG-2 files in DirectShow should use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead of the DVD Navigator filter.</span></span> <span data-ttu-id="5630a-111">Дополнительные сведения см. [в статье поддержка MPEG-2 в DirectShow](mpeg-2-support-in-directshow.md) .</span><span class="sxs-lookup"><span data-stu-id="5630a-111">See [MPEG-2 Support in DirectShow](mpeg-2-support-in-directshow.md) for more information.</span></span>

> [!Note]  
> <span data-ttu-id="5630a-112">Для воспроизведения DVD пользователь должен иметь декодер MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5630a-112">To play DVDs, the user must have an MPEG-2 decoder.</span></span>

 

<span data-ttu-id="5630a-113">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="5630a-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="5630a-114">Функции поддержки DVD в DirectShow</span><span class="sxs-lookup"><span data-stu-id="5630a-114">DVD Support Features in DirectShow</span></span>](dvd-support-features-in-directshow.md)
-   [<span data-ttu-id="5630a-115">Основные сведения о DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-115">DVD Basics</span></span>](dvd-basics.md)
-   [<span data-ttu-id="5630a-116">Создание графа фильтра DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-116">Building the DVD Filter Graph</span></span>](building-the-dvd-filter-graph.md)
-   [<span data-ttu-id="5630a-117">Получение указателей на DVD-интерфейсах</span><span class="sxs-lookup"><span data-stu-id="5630a-117">Obtaining the DVD Interface Pointers</span></span>](obtaining-the-dvd-interface-pointers.md)
-   [<span data-ttu-id="5630a-118">Команды DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-118">DVD Commands</span></span>](dvd-commands.md)
-   [<span data-ttu-id="5630a-119">Определение допустимых операций DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-119">Identifying Valid DVD Operations</span></span>](identifying-valid-dvd-operations.md)
-   [<span data-ttu-id="5630a-120">Синхронизация команд DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-120">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
-   [<span data-ttu-id="5630a-121">Поток данных в навигаторе DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-121">Data Flow in the DVD Navigator</span></span>](data-flow-in-the-dvd-navigator.md)
-   [<span data-ttu-id="5630a-122">Обработка уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-122">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
-   [<span data-ttu-id="5630a-123">Работа с меню DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-123">Working With DVD Menus</span></span>](working-with-dvd-menus.md)
-   [<span data-ttu-id="5630a-124">Потоки аудио и субтитров</span><span class="sxs-lookup"><span data-stu-id="5630a-124">Audio and Subpicture Streams</span></span>](audio-and-subpicture-streams.md)
-   [<span data-ttu-id="5630a-125">Применение уровней родительского управления</span><span class="sxs-lookup"><span data-stu-id="5630a-125">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
-   [<span data-ttu-id="5630a-126">Сохранение и восстановление объектов Двдстате</span><span class="sxs-lookup"><span data-stu-id="5630a-126">Saving and Restoring DvdState Objects</span></span>](saving-and-restoring-dvdstate-objects.md)
-   [<span data-ttu-id="5630a-127">Работа с текстовыми строками DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-127">Working with DVD Text Strings</span></span>](working-with-dvd-text-strings.md)
-   [<span data-ttu-id="5630a-128">Воспроизведение звуковых потоков Караоке</span><span class="sxs-lookup"><span data-stu-id="5630a-128">Playing Karaoke Audio Streams</span></span>](playing-karaoke-audio-streams.md)
-   [<span data-ttu-id="5630a-129">Обработка извлечения с диска</span><span class="sxs-lookup"><span data-stu-id="5630a-129">Handling Disc Ejections</span></span>](handling-disc-ejections.md)
-   [<span data-ttu-id="5630a-130">Усовершенствования воспроизведения DVD в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5630a-130">DVD Playback Enhancements in Windows Vista</span></span>](dvd-playback-enhancements-in-windows-vista.md)
-   [<span data-ttu-id="5630a-131">Конфигурация графа фильтра DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-131">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
-   [<span data-ttu-id="5630a-132">Ярлыки на страницы справочника по C++ DVD</span><span class="sxs-lookup"><span data-stu-id="5630a-132">Shortcuts to C++ DVD Reference Pages</span></span>](shortcuts-to-c-dvd-reference-pages.md)

<span data-ttu-id="5630a-133">Ссылки на разработку декодеров DVD/MPEG2 см. [в статье Разработка декодеров DVD в DirectShow](dvd-decoder-development-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="5630a-133">For references on DVD/MPEG2 decoder development, see [DVD Decoder Development in DirectShow](dvd-decoder-development-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5630a-134">См. также</span><span class="sxs-lookup"><span data-stu-id="5630a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5630a-135">Использование DirectShow</span><span class="sxs-lookup"><span data-stu-id="5630a-135">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



