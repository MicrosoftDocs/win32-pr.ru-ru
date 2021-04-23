---
title: Форматы имен для уникальных имен участников-служб
description: Имя субъекта-службы должно быть уникальным в лесу, в котором он зарегистрирован.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Форматы имен для уникальных имен SPN AD
- Имя субъекта-службы AD, форматы имен для
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252770"
---
# <a name="name-formats-for-unique-spns"></a><span data-ttu-id="47b4c-105">Форматы имен для уникальных имен участников-служб</span><span class="sxs-lookup"><span data-stu-id="47b4c-105">Name Formats for Unique SPNs</span></span>

<span data-ttu-id="47b4c-106">Имя субъекта-службы должно быть уникальным в лесу, в котором он зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="47b4c-106">An SPN must be unique in the forest in which it is registered.</span></span> <span data-ttu-id="47b4c-107">Если оно не является уникальным, проверка подлинности завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="47b4c-107">If it is not unique, authentication will fail.</span></span> <span data-ttu-id="47b4c-108">Синтаксис имени участника-службы состоит из четырех элементов: два обязательных элемента и два дополнительных элемента, которые можно использовать при необходимости для создания уникального имени, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="47b4c-108">The SPN syntax has four elements: two required elements and two additional elements that you can use, if necessary, to produce a unique name as listed in the following table.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47b4c-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="47b4c-109">Element</span></span></th>
<th><span data-ttu-id="47b4c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="47b4c-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="47b4c-111">&quot;&lt;класс службы&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="47b4c-111">&quot;&lt;service class&gt;&quot;</span></span></td>
<td><span data-ttu-id="47b4c-112">Строка, определяющая общий класс службы; Например, &quot; SQLServer &quot; .</span><span class="sxs-lookup"><span data-stu-id="47b4c-112">A string that identifies the general class of service; for example, &quot;SqlServer&quot;.</span></span> <span data-ttu-id="47b4c-113">Существуют хорошо известные имена классов служб, например &quot; www &quot; для веб-службы или &quot; LDAP &quot; для службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="47b4c-113">There are well-known service class names, such as &quot;www&quot; for a web service or &quot;ldap&quot; for a directory service.</span></span> <span data-ttu-id="47b4c-114">Как правило, это может быть любая строка, уникальная для класса службы.</span><span class="sxs-lookup"><span data-stu-id="47b4c-114">In general, this can be any string that is unique to the service class.</span></span> <span data-ttu-id="47b4c-115">Имейте в виду, что в синтаксисе имени участника-службы для разделения элементов используется косая черта (/), поэтому этот символ не может присутствовать в имени класса службы.</span><span class="sxs-lookup"><span data-stu-id="47b4c-115">Be aware that the SPN syntax uses a forward slash (/) to separate elements, so this character cannot appear in a service class name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47b4c-116">&quot;&lt;хост&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="47b4c-116">&quot;&lt;host&gt;&quot;</span></span></td>
<td><span data-ttu-id="47b4c-117">Имя компьютера, на котором запущена служба.</span><span class="sxs-lookup"><span data-stu-id="47b4c-117">The name of the computer on which the service is running.</span></span> <span data-ttu-id="47b4c-118">Это может быть полное DNS-имя или имя NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="47b4c-118">This can be a fully qualified DNS name or a NetBIOS name.</span></span> <span data-ttu-id="47b4c-119">Обратите внимание, что не гарантируется уникальность имен NetBIOS в пределах леса, поэтому имя участника-службы, которое содержит имя NetBIOS, может быть и неуникальным.</span><span class="sxs-lookup"><span data-stu-id="47b4c-119">Be aware that NetBIOS names are not guaranteed to be unique in a forest, so an SPN that contains a NetBIOS name may not be unique.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="47b4c-120">&quot;&lt;порт&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="47b4c-120">&quot;&lt;port&gt;&quot;</span></span></td>
<td><span data-ttu-id="47b4c-121">Дополнительный номер порта для различения нескольких экземпляров одного класса службы на одном хост-компьютере.</span><span class="sxs-lookup"><span data-stu-id="47b4c-121">An optional port number to differentiate between multiple instances of the same service class on a single host computer.</span></span> <span data-ttu-id="47b4c-122">Пропустите этот компонент, если служба использует порт по умолчанию для своего класса службы.</span><span class="sxs-lookup"><span data-stu-id="47b4c-122">Omit this component if the service uses the default port for its service class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47b4c-123">&quot;&lt;имя службы&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="47b4c-123">&quot;&lt;service name&gt;&quot;</span></span></td>
<td><span data-ttu-id="47b4c-124">Необязательное имя, используемое в именах SPN реплицируемой службы для обнаружения данных или служб, предоставляемых службой, или домена, обслуживаемого службой.</span><span class="sxs-lookup"><span data-stu-id="47b4c-124">An optional name used in the SPNs of a replicable service to identify the data or services provided by the service or the domain served by the service.</span></span> <span data-ttu-id="47b4c-125">Этот компонент может иметь один из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="47b4c-125">This component can have one of the following formats:</span></span>
<ul>
<li><span data-ttu-id="47b4c-126">Различающееся имя или objectGUID объекта в домен Active Directory Services, например точка подключения службы (SCP).</span><span class="sxs-lookup"><span data-stu-id="47b4c-126">The distinguished name or objectGUID of an object in Active Directory Domain Services, such as a service connection point (SCP).</span></span></li>
<li><span data-ttu-id="47b4c-127">DNS-имя домена для службы, предоставляющей указанную службу для домена в целом.</span><span class="sxs-lookup"><span data-stu-id="47b4c-127">The DNS name of the domain for a service that provides a specified service for a domain as a whole.</span></span></li>
<li><span data-ttu-id="47b4c-128">DNS-имя записи SRV или MX.</span><span class="sxs-lookup"><span data-stu-id="47b4c-128">The DNS name of an SRV or MX record.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="47b4c-129">Компоненты, представленные в SPN службы, зависят от способа идентификации и репликации службы.</span><span class="sxs-lookup"><span data-stu-id="47b4c-129">The components present in a service's SPNs depend on how the service is identified and replicated.</span></span> <span data-ttu-id="47b4c-130">Существует два основных сценария: службы на основе узла и реплицируемые службы.</span><span class="sxs-lookup"><span data-stu-id="47b4c-130">There are two basic scenarios: host-based services and replicable services.</span></span>

## <a name="host-based-services"></a><span data-ttu-id="47b4c-131">Службы на основе узла</span><span class="sxs-lookup"><span data-stu-id="47b4c-131">Host-based services</span></span>

<span data-ttu-id="47b4c-132">Для службы, размещенной на узле, &lt; компонент "имя службы &gt; " опускается, так как служба уникально идентифицируется классом службы и именем главного компьютера, на котором установлена служба.</span><span class="sxs-lookup"><span data-stu-id="47b4c-132">For a host-based service, the "&lt;service name&gt;" component is omitted because the service is uniquely identified by the service class and the name of the host computer on which the service is installed.</span></span>


```C++
<service class>/<host>
```



<span data-ttu-id="47b4c-133">Только класс службы достаточно для того, чтобы узнать клиентам, какие функции предоставляет служба.</span><span class="sxs-lookup"><span data-stu-id="47b4c-133">The service class alone is sufficient to identify for clients the features that the service provides.</span></span> <span data-ttu-id="47b4c-134">Экземпляры класса службы можно установить на многих компьютерах, и каждый экземпляр предоставляет службы, которые определяются с его главным компьютером.</span><span class="sxs-lookup"><span data-stu-id="47b4c-134">You can install instances of the service class on many computers and each instance provides services that are identified with its host computer.</span></span> <span data-ttu-id="47b4c-135">Примерами служб на основе узла являются FTP и Telnet.</span><span class="sxs-lookup"><span data-stu-id="47b4c-135">FTP and Telnet are examples of host-based services.</span></span> <span data-ttu-id="47b4c-136">Имена участников-служб экземпляра службы на основе узла могут включать номер порта, если служба использует порт, отличный от используемого по умолчанию, или на узле имеется несколько экземпляров службы.</span><span class="sxs-lookup"><span data-stu-id="47b4c-136">The SPNs of a host-based service instance can include the port number if the service uses a non-default port or there are multiple instances of the service on the host.</span></span>


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a><span data-ttu-id="47b4c-137">Реплицируемые службы</span><span class="sxs-lookup"><span data-stu-id="47b4c-137">Replicable services</span></span>

<span data-ttu-id="47b4c-138">Для реплицируемой службы может существовать один или несколько экземпляров службы (реплик), и клиенты не отличают реплику, к которой они подключаются, так как каждая из них предоставляет одну и ту же службу.</span><span class="sxs-lookup"><span data-stu-id="47b4c-138">For a replicable service there can be one or many instances of the service (replicas), and clients do not differentiate which replica they connect to because each provides the same service.</span></span> <span data-ttu-id="47b4c-139">Имена участников-служб для каждой реплики имеют одинаковые &lt; компоненты "класс службы &gt; " и " &lt; имя службы" &gt; , где " &lt; имя службы &gt; " определяет более конкретную функциональность, предоставляемую службой.</span><span class="sxs-lookup"><span data-stu-id="47b4c-139">The SPNs for each replica have the same "&lt;service class&gt;" and "&lt;service name&gt;" components, where "&lt;service name&gt;" identifies more specifically the features provided by the service.</span></span> <span data-ttu-id="47b4c-140">Только компонент " &lt; узел &gt; " и необязательные "порты" могут &lt; &gt; отличаться от имен участников-служб и имен участников-служб.</span><span class="sxs-lookup"><span data-stu-id="47b4c-140">Only the "&lt;host&gt;" and optional "&lt;port&gt;" components would vary from SPN to SPN.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="47b4c-141">Примером реплицируемой службы будет экземпляр службы базы данных, который предоставляет доступ к указанной базе данных.</span><span class="sxs-lookup"><span data-stu-id="47b4c-141">An example of a replicable service would be an instance of a database service that provides access to a specified database.</span></span> <span data-ttu-id="47b4c-142">В этом случае " &lt; класс службы &gt; " определяет приложение базы данных, а " &lt; имя службы &gt; " определяет конкретную базу данных.</span><span class="sxs-lookup"><span data-stu-id="47b4c-142">In this case, "&lt;service class&gt;" identifies the database application and "&lt;service name&gt;" identifies the specific database.</span></span> <span data-ttu-id="47b4c-143">" &lt; имя службы &gt; " может быть различающимся именем точки подключения службы (SCP), содержащей данные подключения для базы данных.</span><span class="sxs-lookup"><span data-stu-id="47b4c-143">"&lt;service name&gt;" could be the distinguished name of a service connection point (SCP) containing connection data for the database.</span></span>


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="47b4c-144">Если клиенты будут использовать NetBIOS-имя для создания SPN службы, Каждая реплика также должна зарегистрировать имя субъекта-службы, которое содержит NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="47b4c-144">If clients will use the NetBIOS name to compose a service's SPN, each replica must also register an SPN containing the NetBIOS name.</span></span>


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="47b4c-145">Еще один пример реплицируемой службы — это служба, которая предоставляет службы для всего домена.</span><span class="sxs-lookup"><span data-stu-id="47b4c-145">Another example of a replicable service is one that provides services to an entire domain.</span></span> <span data-ttu-id="47b4c-146">В этом случае &lt; компонент Service Name &gt; — это DNS-имя обслуживаемого домена.</span><span class="sxs-lookup"><span data-stu-id="47b4c-146">In this case, the "&lt;service name&gt;" component is the DNS name of the domain being served.</span></span> <span data-ttu-id="47b4c-147">В качестве примера такого типа службы реплицируемых служб используется Kerberos KDC.</span><span class="sxs-lookup"><span data-stu-id="47b4c-147">A Kerberos KDC is an example of this type of replicable service.</span></span>

<span data-ttu-id="47b4c-148">Имейте в виду, что при изменении DNS-имени компьютера система обновляет &lt; &gt; элемент Host для всех зарегистрированных имен SPN для этого узла в лесу.</span><span class="sxs-lookup"><span data-stu-id="47b4c-148">Be aware that if the DNS name of a computer changes, the system updates the "&lt;host&gt;" element for all registered SPNs for that host in the forest.</span></span>

 

 




