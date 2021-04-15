---
title: Взаимная проверка подлинности с помощью Kerberos
description: Взаимная проверка подлинности — это функция безопасности, в которой клиентский процесс должен доказать свою личность службе, и служба должна доказать свою личность клиенту, прежде чем трафик приложения передается через подключение клиента или службы.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, взаимная проверка подлинности
- Active Directory, использование, безопасность, взаимная проверка подлинности
- безопасность AD
- безопасность AD, взаимная проверка подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105654285"
---
# <a name="mutual-authentication-using-kerberos"></a><span data-ttu-id="37df6-107">Взаимная проверка подлинности с помощью Kerberos</span><span class="sxs-lookup"><span data-stu-id="37df6-107">Mutual Authentication Using Kerberos</span></span>

<span data-ttu-id="37df6-108">Взаимная проверка подлинности — это функция безопасности, в которой клиентский процесс должен доказать свою личность службе, и служба должна доказать свою личность клиенту, прежде чем трафик приложения передается через подключение клиента или службы.</span><span class="sxs-lookup"><span data-stu-id="37df6-108">Mutual authentication is a security feature in which a client process must prove its identity to a service, and the service must prove its identity to the client, before any application traffic is transmitted over the client/service connection.</span></span>

<span data-ttu-id="37df6-109">Службы домен Active Directory и Windows обеспечивают поддержку имен участников-служб (SPN), которые являются ключевым компонентом механизма Kerberos, с помощью которого клиент проходит проверку подлинности службы.</span><span class="sxs-lookup"><span data-stu-id="37df6-109">Active Directory Domain Services and Windows provide support for service principal names (SPN), which are a key component in the Kerberos mechanism by which a client authenticates a service.</span></span> <span data-ttu-id="37df6-110">SPN — это уникальное имя, идентифицирующее экземпляр службы и связанное с учетной записью входа, под которой работает экземпляр службы.</span><span class="sxs-lookup"><span data-stu-id="37df6-110">An SPN is a unique name that identifies an instance of a service and is associated with the logon account under which the service instance runs.</span></span> <span data-ttu-id="37df6-111">Компоненты имени субъекта-службы — это то, что клиент может создать имя субъекта-службы без учетной записи входа в службу.</span><span class="sxs-lookup"><span data-stu-id="37df6-111">The components of an SPN are such that a client can compose an SPN for a service without the service logon account.</span></span> <span data-ttu-id="37df6-112">Это позволяет клиенту запросить службу для проверки подлинности учетной записи, даже если у клиента нет имени учетной записи.</span><span class="sxs-lookup"><span data-stu-id="37df6-112">This enables the client to request the service to authenticate its account even though the client does not have the account name.</span></span>

<span data-ttu-id="37df6-113">Этот раздел содержит общие сведения о:</span><span class="sxs-lookup"><span data-stu-id="37df6-113">This section includes an overview of:</span></span>

-   <span data-ttu-id="37df6-114">Взаимная проверка подлинности с помощью Kerberos.</span><span class="sxs-lookup"><span data-stu-id="37df6-114">Mutual authentication using Kerberos.</span></span>
-   <span data-ttu-id="37df6-115">Составление уникального имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="37df6-115">Composing a unique SPN.</span></span>
-   <span data-ttu-id="37df6-116">Как установщик службы регистрирует имена субъектов-служб в объекте Account, связанном с экземпляром службы.</span><span class="sxs-lookup"><span data-stu-id="37df6-116">How a service installer registers SPNs on the account object associated with a service instance.</span></span>
-   <span data-ttu-id="37df6-117">Как клиентское приложение использует объект точки подключения службы (SCP) экземпляра службы в службах домен Active Directory Services для получения данных, из которых составлять имена участников-служб для службы.</span><span class="sxs-lookup"><span data-stu-id="37df6-117">How a client application uses a service instance's service connection point (SCP) object in Active Directory Domain Services to retrieve data from which to compose an SPN for the service.</span></span>
-   <span data-ttu-id="37df6-118">Как клиентское приложение использует имя субъекта-службы в сочетании с интерфейсом поставщика поддержки безопасности (SSPI) для проверки подлинности службы.</span><span class="sxs-lookup"><span data-stu-id="37df6-118">How a client application uses a service SPN in conjunction with the Security Support Provider Interface (SSPI) to authenticate the service.</span></span>
-   <span data-ttu-id="37df6-119">Пример кода для приложения клиента или службы Windows Sockets, который использует SCP и SSPI для взаимной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="37df6-119">A code example for a Windows Sockets client/service application that uses an SCP and SSPI to perform mutual authentication.</span></span>
-   <span data-ttu-id="37df6-120">Пример кода для клиента или службы RPC, который выполняет взаимную проверку подлинности с помощью службы имен RPC и проверки подлинности RPC.</span><span class="sxs-lookup"><span data-stu-id="37df6-120">A code example for an RPC client/service that performs mutual authentication using the RPC name service and RPC authentication.</span></span>
-   <span data-ttu-id="37df6-121">Как служба регистрации и разрешения Windows Sockets (РНР) использует имена участников-служб для взаимной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="37df6-121">How a Windows Sockets Registration and Resolution (RnR) service uses SPNs to perform mutual authentication.</span></span>

<span data-ttu-id="37df6-122">В этом разделе обсуждается использование службы домен Active Directory для взаимной проверки подлинности, в частности, назначения точек подключения службы и имен субъектов-служб при взаимной проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="37df6-122">This section discusses using Active Directory Domain Service for mutual authentication, in particular, the purpose of service connection points and service principal names in mutual authentication.</span></span> <span data-ttu-id="37df6-123">Это не полное обсуждение того, как использовать SSPI для взаимной проверки подлинности или проверки подлинности и безопасности, доступной для приложений RPC и Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="37df6-123">It is not a complete discussion of how to use SSPI for mutual authentication or the authentication and security support available for RPC and Windows Sockets applications.</span></span>

<span data-ttu-id="37df6-124">Дополнительные сведения можно найти в разделе</span><span class="sxs-lookup"><span data-stu-id="37df6-124">For more information, see:</span></span>

-   [<span data-ttu-id="37df6-125">Публикация с точками подключения службы</span><span class="sxs-lookup"><span data-stu-id="37df6-125">Publishing with service connection points</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="37df6-126">SSPI</span><span class="sxs-lookup"><span data-stu-id="37df6-126">SSPI</span></span>](/windows/desktop/SecAuthN/sspi)
-   [<span data-ttu-id="37df6-127">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="37df6-127">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [<span data-ttu-id="37df6-128">RPC</span><span class="sxs-lookup"><span data-stu-id="37df6-128">RPC</span></span>](/windows/desktop/Rpc/rpc-start-page)

 

 