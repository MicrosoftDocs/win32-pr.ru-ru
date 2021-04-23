---
description: Функции Опеневентлог, Опенбаккупевентлог, Регистеревентсаурце, Дерегистеревентсаурце и Клосивентлог открывают и закрывают дескрипторы журнала событий.
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: Операции ведения журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065acd268788de8c9674baa1fe47a3b89a719d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683285"
---
# <a name="event-logging-operations"></a><span data-ttu-id="242c5-103">Операции ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="242c5-103">Event Logging Operations</span></span>

<span data-ttu-id="242c5-104">Функции [**опеневентлог**](/windows/desktop/api/Winbase/nf-winbase-openeventloga), [**опенбаккупевентлог**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga), [**регистеревентсаурце**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea), [**дерегистеревентсаурце**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)и [**клосивентлог**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) открывают и закрывают дескрипторы журнала событий.</span><span class="sxs-lookup"><span data-stu-id="242c5-104">The [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga), [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga), [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea), [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource), and [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) functions open and close event log handles.</span></span>

<span data-ttu-id="242c5-105">В следующей таблице показаны операции, которые можно выполнить с открытым журналом событий, и соответствующая функция для каждой операции.</span><span class="sxs-lookup"><span data-stu-id="242c5-105">The following table shows the operations that can be performed on an open event log, and the corresponding function for each operation.</span></span>



| <span data-ttu-id="242c5-106">Операция</span><span class="sxs-lookup"><span data-stu-id="242c5-106">Operation</span></span> | <span data-ttu-id="242c5-107">Функция</span><span class="sxs-lookup"><span data-stu-id="242c5-107">Function</span></span>                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="242c5-108">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="242c5-108">Backup</span></span>    | [<span data-ttu-id="242c5-109">**баккупевентлог**</span><span class="sxs-lookup"><span data-stu-id="242c5-109">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| <span data-ttu-id="242c5-110">Clear</span><span class="sxs-lookup"><span data-stu-id="242c5-110">Clear</span></span>     | [<span data-ttu-id="242c5-111">**клеаревентлог**</span><span class="sxs-lookup"><span data-stu-id="242c5-111">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| <span data-ttu-id="242c5-112">Монитор</span><span class="sxs-lookup"><span data-stu-id="242c5-112">Monitor</span></span>   | [<span data-ttu-id="242c5-113">**нотифичанжеевентлог**</span><span class="sxs-lookup"><span data-stu-id="242c5-113">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| <span data-ttu-id="242c5-114">Запрос</span><span class="sxs-lookup"><span data-stu-id="242c5-114">Query</span></span>     | <span data-ttu-id="242c5-115">[**Жетолдестевентлогрекорд**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [ **жетнумберофевентлогрекордс**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords)</span><span class="sxs-lookup"><span data-stu-id="242c5-115">[**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord), [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords)</span></span> |
| <span data-ttu-id="242c5-116">Чтение</span><span class="sxs-lookup"><span data-stu-id="242c5-116">Read</span></span>      | [<span data-ttu-id="242c5-117">**реадевентлог**</span><span class="sxs-lookup"><span data-stu-id="242c5-117">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| <span data-ttu-id="242c5-118">запись</span><span class="sxs-lookup"><span data-stu-id="242c5-118">Write</span></span>     | [<span data-ttu-id="242c5-119">**репортевент**</span><span class="sxs-lookup"><span data-stu-id="242c5-119">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

<span data-ttu-id="242c5-120">Функции [**опеневентлог**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) и [**репортевент**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) принимают в качестве параметра необязательное имя сервера, что позволяет выполнять операции на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="242c5-120">The [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) and [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) functions take an optional server name as a parameter so the operations can be performed on the remote server.</span></span> <span data-ttu-id="242c5-121">Используйте [**опеневентлог**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) для чтения или выполнения административных операций (резервное копирование, очистка, мониторинг и выполнение запросов) в журнале и использование [**регистеревентсаурце**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) для записи в журнал.</span><span class="sxs-lookup"><span data-stu-id="242c5-121">Use [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) for reading or performing administrative operations (backup, clear, monitor, and query) on the log, and use [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) for writing to the log.</span></span>

<span data-ttu-id="242c5-122">Каждый вызов функции ведения журнала событий является атомарной операцией.</span><span class="sxs-lookup"><span data-stu-id="242c5-122">Each call to an event logging function is an atomic operation.</span></span> <span data-ttu-id="242c5-123">При чтении из журнала событий возвращаются только целые записи событий.</span><span class="sxs-lookup"><span data-stu-id="242c5-123">When you read from the event log, only whole event records are returned.</span></span> <span data-ttu-id="242c5-124">При записи в журнал событий каждая запись события гарантированно записывается последовательно как полная запись в журнале.</span><span class="sxs-lookup"><span data-stu-id="242c5-124">When you write to the event log, each event record is guaranteed to be written sequentially as a complete record in the log.</span></span> <span data-ttu-id="242c5-125">В следующем списке описано, как служба ведения журнала событий обрабатывает особые условия.</span><span class="sxs-lookup"><span data-stu-id="242c5-125">The following list describes how the event-logging service handles special conditions:</span></span>

-   <span data-ttu-id="242c5-126">Служба ведения журнала событий получает операцию чтения и операцию записи одновременно: Если значение позиции чтения находится в конце файла, то либо операция чтения завершается с ошибкой "конец файла" (если операция записи не была завершена), либо возвращается новая запись (если операция записи завершена).</span><span class="sxs-lookup"><span data-stu-id="242c5-126">The event-logging service receives a read operation and a write operation at the same time: If the read position is at the end of the file, either the read operation fails with an "end-of-file" status (if the write operation has not been completed), or it returns the new record (if the write operation has been completed).</span></span>
-   <span data-ttu-id="242c5-127">Служба ведения журнала событий завершает операцию очистки перед получением операции чтения: операция чтения завершается сбоем с состоянием "конец файла".</span><span class="sxs-lookup"><span data-stu-id="242c5-127">The event-logging service completes a clear operation before receiving a read operation: The read operation fails with "end-of-file" status.</span></span>
-   <span data-ttu-id="242c5-128">Служба ведения журнала событий завершает операцию очистки перед получением операции записи: операция Clear усекает журнал, затем операция записи добавляет новую запись в начало журнала.</span><span class="sxs-lookup"><span data-stu-id="242c5-128">The event-logging service completes a clear operation before receiving a write operation: The clear operation truncates the log, then the write operation adds the new record at the beginning of the log.</span></span>

 

 



