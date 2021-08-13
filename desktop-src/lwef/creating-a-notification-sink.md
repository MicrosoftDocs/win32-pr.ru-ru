---
title: Создание приемника уведомлений
description: Создание приемника уведомлений
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf76d77e69df41b7fbd3fb83fbd232dfdfd03682d39681e1f2a4fa9f2d19ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480096"
---
# <a name="creating-a-notification-sink"></a>Создание приемника уведомлений

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

Чтобы получать уведомления о событиях агента Microsoft Agent, необходимо реализовать интерфейс [**иажентнотифисинк**](events.md)или [**иажентнотифисинкекс**](iagentnotifysinkex.md) , а также создать и зарегистрировать объект этого типа в соответствии с соглашениями com:


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



Не забывайте отменять регистрацию приемника уведомлений при завершении работы приложения и освобождении интерфейсов агента Майкрософт.

 

 




