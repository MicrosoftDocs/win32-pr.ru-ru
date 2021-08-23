---
description: После фиксации очереди путем вызова Сетупкоммитфилекуеуе она начнет обрабатывать операции, поставленные в очередь. На каждом шаге очередь отправляет уведомление в подпрограммы обратного вызова, указанную в вызове Сетупкоммитфилекуеуе.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Уведомления в очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06858eeb5c6e9abe200792f83edcc83503270ed2706450d35ef36d5dddc80d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665494"
---
# <a name="queue-notifications"></a>Уведомления в очереди

После фиксации очереди путем вызова [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)она начнет обрабатывать операции, поставленные в очередь. На каждом шаге очередь отправляет уведомление в подпрограммы обратного вызова, указанную в вызове **сетупкоммитфилекуеуе**.

Ниже приведен синтаксис, который [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) использует для отправки уведомления в подпрограммы обратного вызова.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

Значения *param1* и *Param2* содержат дополнительные сведения, относящиеся к уведомлению, отправляемому в подпрограммы обратного вызова. Каждое уведомление, его значения *param1* и *Param2* , а также то, как подпрограммы обратного вызова очереди по умолчанию обрабатывают это уведомление, подробно описывается в разделе [уведомления о очереди файлов](file-queue-notifications.md).

 

 



