---
description: Разбиение уступающей блокировки — это процесс снижения блокировки, которую один клиент имеет на файл, чтобы другой клиент мог открыть файл с оппортунистической блокировкой или без нее.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Разбиение уступающей блокировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a29b6bd36d8c000b5288ea2408897415547c802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664440"
---
# <a name="breaking-opportunistic-locks"></a><span data-ttu-id="fe5ab-103">Разбиение уступающей блокировки</span><span class="sxs-lookup"><span data-stu-id="fe5ab-103">Breaking Opportunistic Locks</span></span>

<span data-ttu-id="fe5ab-104">Разбиение уступающей блокировки — это процесс снижения блокировки, которую один клиент имеет на файл, чтобы другой клиент мог открыть файл с оппортунистической блокировкой или без нее.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-104">Breaking an opportunistic lock is the process of degrading the lock that one client has on a file so that another client can open the file, with or without an opportunistic lock.</span></span> <span data-ttu-id="fe5ab-105">Когда другой клиент запрашивает операцию открытия, сервер задерживает операцию открытия и уведомляет клиента о том, что он владеет оппортунистической блокировкой.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-105">When the other client requests the open operation, the server delays the open operation and notifies the client holding the opportunistic lock.</span></span>

<span data-ttu-id="fe5ab-106">Клиент, удерживающий блокировку, принимает действия, соответствующие типу блокировки, например, отменяя буферы чтения, закрывая файл и т. д.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-106">The client holding the lock then takes actions appropriate to the type of lock, for example abandoning read buffers, closing the file, and so on.</span></span> <span data-ttu-id="fe5ab-107">Только когда клиент, удерживающий уступающую блокировку, уведомляет сервер о том, что он выполняется, сервер открывает файл для клиента, запрашивающего операцию открытия.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-107">Only when the client holding the opportunistic lock notifies the server that it is done does the server open the file for the client requesting the open operation.</span></span> <span data-ttu-id="fe5ab-108">Однако при разрыве блокировки уровня 2 сервер сообщает клиенту, что он был разорван, но не ждет подтверждения, так как кэшированные данные для записи на сервер не записываются.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-108">However, when a level 2 lock is broken, the server reports to the client that it has been broken but does not wait for any acknowledgment, as there is no cached data to be flushed to the server.</span></span>

<span data-ttu-id="fe5ab-109">При подтверждении разрыва любой монопольной блокировки (фильтра, уровня 1 или пакета) владелец поврежденной блокировки не может запросить другую монопольную блокировку.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-109">In acknowledging a break of any exclusive lock (filter, level 1, or batch), the holder of a broken lock cannot request another exclusive lock.</span></span> <span data-ttu-id="fe5ab-110">Она может понизить монопольную блокировку до блокировки уровня 2 или вообще без блокировки.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-110">It can degrade an exclusive lock to a level 2 lock or no lock at all.</span></span> <span data-ttu-id="fe5ab-111">Держатель, как правило, снимает блокировку и закрывает файл, когда все собирается закрыть файл.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-111">The holder typically releases the lock and closes the file when it is about to close the file anyway.</span></span>

<span data-ttu-id="fe5ab-112">Приложения получают уведомления о том, что оппортунистическая блокировка разбивается с помощью члена **Хевент** [**перекрывающейся**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) структуры, связанной с файлом, на котором блокировка была нарушена.</span><span class="sxs-lookup"><span data-stu-id="fe5ab-112">Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the file on which the lock is broken.</span></span> <span data-ttu-id="fe5ab-113">Приложения также могут использовать такие функции, как [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) и [**хасоверлаппедиокомплетед**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span><span class="sxs-lookup"><span data-stu-id="fe5ab-113">Applications may also use functions such as [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) and [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span></span>

 

 
