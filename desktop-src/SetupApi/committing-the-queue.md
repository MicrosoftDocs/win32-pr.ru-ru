---
description: Если функция обратного вызова по умолчанию будет вызываться во время фиксации очереди, ее контекст должен быть инициализирован с помощью функций Сетупинитдефаулткуеуекаллбакк или Сетупинитдефаулткуеуекаллбаккекс.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Фиксация очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67c19b91cc25e5107f91fbd241d96147137a38b8544568e57ea3bbbd58981a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887525"
---
# <a name="committing-the-queue"></a>Фиксация очереди

Если функция обратного вызова по умолчанию будет вызываться во время фиксации очереди, ее контекст должен быть инициализирован с помощью функций [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) или [**сетупинитдефаулткуеуекаллбаккекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) . Если вы используете пользовательскую функцию обратного вызова, которая никогда не вызывает функцию обратного вызова по умолчанию, этот шаг не требуется.

После сборки очереди и инициализации функции обратного вызова, которая будет обрабатывать уведомления очереди, можно вызвать [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , чтобы зафиксировать операции, которые были поставлены в очередь.

В следующем примере [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) используется для фиксации очереди с помощью подпрограммы обратного вызова по умолчанию.

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

В предыдущем примере MyQueue — очередь для фиксации, Овнервиндов — это окно, которое будет владеть любыми диалоговыми окнами, созданными подпрограммыми обратного вызова по умолчанию, Сетупдефаулткуеуекаллбакк указывает, что будет использоваться функция обратного вызова по умолчанию, а *контекст* — это указатель на структуру, возвращенную предыдущим вызовом [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).

 

 



