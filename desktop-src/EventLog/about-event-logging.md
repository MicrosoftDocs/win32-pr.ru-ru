---
description: При возникновении ошибки системный администратор или специалист службы поддержки должен определить причину ошибки, попытаться восстановить потерянные данные и предотвратить повторную попытку.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Сведения о ведении журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080371"
---
# <a name="about-event-logging"></a><span data-ttu-id="c3f1c-103">Сведения о ведении журнала событий</span><span class="sxs-lookup"><span data-stu-id="c3f1c-103">About Event Logging</span></span>

<span data-ttu-id="c3f1c-104">При возникновении ошибки системный администратор или специалист службы поддержки должен определить причину ошибки, попытаться восстановить потерянные данные и предотвратить повторную попытку.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-104">When an error occurs, the system administrator or support representative must determine what caused the error, attempt to recover any lost data, and prevent the error from recurring.</span></span> <span data-ttu-id="c3f1c-105">Это полезно, если приложения, операционная система и другие системные службы записывают важные события, такие как условия нехватки памяти или чрезмерные попытки доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-105">It is helpful if applications, the operating system, and other system services record important events, such as low-memory conditions or excessive attempts to access a disk.</span></span> <span data-ttu-id="c3f1c-106">Затем системный администратор может использовать журнал событий, чтобы определить, какие условия привели к возникновению ошибки, и определить контекст, в котором она возникла.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-106">The system administrator can then use the event log to help determine what conditions caused the error and identify the context in which it occurred.</span></span> <span data-ttu-id="c3f1c-107">Периодически просмотрев журнал событий, системный администратор может обнаруживать проблемы (например, сбой жесткого диска), прежде чем они могут привести к повреждению.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-107">By periodically viewing the event log, the system administrator may be able to identify problems (such as a failing hard disk) before they cause damage.</span></span>

> [!Note]  
> <span data-ttu-id="c3f1c-108">API ведения журнала событий предназначен для приложений, работающих в операционной системе Windows Server 2003, Windows XP или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-108">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="c3f1c-109">В Windows Vista инфраструктура ведения журнала событий была изменена.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-109">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="c3f1c-110">Приложения, предназначенные для работы в операционной системе Windows Vista или более поздней версии, теперь должны использовать [журнал событий Windows](/windows/desktop/WES/windows-event-log) для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-110">Applications that are designed to run on the Windows Vista or later operating systems should now use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>

 
<span data-ttu-id="c3f1c-111">В этом разделе обсуждается интерфейс программирования для записи и использования событий с помощью ведения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-111">This section discusses the programming interface for writing and consuming events using Event Logging.</span></span>

-   [<span data-ttu-id="c3f1c-112">Типы событий</span><span class="sxs-lookup"><span data-stu-id="c3f1c-112">Event types</span></span>](event-types.md)
-   [<span data-ttu-id="c3f1c-113">Рекомендации по ведению журнала</span><span class="sxs-lookup"><span data-stu-id="c3f1c-113">Logging guidelines</span></span>](logging-guidelines.md)
-   [<span data-ttu-id="c3f1c-114">Элементы ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="c3f1c-114">Event logging elements</span></span>](event-logging-elements.md)
-   [<span data-ttu-id="c3f1c-115">Операции ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="c3f1c-115">Event logging operations</span></span>](event-logging-operations.md)
-   [<span data-ttu-id="c3f1c-116">Модель ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="c3f1c-116">Event logging model</span></span>](event-logging-model.md)
-   [<span data-ttu-id="c3f1c-117">Безопасность ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="c3f1c-117">Event logging security</span></span>](event-logging-security.md)

> [!Note]  
> <span data-ttu-id="c3f1c-118">Приложения, которые публикуют события размером более 64 килобайт на компьютере под управлением Windows Server 2003, Windows XP или Windows 2000, не смогут публиковать события на компьютере под управлением Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-118">Applications that publish events that are larger than 64 kilobytes on a Windows Server 2003, Windows XP, or Windows 2000 computer will not be able to publish events on a Windows Vista or later computer.</span></span>
