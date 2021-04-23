---
description: Если подпрограммы обратного вызова очереди по умолчанию инициализированы и заданы при вызове Сетупкоммитфилекуеуе, очередь вызывает подпрограммы обратного вызова очереди по умолчанию, и вам не нужно ничего делать.
ms.assetid: a976c275-f128-490d-a544-efbfc6fd87f4
title: Вызов подпрограммы обратного вызова очереди по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24449fc1fcd92d8041de6f104092f45925a495b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664534"
---
# <a name="calling-the-default-queue-callback-routine"></a><span data-ttu-id="263ee-103">Вызов подпрограммы обратного вызова очереди по умолчанию</span><span class="sxs-lookup"><span data-stu-id="263ee-103">Calling the Default Queue Callback Routine</span></span>

<span data-ttu-id="263ee-104">Если подпрограммы обратного вызова очереди по умолчанию инициализированы и заданы при вызове [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , очередь вызывает подпрограммы обратного вызова очереди по умолчанию, и вам не нужно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="263ee-104">If the default queue callback routine is initialized and specified when [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) is called, the queue calls the default queue callback routine internally and you need do nothing more.</span></span>

<span data-ttu-id="263ee-105">При создании подпрограммы обратного вызова фильтра, которая использует подсистему обратного вызова очереди по умолчанию для выполнения подмножества уведомлений очереди, подсистема обратного вызова фильтра должна вызывать [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) явным образом.</span><span class="sxs-lookup"><span data-stu-id="263ee-105">If you create a filter callback routine that relies on the default queue callback routine to handle a subset of the queue notifications, your filter callback routine must call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="263ee-106">При явном вызове [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) необходимо передать указатель void, возвращенный либо [**Сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) , либо [**сетупинитдефаулткуеуекаллбаккекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="263ee-106">When you call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly, you must pass in the void pointer returned by either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

> [!Note]  
> <span data-ttu-id="263ee-107">Один из способов сделать это — создать структуру контекста для пользовательской подпрограммы обратного вызова, которая включает в себя в качестве одного из членов указатель void, возвращенный [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) или [**сетупинитдефаулткуеуекаллбаккекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="263ee-107">One way to do this is to create a context structure for your custom callback routine that includes as one of its members the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

 

 



