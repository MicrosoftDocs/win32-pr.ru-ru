---
description: Управление Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Управление Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682176"
---
# <a name="quality-control-management"></a><span data-ttu-id="a5352-103">Управление Quality-Control</span><span class="sxs-lookup"><span data-stu-id="a5352-103">Quality-Control Management</span></span>

<span data-ttu-id="a5352-104">Контроль качества — это механизм для настройки скорости потока данных с помощью графа фильтра в ответ на производительность во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a5352-104">Quality control is a mechanism for adjusting the rate of data flow through the filter graph in response to run-time performance.</span></span> <span data-ttu-id="a5352-105">Если фильтр модуля подготовки отчетов получает слишком много данных или слишком мало данных, он может отправить *качественное сообщение*.</span><span class="sxs-lookup"><span data-stu-id="a5352-105">If a renderer filter is receiving too much data or too little data, it can send a *quality message*.</span></span> <span data-ttu-id="a5352-106">В сообщении о контроле запрашивается коррекция скорости передачи данных.</span><span class="sxs-lookup"><span data-stu-id="a5352-106">The quality message requests an adjustment in the data rate.</span></span> <span data-ttu-id="a5352-107">По умолчанию сообщения о контроле качества передаются из модуля подготовки отчетов, пока не достигают фильтра, который может ответить (если таковой имеется).</span><span class="sxs-lookup"><span data-stu-id="a5352-107">By default, quality messages travel upstream from the renderer until they reach a filter that can respond (if any).</span></span> <span data-ttu-id="a5352-108">Приложение также может реализовать пользовательский диспетчер качества.</span><span class="sxs-lookup"><span data-stu-id="a5352-108">An application can also implement a custom quality manager.</span></span> <span data-ttu-id="a5352-109">В этом случае модуль подготовки отчетов передает качественные сообщения непосредственно менеджеру по качеству приложения.</span><span class="sxs-lookup"><span data-stu-id="a5352-109">In that case, the renderer passes quality messages directly to the application's quality manager.</span></span>

<span data-ttu-id="a5352-110">Эта статья содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="a5352-110">This article contains the following topics.</span></span>

-   [<span data-ttu-id="a5352-111">Сообщения о контроле качества</span><span class="sxs-lookup"><span data-stu-id="a5352-111">Quality Messages</span></span>](quality-messages.md)
-   [<span data-ttu-id="a5352-112">Контроль качества по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a5352-112">Default Quality Control</span></span>](default-quality-control.md)

## <a name="related-topics"></a><span data-ttu-id="a5352-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a5352-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5352-114">Поток данных для разработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="a5352-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="a5352-115">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="a5352-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



