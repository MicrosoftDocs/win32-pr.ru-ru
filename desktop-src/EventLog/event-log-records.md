---
description: Сведения о каждом событии хранятся в журнале событий в записи журнала событий. Запись журнала событий включает сведения о времени, типе и категории. Дополнительные сведения см. в разделе Структура EVENTLOGRECORD.
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: Записи журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908867"
---
# <a name="event-log-records"></a><span data-ttu-id="e73f8-105">Записи журнала событий</span><span class="sxs-lookup"><span data-stu-id="e73f8-105">Event Log Records</span></span>

<span data-ttu-id="e73f8-106">Сведения о каждом событии хранятся в журнале событий в *записи журнала событий*.</span><span class="sxs-lookup"><span data-stu-id="e73f8-106">Information about each event is stored in the event log in an *event log record*.</span></span> <span data-ttu-id="e73f8-107">Запись журнала событий включает сведения о времени, типе и категории.</span><span class="sxs-lookup"><span data-stu-id="e73f8-107">The event log record includes time, type, and category information.</span></span> <span data-ttu-id="e73f8-108">Дополнительные сведения см. в разделе Структура [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="e73f8-108">For more information, see the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure.</span></span>

<span data-ttu-id="e73f8-109">Элемент **RecordNumber** элемента [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) содержит номер записи для записи журнала событий.</span><span class="sxs-lookup"><span data-stu-id="e73f8-109">The **RecordNumber** member of [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contains the record number for the event log record.</span></span> <span data-ttu-id="e73f8-110">Самой первой записью, записанной в журнал событий, является номер записи 1, а другие записи нумеруются последовательно.</span><span class="sxs-lookup"><span data-stu-id="e73f8-110">The very first record written to an event log is record number 1, and other records are numbered sequentially.</span></span> <span data-ttu-id="e73f8-111">Если номер записи достигает значения ULONG \_ Max, номер следующей записи будет равен 0, а не 1, однако для поиска записи можно использовать нуль.</span><span class="sxs-lookup"><span data-stu-id="e73f8-111">If the record number reaches ULONG\_MAX, the next record number will be 0, not 1; however, you use zero to seek to the record.</span></span>

<span data-ttu-id="e73f8-112">Если для параметра реестра [retention](eventlog-key.md) установлено значение 0, записи о событиях будут перезаписаны по достижении максимального размера журнала.</span><span class="sxs-lookup"><span data-stu-id="e73f8-112">If the [Retention](eventlog-key.md) registry value is set to zero, the event records are overwritten when the maximum log size is reached.</span></span> <span data-ttu-id="e73f8-113">Поэтому самая старая запись в журнале событий может не быть записью с номером 1.</span><span class="sxs-lookup"><span data-stu-id="e73f8-113">Therefore, the oldest record in an event log may not be record number 1.</span></span> <span data-ttu-id="e73f8-114">Чтобы найти самую старую запись в журнале, вызовите функцию [**жетолдестевентлогрекорд**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="e73f8-114">To identify the oldest record in the log, call the [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) function.</span></span> <span data-ttu-id="e73f8-115">Затем можно вызвать функцию [**жетнумберофевентлогрекордс**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) и добавить возвращаемое значение к самому старому номеру записи, чтобы определить самую новую запись.</span><span class="sxs-lookup"><span data-stu-id="e73f8-115">You can then call the [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) function and add the returned value to the oldest record number to determine the newest record.</span></span>

<span data-ttu-id="e73f8-116">Вы можете считывать отдельные записи из журнала событий с помощью функции [**реадевентлог**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) .</span><span class="sxs-lookup"><span data-stu-id="e73f8-116">You can read individual records from the event log using the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function.</span></span> <span data-ttu-id="e73f8-117">Дополнительные сведения см. в разделе [запросы сведений о событиях](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="e73f8-117">For more information, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



