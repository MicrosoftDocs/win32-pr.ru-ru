---
title: Настройка очереди запросов
description: Настройка очереди запросов
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888364"
---
# <a name="configuring-the-request-queue"></a>Настройка очереди запросов

При открытии или создании очереди запросов вызывающее приложение получает к нему маркер, который можно использовать для отправки запросов или настройки очереди запросов. Вызов [**хттпсетурлграуппроперти**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) с помощью **хттпсервербиндингпроперти** и указание маркера очереди запросов в структуре [**\_ \_ сведений о привязке HTTP**](/windows/desktop/api/Http/ns-http-http_binding_info) , указанной в параметре *ппропертинформатион* , связывает группу URL-адресов с очередью запросов. Свойства очереди запросов задаются только приложением, которое создает очередь запросов. Например, чтобы задать свойство Length очереди сервера, приложение Creator вызывает [**хттпсетрекуесткуеуепроперти**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) , указав **хттпсерверкуеуеленгспроперти** в параметре *Property* .

 

 




