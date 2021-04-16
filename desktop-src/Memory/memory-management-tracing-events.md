---
description: 'Дополнительные сведения: события трассировки управления памятью'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: События трассировки управления памятью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664674"
---
# <a name="memory-management-tracing-events"></a><span data-ttu-id="d2fd4-103">События трассировки управления памятью</span><span class="sxs-lookup"><span data-stu-id="d2fd4-103">Memory Management Tracing Events</span></span>

<span data-ttu-id="d2fd4-104">В этом разделе описаны подробные сведения о конкретном событии трассировки управления памятью.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-104">This section describes detailed information on specific Memory management tracing event details.</span></span>

<span data-ttu-id="d2fd4-105">Трассировка управления памятью — это функция устранения неполадок, которую можно включить в двоичных файлах розничной торговли для трассировки определенных событий управления памятью с минимальными издержками.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-105">Memory management tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain memory management events with minimal overhead.</span></span> <span data-ttu-id="d2fd4-106">Эта функция обеспечивает улучшенные возможности диагностики для разработчиков и поддержки продуктов.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="d2fd4-107">Трассировка событий управления памятью поддерживает операции выделения, перераспределения и освобождения кучи трассировки.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-107">Memory management event tracing supports tracing heap allocation, reallocation, and free operations.</span></span>

<span data-ttu-id="d2fd4-108">Трассировка событий управления памятью использует средство трассировки событий для Windows (ETW), предназначенное для общего назначения, высокоскоростной трассировки, обеспечиваемой операционной системой.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-108">Memory management event tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="d2fd4-109">ETW предоставляет механизм трассировки для событий, создаваемых как приложениями пользовательского режима, так и драйверами устройств в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-109">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="d2fd4-110">ETW может динамически включать и отключать ведение журнала, что упрощает выполнение подробной трассировки в рабочих средах без необходимости перезагрузки или перезапуска приложений.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-110">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="d2fd4-111">Трассировка событий управления памятью с помощью ETW поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-111">Memory management event tracing using ETW is supported on Windows 7 , Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="d2fd4-112">Общие сведения о трассировке событий Windows см. в статье [улучшение отладки и настройка производительности с помощью ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="d2fd4-112">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="d2fd4-113">В следующем списке приведены подробные сведения о каждом событии трассировки управления памятью.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-113">The following list provides detailed information for each memory management tracing event.</span></span> <span data-ttu-id="d2fd4-114">Для получения дополнительных сведений о любом событии щелкните имя события.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-114">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="d2fd4-115">Название мероприятия</span><span class="sxs-lookup"><span data-stu-id="d2fd4-115">Event Name</span></span>                                                  | <span data-ttu-id="d2fd4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d2fd4-116">Description</span></span>                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="d2fd4-117">**\_ \_ выделено событие кучи ETW \_**</span><span class="sxs-lookup"><span data-stu-id="d2fd4-117">**ETW\_HEAP\_EVENT\_ALLOC**</span></span>](etw-heap-event-alloc.md)     | <span data-ttu-id="d2fd4-118">Событие трассировки управления памятью для операции выделения кучи.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-118">Memory management tracing event for a heap allocation operation.</span></span>    |
| [<span data-ttu-id="d2fd4-119">**\_событие КУЧИ \_ ETW \_ свободно**</span><span class="sxs-lookup"><span data-stu-id="d2fd4-119">**ETW\_HEAP\_EVENT\_FREE**</span></span>](etw-heap-event-free.md)       | <span data-ttu-id="d2fd4-120">Событие трассировки управления памятью для операции освобождения кучи.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-120">Memory management tracing event for a heap free operation.</span></span>          |
| [<span data-ttu-id="d2fd4-121">**перераспределение \_ событий КУЧИ ETW \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d2fd4-121">**ETW\_HEAP\_EVENT\_REALLOC**</span></span>](etw-heap-event-realloc.md) | <span data-ttu-id="d2fd4-122">Событие трассировки управления памятью для операции повторного выделения кучи.</span><span class="sxs-lookup"><span data-stu-id="d2fd4-122">Memory management tracing event for a heap re-allocation operation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d2fd4-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d2fd4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2fd4-124">Усовершенствованные отладка и настройка производительности с помощью приложения ETW</span><span class="sxs-lookup"><span data-stu-id="d2fd4-124">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
