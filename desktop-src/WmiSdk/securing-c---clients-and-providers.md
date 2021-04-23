---
description: Как поставщики C++, так и клиентские приложения должны выполнять многие из одних и тех же операций для обеспечения безопасности WMI.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Защита клиентов и поставщиков C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701992"
---
# <a name="securing-c-clients-and-providers"></a><span data-ttu-id="9b51d-103">Защита клиентов и поставщиков C++</span><span class="sxs-lookup"><span data-stu-id="9b51d-103">Securing C++ Clients and Providers</span></span>

<span data-ttu-id="9b51d-104">Как поставщики C++, так и клиентские приложения должны выполнять многие из одних и тех же операций для обеспечения безопасности WMI.</span><span class="sxs-lookup"><span data-stu-id="9b51d-104">Both C++ providers and client applications must perform many of the same operations to maintain WMI security.</span></span>

<span data-ttu-id="9b51d-105">Клиентские приложения должны правильно задавать [олицетворение](setting-the-default-process-security-level-using-c-.md) DCOM и уровни [проверки подлинности](setting-authentication-in-wmi.md) при подключении к WMI.</span><span class="sxs-lookup"><span data-stu-id="9b51d-105">Client applications must set DCOM [impersonation](setting-the-default-process-security-level-using-c-.md) and [authentication](setting-authentication-in-wmi.md) levels correctly when connecting to WMI.</span></span> <span data-ttu-id="9b51d-106">Обратные вызовы от [асинхронных вызовов](setting-security-on-an-asynchronous-call.md) имеют риски безопасности, поэтому клиентские приложения должны [выполнять проверки доступа](performing-access-checks.md) , чтобы обеспечить обратный вызов из надежного источника.</span><span class="sxs-lookup"><span data-stu-id="9b51d-106">Callbacks from [asynchronous calls](setting-security-on-an-asynchronous-call.md) have security risks, so client applications must [perform access checks](performing-access-checks.md) to ensure the callback is from a trusted source.</span></span> <span data-ttu-id="9b51d-107">Клиенты должны защищать как [временные, так и постоянные потребители событий](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="9b51d-107">Clients need to secure both [temporary and permanent event consumers](securing-wmi-events.md).</span></span>

<span data-ttu-id="9b51d-108">Поставщик может [выполнять проверки доступа](performing-access-checks.md) , чтобы гарантировать, что создаваемые ресурсы будут доступны только соответствующим клиентам.</span><span class="sxs-lookup"><span data-stu-id="9b51d-108">A provider may [perform access checks](performing-access-checks.md) to ensure that the resources it creates are only accessed by appropriate clients.</span></span>

<span data-ttu-id="9b51d-109">И поставщики, и клиенты также могут устанавливать безопасность для [конкретного прокси-](setting-the-security-on-iwbemservices-and-other-proxies.md) соединения.</span><span class="sxs-lookup"><span data-stu-id="9b51d-109">Both providers and clients also can set the security on a [specific proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) connection.</span></span> <span data-ttu-id="9b51d-110">Они также могут включать [привилегии](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="9b51d-110">Both can also enable [privileges](executing-privileged-operations.md).</span></span> <span data-ttu-id="9b51d-111">Поставщик событий должен гарантировать, что потребитель клиента имеет права доступа для [получения запрошенного события](providing-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="9b51d-111">An event provider must ensure that the client consumer has privileges to [receive a requested event](providing-events-securely.md).</span></span>

<span data-ttu-id="9b51d-112">Как клиенту, так и поставщику может потребоваться установить удаленное подключение, для которого требуется другая служба проверки подлинности, NTLM вместо Kerberos.</span><span class="sxs-lookup"><span data-stu-id="9b51d-112">Either a client or provider may need to make a remote connection that requires a different authentication service, NTLM instead of Kerberos for example.</span></span>

 

 



