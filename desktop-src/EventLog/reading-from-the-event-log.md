---
description: Приложение "Просмотр событий" использует функцию Опеневентлог, чтобы открыть журнал событий для источника событий.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Чтение из журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080626"
---
# <a name="reading-from-the-event-log"></a><span data-ttu-id="076bf-103">Чтение из журнала событий</span><span class="sxs-lookup"><span data-stu-id="076bf-103">Reading from the Event Log</span></span>

<span data-ttu-id="076bf-104">Приложение "Просмотр событий" использует функцию [**опеневентлог**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) , чтобы открыть журнал событий для источника событий.</span><span class="sxs-lookup"><span data-stu-id="076bf-104">An event viewer application uses the [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to open the event log for an event source.</span></span> <span data-ttu-id="076bf-105">Затем средство просмотра событий может использовать функцию [**реадевентлог**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) для чтения записей событий из журнала.</span><span class="sxs-lookup"><span data-stu-id="076bf-105">The event viewer can then use the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to read event records from the log.</span></span> <span data-ttu-id="076bf-106">**Реадевентлог** возвращает буфер, содержащий структуру [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) , и дополнительные сведения, описывающие зарегистрированное событие.</span><span class="sxs-lookup"><span data-stu-id="076bf-106">**ReadEventLog** returns a buffer containing an [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure and additional information that describes a logged event.</span></span> <span data-ttu-id="076bf-107">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="076bf-107">The following diagram illustrates this process.</span></span>

![чтение из журнала событий](images/readlog.png)

<span data-ttu-id="076bf-109">Пример кода см. в разделе [запросы сведений о событиях](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="076bf-109">For example code, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



