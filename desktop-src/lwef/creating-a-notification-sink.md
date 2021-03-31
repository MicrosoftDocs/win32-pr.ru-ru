---
title: Создание приемника уведомлений
description: Создание приемника уведомлений
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481cdd754e545ef87e3c0dc44324d46e48baf044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411363"
---
# <a name="creating-a-notification-sink"></a>Создание приемника уведомлений

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Чтобы получать уведомления о событиях агента Microsoft Agent, необходимо реализовать интерфейс [**иажентнотифисинк**](events.md)или [**иажентнотифисинкекс**](iagentnotifysinkex.md) , а также создать и зарегистрировать объект этого типа в соответствии с соглашениями com:


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



Не забывайте отменять регистрацию приемника уведомлений при завершении работы приложения и освобождении интерфейсов агента Майкрософт.

 

 




