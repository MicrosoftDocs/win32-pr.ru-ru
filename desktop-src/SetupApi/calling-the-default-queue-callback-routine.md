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
# <a name="calling-the-default-queue-callback-routine"></a>Вызов подпрограммы обратного вызова очереди по умолчанию

Если подпрограммы обратного вызова очереди по умолчанию инициализированы и заданы при вызове [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , очередь вызывает подпрограммы обратного вызова очереди по умолчанию, и вам не нужно ничего делать.

При создании подпрограммы обратного вызова фильтра, которая использует подсистему обратного вызова очереди по умолчанию для выполнения подмножества уведомлений очереди, подсистема обратного вызова фильтра должна вызывать [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) явным образом.

> [!IMPORTANT]
> При явном вызове [**сетупдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) необходимо передать указатель void, возвращенный либо [**Сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) , либо [**сетупинитдефаулткуеуекаллбаккекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).

 

> [!Note]  
> Один из способов сделать это — создать структуру контекста для пользовательской подпрограммы обратного вызова, которая включает в себя в качестве одного из членов указатель void, возвращенный [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) или [**сетупинитдефаулткуеуекаллбаккекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).

 

 

 



