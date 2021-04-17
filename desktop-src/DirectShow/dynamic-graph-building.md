---
description: Построение динамического графа
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Построение динамического графа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673031"
---
# <a name="dynamic-graph-building"></a><span data-ttu-id="31c44-103">Построение динамического графа</span><span class="sxs-lookup"><span data-stu-id="31c44-103">Dynamic Graph Building</span></span>

<span data-ttu-id="31c44-104">Если необходимо изменить существующий граф фильтра, можно отключить граф, внести изменения и перезапустить диаграмму.</span><span class="sxs-lookup"><span data-stu-id="31c44-104">If you need to modify an existing filter graph, you can stop the graph, make the changes, and restart the graph.</span></span> <span data-ttu-id="31c44-105">Обычно это лучший подход.</span><span class="sxs-lookup"><span data-stu-id="31c44-105">This is usually the best approach.</span></span> <span data-ttu-id="31c44-106">Однако в некоторых случаях может потребоваться изменить график, пока он все еще выполняется.</span><span class="sxs-lookup"><span data-stu-id="31c44-106">However, under some circumstances, you might want to alter a graph while it is still running.</span></span> <span data-ttu-id="31c44-107">Пример:</span><span class="sxs-lookup"><span data-stu-id="31c44-107">For example:</span></span>

-   <span data-ttu-id="31c44-108">Приложение вставляет фильтр видеоэффектов во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="31c44-108">The application inserts a video effects filter during playback.</span></span>
-   <span data-ttu-id="31c44-109">Фильтр источника переключает типы носителей вернуться, возможно, требует нового фильтра распаковки.</span><span class="sxs-lookup"><span data-stu-id="31c44-109">A source filter switches media types midstream, possibly requiring a new decompression filter.</span></span>
-   <span data-ttu-id="31c44-110">Приложение добавляет новый поток видео в граф.</span><span class="sxs-lookup"><span data-stu-id="31c44-110">The application adds a new video stream to the graph.</span></span>

<span data-ttu-id="31c44-111">Все это примеры *динамического построения графа*— термин, охватывающий любые изменения в графе фильтра, пока график продолжит работать.</span><span class="sxs-lookup"><span data-stu-id="31c44-111">These are all examples of *dynamic graph building*, a term that covers any kind of change to a filter graph while the graph continues to run.</span></span> <span data-ttu-id="31c44-112">Построение динамического графа может инициироваться приложением или фильтром в графе.</span><span class="sxs-lookup"><span data-stu-id="31c44-112">Dynamic graph building can be initiated by an application or by a filter in the graph.</span></span> <span data-ttu-id="31c44-113">Возможны три различных сценария:</span><span class="sxs-lookup"><span data-stu-id="31c44-113">Three distinct scenarios are possible:</span></span>

-   <span data-ttu-id="31c44-114">[Изменения динамического формата](dynamic-format-changes.md): фильтр может изменять форматы вернуться, без необходимости удалять или заменять фильтры.</span><span class="sxs-lookup"><span data-stu-id="31c44-114">[Dynamic Format Changes](dynamic-format-changes.md): A filter can change formats midstream, without the need to remove or replace any filters.</span></span>
-   <span data-ttu-id="31c44-115">[Динамическое](dynamic-reconnection.md)повторное подключение: изменение диаграммы путем добавления или удаления фильтров.</span><span class="sxs-lookup"><span data-stu-id="31c44-115">[Dynamic Reconnection](dynamic-reconnection.md): Changing the graph by adding or removing filters.</span></span>
-   <span data-ttu-id="31c44-116">[Цепочки фильтров](filter-chains.md): Добавление, удаление и управление цепочками фильтров.</span><span class="sxs-lookup"><span data-stu-id="31c44-116">[Filter Chains](filter-chains.md): Adding, removing, and controlling chains of filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31c44-117">См. также</span><span class="sxs-lookup"><span data-stu-id="31c44-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31c44-118">О DirectShow</span><span class="sxs-lookup"><span data-stu-id="31c44-118">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



