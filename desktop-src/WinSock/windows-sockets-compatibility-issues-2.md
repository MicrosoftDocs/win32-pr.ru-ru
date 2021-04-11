---
description: Сокеты Windows 2 продолжат поддерживать все семантики 1,1 сокетов Windows и вызовы функций, за исключением тех, которые работают с псевдо-блокировкой.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Проблемы совместимости с сокетами Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263468"
---
# <a name="windows-sockets-compatibility-issues"></a><span data-ttu-id="a70d3-103">Проблемы совместимости с сокетами Windows</span><span class="sxs-lookup"><span data-stu-id="a70d3-103">Windows Sockets Compatibility Issues</span></span>

<span data-ttu-id="a70d3-104">Сокеты Windows 2 продолжат поддерживать все семантики 1,1 сокетов Windows и вызовы функций, за исключением тех, которые работают с псевдо-блокировкой.</span><span class="sxs-lookup"><span data-stu-id="a70d3-104">Windows Sockets 2 continues to support all of the Windows Sockets 1.1 semantics and function calls except for those dealing with pseudo-blocking.</span></span> <span data-ttu-id="a70d3-105">Так как сокеты Windows 2 выполняются только в 32-разрядных, запланированных для использования средах с вытеснением, нет необходимости реализовывать псевдо-блокировку, найденную в Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="a70d3-105">Since Windows Sockets 2 runs only in 32-bit, preemptively scheduled environments, there is no need to implement the pseudo-blocking found in Windows Sockets 1.1.</span></span> <span data-ttu-id="a70d3-106">Это означает, что код ошибки ВСАЕИНПРОГРЕСС никогда не будет указан и следующие функции 1,1 сокетов Windows недоступны для приложений Windows Sockets 2:</span><span class="sxs-lookup"><span data-stu-id="a70d3-106">This means that the WSAEINPROGRESS error code will never be indicated and that the following Windows Sockets 1.1 functions are not available to Windows Sockets 2 applications:</span></span>

-   <span data-ttu-id="a70d3-107">всаканцелблоккингкалл</span><span class="sxs-lookup"><span data-stu-id="a70d3-107">WSACancelBlockingCall</span></span>
-   <span data-ttu-id="a70d3-108">всаисблоккинг</span><span class="sxs-lookup"><span data-stu-id="a70d3-108">WSAIsBlocking</span></span>
-   <span data-ttu-id="a70d3-109">всасетблоккингхук</span><span class="sxs-lookup"><span data-stu-id="a70d3-109">WSASetBlockingHook</span></span>
-   <span data-ttu-id="a70d3-110">всаунхукблоккингхук</span><span class="sxs-lookup"><span data-stu-id="a70d3-110">WSAUnhookBlockingHook</span></span>

<span data-ttu-id="a70d3-111">Программы Windows Sockets 1,1, написанные для использования псевдо-блокировки, будут работать правильно, так как они связаны с Winsock.dll или Wsock32.dll.</span><span class="sxs-lookup"><span data-stu-id="a70d3-111">Windows Sockets 1.1 programs that are written to utilize pseudo-blocking will continue to operate correctly since they link to either Winsock.dll or Wsock32.dll.</span></span> <span data-ttu-id="a70d3-112">Оба варианта продолжают поддерживать полный набор функций 1,1 сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="a70d3-112">Both continue to support the complete set of Windows Sockets 1.1 functions.</span></span> <span data-ttu-id="a70d3-113">Чтобы программы могли стать приложениями Windows Sockets 2, необходимо внести некоторые изменения в код.</span><span class="sxs-lookup"><span data-stu-id="a70d3-113">In order for programs to become Windows Sockets 2 applications, some code modification must occur.</span></span> <span data-ttu-id="a70d3-114">В большинстве случаев разумное использование потоков можно заменить на обработку, которая была выполнена с помощью блокирующей функции-ловушки.</span><span class="sxs-lookup"><span data-stu-id="a70d3-114">In most cases, the judicious use of threads can be substituted to accommodate processing that was being accomplished with a blocking hook function.</span></span>

 

 



