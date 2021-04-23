---
description: После фиксации очереди путем вызова Сетупкоммитфилекуеуе она начнет обрабатывать операции, поставленные в очередь. На каждом шаге очередь отправляет уведомление в подпрограммы обратного вызова, указанную в вызове Сетупкоммитфилекуеуе.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Уведомления в очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842a3ebc82640789fdb6e730e881d6790a0d642b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664086"
---
# <a name="queue-notifications"></a><span data-ttu-id="ea53f-104">Уведомления в очереди</span><span class="sxs-lookup"><span data-stu-id="ea53f-104">Queue Notifications</span></span>

<span data-ttu-id="ea53f-105">После фиксации очереди путем вызова [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)она начнет обрабатывать операции, поставленные в очередь.</span><span class="sxs-lookup"><span data-stu-id="ea53f-105">After a queue is committed by calling [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), it will begin to process the queued operations.</span></span> <span data-ttu-id="ea53f-106">На каждом шаге очередь отправляет уведомление в подпрограммы обратного вызова, указанную в вызове **сетупкоммитфилекуеуе**.</span><span class="sxs-lookup"><span data-stu-id="ea53f-106">At each step, the queue sends a notification to the callback routine specified in the call to **SetupCommitFileQueue**.</span></span>

<span data-ttu-id="ea53f-107">Ниже приведен синтаксис, который [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) использует для отправки уведомления в подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ea53f-107">Following is the syntax that [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

<span data-ttu-id="ea53f-108">Значения *param1* и *Param2* содержат дополнительные сведения, относящиеся к уведомлению, отправляемому в подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ea53f-108">The values of *Param1* and *Param2* contain additional information relevant to the notification being sent to the callback routine.</span></span> <span data-ttu-id="ea53f-109">Каждое уведомление, его значения *param1* и *Param2* , а также то, как подпрограммы обратного вызова очереди по умолчанию обрабатывают это уведомление, подробно описывается в разделе [уведомления о очереди файлов](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ea53f-109">Each notification, its *Param1* and *Param2* values, and how the default queue callback routine handles that notification, is described in detail in [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 



