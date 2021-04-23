---
title: Схема запроса
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Дополнительные сведения: Схема запроса'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aa9b6c842ff7acd874e8e467d07c31e298a63564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265895"
---
# <a name="query-schema"></a><span data-ttu-id="2d3a4-103">Схема запроса</span><span class="sxs-lookup"><span data-stu-id="2d3a4-103">Query Schema</span></span>

<span data-ttu-id="2d3a4-104">Схема запроса определяет следующие элементы и типы, которые можно использовать для написания структурированного XML-запроса для получения событий из канала или файла журнала:</span><span class="sxs-lookup"><span data-stu-id="2d3a4-104">The Query Schema defines the following elements and types that you can use to write a structured XML query to retrieve events from a channel or log file:</span></span>

-   [<span data-ttu-id="2d3a4-105">Элементы Куерисчема</span><span class="sxs-lookup"><span data-stu-id="2d3a4-105">QuerySchema Elements</span></span>](queryschema-elements.md)
-   [<span data-ttu-id="2d3a4-106">Сложные типы Куерисчема</span><span class="sxs-lookup"><span data-stu-id="2d3a4-106">QuerySchema Complex Types</span></span>](queryschema-complex-types.md)

<span data-ttu-id="2d3a4-107">Раздел Elements содержит имена элементов, используемых в запросе. Однако, чтобы получить подробные сведения для каждого элемента, см. сложный тип, содержащий элемент.</span><span class="sxs-lookup"><span data-stu-id="2d3a4-107">The elements section contains the names of the elements that you use in your query; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="2d3a4-108">Запрос может содержать одно или несколько выражений XPath, которые используются для включения или исключения событий в результирующем наборе запроса.</span><span class="sxs-lookup"><span data-stu-id="2d3a4-108">A query can contain one or more XPath expressions that are used to include or exclude event in the query result set.</span></span> <span data-ttu-id="2d3a4-109">Можно запрашивать события из нескольких каналов или файлов журналов, но нельзя смешивать каналы и файлы журналов.</span><span class="sxs-lookup"><span data-stu-id="2d3a4-109">You can query for events from multiple channels or log files but you cannot mix channels and log files.</span></span> <span data-ttu-id="2d3a4-110">Можно использовать запрос в любой функции, принимающей XPath (например, функции [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) или [**евтсубскрибе**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ).</span><span class="sxs-lookup"><span data-stu-id="2d3a4-110">You can use a query in any function that takes an XPath (for example, the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions).</span></span> <span data-ttu-id="2d3a4-111">Каждый заданный XPath ограничен 32 выражениями.</span><span class="sxs-lookup"><span data-stu-id="2d3a4-111">Each XPath that you specify is limited to 32 expressions.</span></span> <span data-ttu-id="2d3a4-112">Пример см. в разделе [Использование событий](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="2d3a4-112">For an example, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="2d3a4-113">Windows SDK включает схему в \\ \\ файл включения запроса. xsd.</span><span class="sxs-lookup"><span data-stu-id="2d3a4-113">The Windows SDK includes the schema in the \\Include\\Query.xsd file.</span></span>

<span data-ttu-id="2d3a4-114">В дополнение к схеме запроса журнал событий Windows также определяет следующие схемы:</span><span class="sxs-lookup"><span data-stu-id="2d3a4-114">In addition to the Query schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="2d3a4-115">[Евентманифест Schema](eventmanifestschema-schema.md)— определяет элементы и типы, используемые для записи манифеста инструментирования.</span><span class="sxs-lookup"><span data-stu-id="2d3a4-115">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="2d3a4-116">[Схема событий](eventschema-schema.md)— определяет элементы и типы, используемые для отрисовки события.</span><span class="sxs-lookup"><span data-stu-id="2d3a4-116">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d3a4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2d3a4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d3a4-118">Использование событий</span><span class="sxs-lookup"><span data-stu-id="2d3a4-118">Consuming Events</span></span>](consuming-events.md)
</dt> </dl>

 

 




