---
title: Создание клиентами SPN службы
description: Для проверки подлинности службы клиентское приложение формирует имя субъекта-службы для экземпляра службы, к которому она должна подключиться.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Как клиенты составлять AD SPN службы
- имя субъекта-службы AD, как клиенты составлять SPN службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986145"
---
# <a name="how-clients-compose-a-services-spn"></a><span data-ttu-id="5ded5-105">Создание клиентами SPN службы</span><span class="sxs-lookup"><span data-stu-id="5ded5-105">How Clients Compose a Service's SPN</span></span>

<span data-ttu-id="5ded5-106">Для проверки подлинности службы клиентское приложение формирует имя субъекта-службы для экземпляра службы, к которому она должна подключиться.</span><span class="sxs-lookup"><span data-stu-id="5ded5-106">To authenticate a service, a client application composes an SPN for the service instance to which it must connect.</span></span> <span data-ttu-id="5ded5-107">Клиентское приложение может использовать функцию [**дсмакеспн**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) для создания имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="5ded5-107">The client application can use the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function to compose an SPN.</span></span> <span data-ttu-id="5ded5-108">Клиент указывает компоненты имени субъекта-службы, используя известные данные или данные, полученные из источников, отличных от самой службы.</span><span class="sxs-lookup"><span data-stu-id="5ded5-108">The client specifies the components of the SPN using known data or data retrieved from sources other than the service itself.</span></span>

<span data-ttu-id="5ded5-109">Форма имени субъекта-службы, как показано в следующей форме:</span><span class="sxs-lookup"><span data-stu-id="5ded5-109">The form of an SPN is as shown in the following form:</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="5ded5-110">В этой форме требуются " &lt; класс службы &gt; " и " &lt; узел &gt; ".</span><span class="sxs-lookup"><span data-stu-id="5ded5-110">In this form, "&lt;service class&gt;" and "&lt;host&gt;" are required.</span></span> <span data-ttu-id="5ded5-111">" &lt; Port &gt; " и " &lt; Service Name &gt; " необязательно.</span><span class="sxs-lookup"><span data-stu-id="5ded5-111">"&lt;port&gt;" and "&lt;service name&gt;" optional.</span></span>

<span data-ttu-id="5ded5-112">Как правило, клиент распознает &lt; часть имени "класс службы &gt; " и определяет, какие из дополнительных компонентов следует включить в имя участника-службы.</span><span class="sxs-lookup"><span data-stu-id="5ded5-112">Typically, the client recognizes the "&lt;service class&gt;" part of the name, and recognizes which of the optional components to include in the SPN.</span></span> <span data-ttu-id="5ded5-113">Клиент может получать компоненты имени субъекта-службы из таких источников, как точка подключения службы (SCP) или входные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ded5-113">The client can retrieve components of the SPN from sources such as a service connection point (SCP) or user input.</span></span> <span data-ttu-id="5ded5-114">Например, клиент может прочитать атрибут **SERVICEDNSNAME** SCP службы, чтобы получить &lt; компонент "host &gt; ".</span><span class="sxs-lookup"><span data-stu-id="5ded5-114">For example, the client can read the **serviceDNSName** attribute of a service's SCP to get the "&lt;host&gt;" component.</span></span> <span data-ttu-id="5ded5-115">Атрибут **serviceDNSName** содержит либо DNS-имя сервера, на котором работает экземпляр службы, либо DNS-имя записей SRV, содержащих данные узла для реплик службы.</span><span class="sxs-lookup"><span data-stu-id="5ded5-115">The **serviceDNSName** attribute contains either the DNS name of the server on which the service instance is running or the DNS name of SRV records containing the host data for service replicas.</span></span> <span data-ttu-id="5ded5-116">&lt;Компонент Service Name &gt; , используемый только для реплицируемых служб, может быть РАЗЛИЧАЮЩИМСЯ именем SCP службы, DNS-именем домена, обслуживаемого службой, или DNS-именем записей SRV или MX.</span><span class="sxs-lookup"><span data-stu-id="5ded5-116">The "&lt;service name&gt;" component, used only for replicable services, can be the distinguished name of the service's SCP, the DNS name of the domain served by the service, or the DNS name of SRV or MX records.</span></span>

<span data-ttu-id="5ded5-117">Дополнительные сведения и пример кода, используемый для составления имени субъекта-службы, см. в разделе [как клиент проверяет подлинность службы сокетов Windows на основе SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span><span class="sxs-lookup"><span data-stu-id="5ded5-117">For more information and a code example used to compose an SPN for a service, see [How a Client Authenticates an SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span></span>

<span data-ttu-id="5ded5-118">Дополнительные сведения и описание компонентов имени субъекта-службы см. в разделе [форматы имен для уникальных имен участников-служб](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="5ded5-118">For more information and a description of the SPN components, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

 

 




