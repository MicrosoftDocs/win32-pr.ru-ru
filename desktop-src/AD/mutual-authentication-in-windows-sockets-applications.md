---
title: взаимная проверка подлинности в приложениях Windows sockets
description: службы Microsoft Windows sockets могут использовать api регистрации и разрешения (рнр) для публикации служб или могут использовать точки подключения службы.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- взаимная проверка подлинности в приложениях Windows sockets
- Active Directory, использование, взаимная проверка подлинности в Windows приложениях сокетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a7267159f826d572a8efd101ab86338f5a24c6966b8d2af3a260e1f4af6244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025752"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>взаимная проверка подлинности в приложениях Windows sockets

службы Microsoft Windows sockets могут использовать api регистрации и разрешения (рнр) для публикации служб или могут использовать точки подключения службы.

дополнительные сведения и пример кода, демонстрирующий выполнение взаимной проверки подлинности для службы Windows sockets, которая публикуется с помощью точки подключения службы, см. [в разделе взаимная проверка подлинности в службе сокетов Windows с SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md). В этом примере кода используется пакет безопасности SSPI для управления согласованиями проверки подлинности между клиентом и службой WinSock.

Служба WinSock РНР может использовать аналогичный код для выполнения взаимной проверки подлинности с помощью пакета SSPI. В этом случае служба будет составлять свои имена участников-служб, используя различающееся имя записи службы в контейнере Винсокксервицес в каталоге.

Например, если служба регистрирует себя с именем «Винсоккрнрсамплесервице», имя SPN службы сопоставлено со следующим различающимся именем:


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




