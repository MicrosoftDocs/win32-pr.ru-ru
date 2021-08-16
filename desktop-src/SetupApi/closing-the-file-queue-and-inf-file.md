---
description: После того как очередь завершит фиксацию своих операций, ее следует закрыть с помощью функции Сетупклосефилекуеуе с маркером, созданным Сетупопенфилекуеуе.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Закрытие файловой очереди и INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce5c81c75f7515acfb346b4277e416b0cb2c2a9be6e40464dcfdfc21c3b23bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887579"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Закрытие файловой очереди и INF-файла

После того как очередь завершит фиксацию своих операций, ее следует закрыть с помощью функции [**сетупклосефилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) с маркером, созданным [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue). Обратный вызов очереди по умолчанию должен быть уничтожен и создан повторно, прежде чем можно будет зафиксировать другую очередь.

Если контекст по умолчанию был инициирован для использования подпрограммы обратного вызова по умолчанию, он также должен быть завершен путем вызова функции [**сетуптермдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) . *Контекст* является указателем на структуру, возвращаемую функцией [**сетупинитдефаулткуеуекаллбакк**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .

Если доступ к данным INF больше не требуется, вызовите функцию [**сетупклосеинффиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) с маркером, созданным [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) для освобождения системных ресурсов.

 

 



