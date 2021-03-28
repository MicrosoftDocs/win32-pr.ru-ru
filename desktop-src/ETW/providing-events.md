---
description: Поставщики — это приложения, которые содержат Инструментирование трассировки событий.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Предоставление событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984477"
---
# <a name="providing-events"></a><span data-ttu-id="de026-103">Предоставление событий</span><span class="sxs-lookup"><span data-stu-id="de026-103">Providing Events</span></span>

<span data-ttu-id="de026-104">Поставщики — это приложения, которые содержат Инструментирование трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="de026-104">Providers are applications that contain event tracing instrumentation.</span></span> <span data-ttu-id="de026-105">После того как поставщик регистрируется, контроллер может включить или отключить трассировку событий в поставщике.</span><span class="sxs-lookup"><span data-stu-id="de026-105">After a provider registers itself, a controller can then enable or disable event tracing in the provider.</span></span> <span data-ttu-id="de026-106">Поставщик определяет его интерпретацию включения или отключения.</span><span class="sxs-lookup"><span data-stu-id="de026-106">The provider defines its interpretation of being enabled or disabled.</span></span> <span data-ttu-id="de026-107">Как правило, включенный поставщик создает события, а отключенный поставщик — нет.</span><span class="sxs-lookup"><span data-stu-id="de026-107">Generally, an enabled provider generates events, and a disabled provider does not.</span></span> <span data-ttu-id="de026-108">Это позволяет добавлять в приложение трассировку событий, не требуя, чтобы она создавала события все время.</span><span class="sxs-lookup"><span data-stu-id="de026-108">This lets you add event tracing to your application without requiring that it generate events all the time.</span></span>

<span data-ttu-id="de026-109">В этом разделе показано, как:</span><span class="sxs-lookup"><span data-stu-id="de026-109">This section shows you how to:</span></span>

-   [<span data-ttu-id="de026-110">Запись событий</span><span class="sxs-lookup"><span data-stu-id="de026-110">Write events</span></span>](writing-events.md)
-   [<span data-ttu-id="de026-111">Запись связанных событий</span><span class="sxs-lookup"><span data-stu-id="de026-111">Write related events</span></span>](writing-related-events-in-an-end-to-end-scenario.md)
-   [<span data-ttu-id="de026-112">Публикация схемы событий для совместного использования с потребителями</span><span class="sxs-lookup"><span data-stu-id="de026-112">Publish your event schema to share with consumers</span></span>](publishing-your-event-schema.md)

<span data-ttu-id="de026-113">Дополнительные сведения об управлении сеансами трассировки событий см. в разделе [Управление сеансами трассировки событий](controlling-event-tracing-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="de026-113">For information about controlling event tracing sessions, see [Controlling Event Tracing Sessions](controlling-event-tracing-sessions.md).</span></span> <span data-ttu-id="de026-114">Сведения о потреблении событий от поставщика трассировки событий см. в разделе [Использование событий](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="de026-114">For information about consuming events from an event trace provider, see [Consuming Events](consuming-events.md).</span></span>

 

 



