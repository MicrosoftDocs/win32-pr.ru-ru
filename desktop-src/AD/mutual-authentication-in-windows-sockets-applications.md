---
title: Взаимная проверка подлинности в приложениях Windows Sockets
description: Службы сокетов Microsoft Windows могут использовать API регистрации и разрешения (РНР) для публикации служб или могут использовать точки подключения службы.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Взаимная проверка подлинности в приложениях Windows Sockets
- Active Directory, использование, взаимная проверка подлинности в приложениях Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252771"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a><span data-ttu-id="ce79c-105">Взаимная проверка подлинности в приложениях Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="ce79c-105">Mutual Authentication in Windows Sockets Applications</span></span>

<span data-ttu-id="ce79c-106">Службы сокетов Microsoft Windows могут использовать API регистрации и разрешения (РНР) для публикации служб или могут использовать точки подключения службы.</span><span class="sxs-lookup"><span data-stu-id="ce79c-106">Microsoft Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services, or they can use service connection points.</span></span>

<span data-ttu-id="ce79c-107">Дополнительные сведения и пример кода, в котором показано, как выполнить взаимную проверку подлинности для службы сокетов Windows, которая публикуется с помощью точки подключения службы, см. [в статье взаимная проверка подлинности в службе сокетов Windows с SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="ce79c-107">For more information and a code example that shows how to perform mutual authentication for a Windows Sockets service that publishes using a service connection point, see [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span></span> <span data-ttu-id="ce79c-108">В этом примере кода используется пакет безопасности SSPI для управления согласованиями проверки подлинности между клиентом и службой WinSock.</span><span class="sxs-lookup"><span data-stu-id="ce79c-108">This code example uses an SSPI security package to manage the authentication negotiations between a client and the WinSock service.</span></span>

<span data-ttu-id="ce79c-109">Служба WinSock РНР может использовать аналогичный код для выполнения взаимной проверки подлинности с помощью пакета SSPI.</span><span class="sxs-lookup"><span data-stu-id="ce79c-109">A WinSock RnR service can use similar code to perform mutual authentication using an SSPI package.</span></span> <span data-ttu-id="ce79c-110">В этом случае служба будет составлять свои имена участников-служб, используя различающееся имя записи службы в контейнере Винсокксервицес в каталоге.</span><span class="sxs-lookup"><span data-stu-id="ce79c-110">In this case, the service would compose its SPNs using the distinguished name of the service's entry in the WinsockServices container in the directory.</span></span>

<span data-ttu-id="ce79c-111">Например, если служба регистрирует себя с именем «Винсоккрнрсамплесервице», имя SPN службы сопоставлено со следующим различающимся именем:</span><span class="sxs-lookup"><span data-stu-id="ce79c-111">For example, if the service registers itself with the name "WinSockRnRSampleService", you would compose the service's SPN from the following distinguished name:</span></span>


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




