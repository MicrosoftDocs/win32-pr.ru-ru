---
description: Имитация построения графа с помощью Графедит
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Имитация построения графа с помощью Графедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495228"
---
# <a name="simulating-graph-building-with-graphedit"></a><span data-ttu-id="ae54a-103">Имитация построения графа с помощью Графедит</span><span class="sxs-lookup"><span data-stu-id="ae54a-103">Simulating Graph Building with GraphEdit</span></span>

<span data-ttu-id="ae54a-104">DirectShow предоставляет служебную программу отладки с именем Графедит, которую можно использовать для создания и проверки графов фильтра.</span><span class="sxs-lookup"><span data-stu-id="ae54a-104">DirectShow provides a debugging utility called GraphEdit, which you can use to create and test filter graphs.</span></span>

<span data-ttu-id="ae54a-105">Графедит — это визуальное средство для создания графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="ae54a-105">GraphEdit is a visual tool for building filter graphs.</span></span> <span data-ttu-id="ae54a-106">С помощью Графедит можно поэкспериментировать с графом фильтра, прежде чем писать код приложения.</span><span class="sxs-lookup"><span data-stu-id="ae54a-106">With GraphEdit, you can experiment with a filter graph before you write any application code.</span></span> <span data-ttu-id="ae54a-107">Можно также загрузить граф фильтра, создаваемый приложением, чтобы убедиться, что приложение создает правильный граф.</span><span class="sxs-lookup"><span data-stu-id="ae54a-107">You can also load a filter graph that your application creates, to verify that your application is building the correct graph.</span></span> <span data-ttu-id="ae54a-108">Если вы разрабатываете пользовательский фильтр, Графедит предоставляет быстрый способ его тестирования: просто загрузите граф с настраиваемым фильтром и попробуйте запустить граф.</span><span class="sxs-lookup"><span data-stu-id="ae54a-108">If you develop a custom filter, GraphEdit provides a quick way to test it: Simply load a graph with your custom filter and try running the graph.</span></span> <span data-ttu-id="ae54a-109">Если вы не знакомы с DirectShow, Графедит является хорошим способом ознакомиться с графами фильтров и архитектурой DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ae54a-109">If you are new to DirectShow, GraphEdit is a good way to become familiar with filter graphs and the DirectShow architecture.</span></span>

<span data-ttu-id="ae54a-110">На следующем рисунке показано, как Графедит представляет простой граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="ae54a-110">The following illustration shows how GraphEdit represents a simple filter graph.</span></span>

![Простая диаграмма фильтра в графедит](images/gedit09.png)

<span data-ttu-id="ae54a-112">Каждый фильтр представлен в виде прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ae54a-112">Each filter is represented as a rectangle.</span></span> <span data-ttu-id="ae54a-113">Небольшие квадраты вдоль краев фильтров представляют контакты.</span><span class="sxs-lookup"><span data-stu-id="ae54a-113">Smaller squares along the edges of the filters represent pins.</span></span> <span data-ttu-id="ae54a-114">Входные контакты расположены слева от фильтра, а выходные контакты — справа.</span><span class="sxs-lookup"><span data-stu-id="ae54a-114">Input pins are on the left side of the filter, and output pins are on the right side.</span></span> <span data-ttu-id="ae54a-115">Стрелки представляют соединения между ПИН-контактами.</span><span class="sxs-lookup"><span data-stu-id="ae54a-115">The arrows represent the connections between pins.</span></span>

<span data-ttu-id="ae54a-116">С помощью Графедит можно:</span><span class="sxs-lookup"><span data-stu-id="ae54a-116">With GraphEdit, you can:</span></span>

-   <span data-ttu-id="ae54a-117">Создание и изменение графов фильтров с помощью визуального интерфейса, интерфейсов перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="ae54a-117">Create and modify filter graphs using a visual, drag-and-drop interface.</span></span>
-   <span data-ttu-id="ae54a-118">Имитировать программные вызовы для создания графа.</span><span class="sxs-lookup"><span data-stu-id="ae54a-118">Simulate programmatic calls to build a graph.</span></span>
-   <span data-ttu-id="ae54a-119">Выполнение, приостановка, остановка и поиск графа.</span><span class="sxs-lookup"><span data-stu-id="ae54a-119">Run, pause, stop, and seek a graph.</span></span>
-   <span data-ttu-id="ae54a-120">Проверьте, какие фильтры зарегистрированы на компьютере, и просмотрите сведения о реестре для каждого фильтра.</span><span class="sxs-lookup"><span data-stu-id="ae54a-120">See what filters are registered on your computer, and view registry information for each filter.</span></span>
-   <span data-ttu-id="ae54a-121">Просмотр страниц свойств фильтра.</span><span class="sxs-lookup"><span data-stu-id="ae54a-121">View filter property pages.</span></span>
-   <span data-ttu-id="ae54a-122">Просмотр типов мультимедиа-подключений.</span><span class="sxs-lookup"><span data-stu-id="ae54a-122">View the media types of pin connections.</span></span>

<span data-ttu-id="ae54a-123">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="ae54a-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="ae54a-124">Использование Графедит</span><span class="sxs-lookup"><span data-stu-id="ae54a-124">Using GraphEdit</span></span>](using-graphedit.md)
-   [<span data-ttu-id="ae54a-125">Загрузка графа из внешнего процесса</span><span class="sxs-lookup"><span data-stu-id="ae54a-125">Loading a Graph From an External Process</span></span>](loading-a-graph-from-an-external-process.md)
-   [<span data-ttu-id="ae54a-126">Сохранение графа фильтра в файл Графедит</span><span class="sxs-lookup"><span data-stu-id="ae54a-126">Saving a Filter Graph to a GraphEdit File</span></span>](saving-a-filter-graph-to-a-graphedit-file.md)
-   [<span data-ttu-id="ae54a-127">Программная загрузка файла Графедит</span><span class="sxs-lookup"><span data-stu-id="ae54a-127">Loading a GraphEdit File Programmatically</span></span>](loading-a-graphedit-file-programmatically.md)
-   [<span data-ttu-id="ae54a-128">Формат файла Графедит</span><span class="sxs-lookup"><span data-stu-id="ae54a-128">GraphEdit File Format</span></span>](graphedit-file-format.md)

## <a name="related-topics"></a><span data-ttu-id="ae54a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ae54a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae54a-130">Использование DirectShow</span><span class="sxs-lookup"><span data-stu-id="ae54a-130">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



