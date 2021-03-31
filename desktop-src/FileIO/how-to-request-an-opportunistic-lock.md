---
description: Для запроса уступающей блокировки сначала открывается файл с разрешениями и флагами, соответствующими приложению, открывающему файл. Все файлы, для которых будут запрошены уступающей блокировки, должны быть открыты для перекрывающихся (асинхронных) операций.
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Как запросить уступающую блокировку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912856"
---
# <a name="how-to-request-an-opportunistic-lock"></a><span data-ttu-id="c222b-104">Как запросить уступающую блокировку</span><span class="sxs-lookup"><span data-stu-id="c222b-104">How to Request an Opportunistic Lock</span></span>

<span data-ttu-id="c222b-105">Клиентские приложения напрямую запрашивают уступающей блокировку только в том случае, если блокировка предназначена для файла на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="c222b-105">Client applications directly request opportunistic locks only when the lock is intended for a file on the local server.</span></span> <span data-ttu-id="c222b-106">При доступе к файлам на удаленных серверах это перенаправитель сети, а не клиентское приложение, которое запрашивает уступающую блокировку с удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="c222b-106">When accessing files on remote servers, it is the network redirector, and not the client application, that requests the opportunistic lock from the remote server.</span></span>

<span data-ttu-id="c222b-107">Для запроса уступающей блокировки сначала открывается файл с разрешениями и флагами, соответствующими приложению, открывающему файл.</span><span class="sxs-lookup"><span data-stu-id="c222b-107">Opportunistic locks are requested by first opening a file with permissions and flags appropriate to the application opening the file.</span></span> <span data-ttu-id="c222b-108">Все файлы, для которых будут запрошены уступающей блокировки, должны быть открыты для перекрывающихся (асинхронных) операций.</span><span class="sxs-lookup"><span data-stu-id="c222b-108">All files for which opportunistic locks will be requested must be opened for overlapped (asynchronous) operation.</span></span> <span data-ttu-id="c222b-109">После открытия файлов для выполнения операции перекрытия Используйте функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) с соответствующим управляющим кодом для запроса уступающей блокировки.</span><span class="sxs-lookup"><span data-stu-id="c222b-109">After the files are opened for overlapped operation, use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the appropriate control code to request an opportunistic lock.</span></span> <span data-ttu-id="c222b-110">Список операций оппортунистической блокировки см. в разделе [операции оппортунистической блокировки](opportunistic-lock-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c222b-110">For a list of the opportunistic lock operations, see [Opportunistic Lock Operations](opportunistic-lock-operations.md).</span></span>

<span data-ttu-id="c222b-111">Приложения получают уведомления о разрыве оппортунистической блокировки с помощью члена **Хевент** [**перекрывающейся**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) структуры, связанной с файлом.</span><span class="sxs-lookup"><span data-stu-id="c222b-111">Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the file.</span></span> <span data-ttu-id="c222b-112">Приложения также могут использовать такие функции, как [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) и [**хасоверлаппедиокомплетед**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span><span class="sxs-lookup"><span data-stu-id="c222b-112">Applications may also use functions such as [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) and [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span></span> <span data-ttu-id="c222b-113">Приложение отвечает за сопоставление правильного файла с поврежденной оппортунистической блокировкой.</span><span class="sxs-lookup"><span data-stu-id="c222b-113">The application is responsible for associating the correct file with the broken opportunistic lock.</span></span>

<span data-ttu-id="c222b-114">Дополнительные сведения об уведомлении см. в разделе [Синхронизация](/windows/desktop/Sync/synchronization).</span><span class="sxs-lookup"><span data-stu-id="c222b-114">For more information on notification, see [Synchronization](/windows/desktop/Sync/synchronization).</span></span>

 

 
