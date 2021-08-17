---
title: Настройка очереди запросов
description: Настройка очереди запросов
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08a8f931d8875fda43b485bada93d2bf5291d0d2b90e85c8b31bd631e8c7fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014932"
---
# <a name="configuring-the-request-queue"></a>Настройка очереди запросов

При открытии или создании очереди запросов вызывающее приложение получает к нему маркер, который можно использовать для отправки запросов или настройки очереди запросов. Вызов [**хттпсетурлграуппроперти**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) с помощью **хттпсервербиндингпроперти** и указание маркера очереди запросов в структуре [**\_ \_ сведений о привязке HTTP**](/windows/desktop/api/Http/ns-http-http_binding_info) , указанной в параметре *ппропертинформатион* , связывает группу URL-адресов с очередью запросов. Свойства очереди запросов задаются только приложением, которое создает очередь запросов. Например, чтобы задать свойство Length очереди сервера, приложение Creator вызывает [**хттпсетрекуесткуеуепроперти**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) , указав **хттпсерверкуеуеленгспроперти** в параметре *Property* .

 

 




