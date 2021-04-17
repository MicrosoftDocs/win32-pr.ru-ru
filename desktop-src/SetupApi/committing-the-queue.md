---
description: Если функция обратного вызова по умолчанию будет вызываться во время фиксации очереди, ее контекст должен быть инициализирован с помощью функций Сетупинитдефаулткуеуекаллбакк или Сетупинитдефаулткуеуекаллбаккекс.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Фиксация очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663517"
---
# <a name="committing-the-queue"></a><span data-ttu-id="5d7d7-103">Фиксация очереди</span><span class="sxs-lookup"><span data-stu-id="5d7d7-103">Committing the Queue</span></span>

<span data-ttu-id="5d7d7-104">Если функция обратного вызова по умолчанию будет вызываться во время фиксации очереди, ее контекст должен быть инициализирован с помощью функций [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) или [**сетупинитдефаулткуеуекаллбаккекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) .</span><span class="sxs-lookup"><span data-stu-id="5d7d7-104">If the default callback function is going to be called during the queue commitment, the context for it must be initialized using the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) functions.</span></span> <span data-ttu-id="5d7d7-105">Если вы используете пользовательскую функцию обратного вызова, которая никогда не вызывает функцию обратного вызова по умолчанию, этот шаг не требуется.</span><span class="sxs-lookup"><span data-stu-id="5d7d7-105">If you are using a custom callback function that never calls the default callback function, this step is not necessary.</span></span>

<span data-ttu-id="5d7d7-106">После сборки очереди и инициализации функции обратного вызова, которая будет обрабатывать уведомления очереди, можно вызвать [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , чтобы зафиксировать операции, которые были поставлены в очередь.</span><span class="sxs-lookup"><span data-stu-id="5d7d7-106">After the queue is built and the callback function that will process queue notifications has been initialized, you can call [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the operations that have been enqueued.</span></span>

<span data-ttu-id="5d7d7-107">В следующем примере [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) используется для фиксации очереди с помощью подпрограммы обратного вызова по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5d7d7-107">The following example uses [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the queue using the default callback routine.</span></span>

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

<span data-ttu-id="5d7d7-108">В предыдущем примере MyQueue — очередь для фиксации, Овнервиндов — это окно, которое будет владеть любыми диалоговыми окнами, созданными подпрограммыми обратного вызова по умолчанию, Сетупдефаулткуеуекаллбакк указывает, что будет использоваться функция обратного вызова по умолчанию, а *контекст* — это указатель на структуру, возвращенную предыдущим вызовом [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span><span class="sxs-lookup"><span data-stu-id="5d7d7-108">In the preceding example, MyQueue is the queue to commit, OwnerWindow is the window that will own any dialog boxes created by the default callback routine, SetupDefaultQueueCallback specifies that the default callback function will be used, and *Context* is a pointer to the structure returned by the previous call to [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span></span>

 

 



