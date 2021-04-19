---
description: О диспетчере графов фильтров
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: О диспетчере графов фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537832"
---
# <a name="about-the-filter-graph-manager"></a><span data-ttu-id="a0f23-103">О диспетчере графов фильтров</span><span class="sxs-lookup"><span data-stu-id="a0f23-103">About the Filter Graph Manager</span></span>

<span data-ttu-id="a0f23-104">[Диспетчер графов фильтров](filter-graph-manager.md) — это COM-объект, управляющий фильтрами в графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="a0f23-104">The [Filter Graph Manager](filter-graph-manager.md) is a COM object that controls the filters in a filter graph.</span></span> <span data-ttu-id="a0f23-105">Он выполняет множество функций, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="a0f23-105">It performs many functions, including the following:</span></span>

-   <span data-ttu-id="a0f23-106">Согласование изменений состояния между фильтрами.</span><span class="sxs-lookup"><span data-stu-id="a0f23-106">Coordinating state changes among the filters.</span></span>
-   <span data-ttu-id="a0f23-107">Установка ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="a0f23-107">Establishing a reference clock.</span></span>
-   <span data-ttu-id="a0f23-108">Передача событий обратно в приложение.</span><span class="sxs-lookup"><span data-stu-id="a0f23-108">Communicating events back to the application.</span></span>
-   <span data-ttu-id="a0f23-109">Предоставление методов для приложений для построения графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="a0f23-109">Providing methods for applications to build the filter graph.</span></span>

<span data-ttu-id="a0f23-110">Каждая из этих функций описана вкратце.</span><span class="sxs-lookup"><span data-stu-id="a0f23-110">Each of these functions is described briefly here.</span></span> <span data-ttu-id="a0f23-111">Подробные сведения можно найти в другой части документации.</span><span class="sxs-lookup"><span data-stu-id="a0f23-111">Details can be found elsewhere in the documentation.</span></span>

<span data-ttu-id="a0f23-112">**Изменения состояния**.</span><span class="sxs-lookup"><span data-stu-id="a0f23-112">**State changes**.</span></span> <span data-ttu-id="a0f23-113">Изменения состояния в фильтрах должны выполняться в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="a0f23-113">State changes within filters must occur in a particular order.</span></span> <span data-ttu-id="a0f23-114">Таким образом, приложение не выполняет команды изменения состояния непосредственно в фильтры.</span><span class="sxs-lookup"><span data-stu-id="a0f23-114">Therefore, the application does not issue state-change commands directly to the filters.</span></span> <span data-ttu-id="a0f23-115">Вместо этого он предоставляет одну команду диспетчеру графа фильтров, которая распространяет команду на каждый из фильтров.</span><span class="sxs-lookup"><span data-stu-id="a0f23-115">Instead, it gives a single command to the Filter Graph Manager, which distributes the command to each of the filters.</span></span> <span data-ttu-id="a0f23-116">Поиск работает аналогичным образом: приложение передает команду Seek диспетчеру графа фильтров, который распределяет его по фильтрам.</span><span class="sxs-lookup"><span data-stu-id="a0f23-116">Seeking works in a similar fashion: The application gives a seek command to the Filter Graph Manager, which distributes it to the filters.</span></span>

<span data-ttu-id="a0f23-117">**Ссылочное время**.</span><span class="sxs-lookup"><span data-stu-id="a0f23-117">**Reference clock**.</span></span> <span data-ttu-id="a0f23-118">Все фильтры в графе используют одинаковые часы, называемые *ссылочным временем*.</span><span class="sxs-lookup"><span data-stu-id="a0f23-118">All of the filters in the graph use the same clock, called a *reference clock*.</span></span> <span data-ttu-id="a0f23-119">Ссылочное время гарантирует, что все потоки будут синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="a0f23-119">The reference clock ensures that all the streams are synchronized.</span></span> <span data-ttu-id="a0f23-120">Время, когда необходимо визуализировать видеокадр или образец звука, называется *временем презентации*.</span><span class="sxs-lookup"><span data-stu-id="a0f23-120">The time at which a video frame or audio sample should be rendered is called the *presentation time*.</span></span> <span data-ttu-id="a0f23-121">Время презентации измеряется относительно ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="a0f23-121">The presentation time is measured relative to the reference clock.</span></span> <span data-ttu-id="a0f23-122">Диспетчер графов фильтров выбирает контрольные часы, обычно часы звуковой карты или системные часы.</span><span class="sxs-lookup"><span data-stu-id="a0f23-122">The Filter Graph Manager chooses a reference clock, usually either the clock on the sound card, or the system clock.</span></span>

<span data-ttu-id="a0f23-123">**События графа**.</span><span class="sxs-lookup"><span data-stu-id="a0f23-123">**Graph events**.</span></span> <span data-ttu-id="a0f23-124">Диспетчер графов фильтров использует очередь событий для информирования приложения о событиях, происходящих в графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="a0f23-124">The Filter Graph Manager uses an event queue to inform the application of events that occur in the filter graph.</span></span> <span data-ttu-id="a0f23-125">Этот механизм аналогичен циклу обработки сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="a0f23-125">This mechanism is similar to a Windows message loop.</span></span>

<span data-ttu-id="a0f23-126">**Методы построения графа**.</span><span class="sxs-lookup"><span data-stu-id="a0f23-126">**Graph-building methods**.</span></span> <span data-ttu-id="a0f23-127">Диспетчер графов фильтров предоставляет приложениям методы для добавления фильтров к графу, подключения фильтров к другим фильтрам и фильтров отключения.</span><span class="sxs-lookup"><span data-stu-id="a0f23-127">The Filter Graph Manager provides methods for the application to add filters to the graph, connect filters to other filters, and disconnect filters.</span></span>

<span data-ttu-id="a0f23-128">Одна из функций, которую диспетчер графов фильтров не обрабатывает, — перемещение данных из одного фильтра в следующий.</span><span class="sxs-lookup"><span data-stu-id="a0f23-128">One function the Filter Graph Manager does not handle is moving data from one filter to the next.</span></span> <span data-ttu-id="a0f23-129">Это делается самими фильтрами, через их подключения.</span><span class="sxs-lookup"><span data-stu-id="a0f23-129">This is done by the filters themselves, through their pin connections.</span></span> <span data-ttu-id="a0f23-130">Обработка всегда происходит в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="a0f23-130">Processing always happens on a separate thread.</span></span>

> [!Note]  
> <span data-ttu-id="a0f23-131">Фильтры всегда находятся в свободной потоке, находятся в том же процессе, что и диспетчер графа фильтров, и загружаются с внутрипроцессного сервера.</span><span class="sxs-lookup"><span data-stu-id="a0f23-131">Filters are always free-threaded, reside in the same process as the Filter Graph Manager, and are loaded from in-process servers.</span></span> <span data-ttu-id="a0f23-132">Таким образом, вызовы методов не маршалируются между фильтрами или между фильтрами и диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="a0f23-132">Therefore, method calls are not marshaled between filters, or between filters and the Filter Graph Manager.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a0f23-133">См. также</span><span class="sxs-lookup"><span data-stu-id="a0f23-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f23-134">Поток данных в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="a0f23-134">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="a0f23-135">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0f23-135">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="a0f23-136">Настройка часов графа</span><span class="sxs-lookup"><span data-stu-id="a0f23-136">Setting the Graph Clock</span></span>](setting-the-graph-clock.md)
</dt> <dt>

[<span data-ttu-id="a0f23-137">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0f23-137">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



