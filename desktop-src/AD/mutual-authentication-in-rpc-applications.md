---
title: Взаимная проверка подлинности в приложениях RPC
description: Службы RPC могут использовать точки подключения службы для публикации или могут использовать API-интерфейсы службы имен RPC (Рпкнс).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Взаимная проверка подлинности в Active Directory для приложений RPC
- Active Directory, использование, взаимная проверка подлинности, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890407"
---
# <a name="mutual-authentication-in-rpc-applications"></a><span data-ttu-id="01325-105">Взаимная проверка подлинности в приложениях RPC</span><span class="sxs-lookup"><span data-stu-id="01325-105">Mutual Authentication in RPC Applications</span></span>

<span data-ttu-id="01325-106">Службы RPC могут использовать точки подключения службы для публикации или могут использовать API-интерфейсы службы имен RPC (Рпкнс).</span><span class="sxs-lookup"><span data-stu-id="01325-106">RPC services can use service connection points to publish themselves, or they can use the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="01325-107">В этом разделе описывается взаимная проверка подлинности со службой RPC, которая публикует себя с помощью API-интерфейсов службы имен RPC (Рпкнс).</span><span class="sxs-lookup"><span data-stu-id="01325-107">This topic discusses how to perform mutual authentication with an RPC service that publishes itself using the RPC name service (RpcNs) APIs.</span></span>

<span data-ttu-id="01325-108">**Регистрация имени участника-службы в каталоге**</span><span class="sxs-lookup"><span data-stu-id="01325-108">**To register an SPN in the directory**</span></span>

1.  <span data-ttu-id="01325-109">Вызовите функцию [**дсжетспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) , чтобы создать имя участника-службы (SPN) для службы.</span><span class="sxs-lookup"><span data-stu-id="01325-109">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose a service principal name (SPN) for the service.</span></span>
2.  <span data-ttu-id="01325-110">Вызовите функцию [**дсвритеаккаунтспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) , чтобы зарегистрировать имя субъекта-службы в учетной записи или учетной записи компьютера, в контексте которой будет выполняться служба.</span><span class="sxs-lookup"><span data-stu-id="01325-110">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the SPN on the service account or computer account in whose context the service will run.</span></span>

<span data-ttu-id="01325-111">**Регистрация службы в службе именования RPC**</span><span class="sxs-lookup"><span data-stu-id="01325-111">**To register a service with the RPC naming service**</span></span>

1.  <span data-ttu-id="01325-112">Убедитесь, что соответствующие имена участников-служб зарегистрированы в учетной записи, от имени которой запущена служба.</span><span class="sxs-lookup"><span data-stu-id="01325-112">Verify that the appropriate SPNs are registered on the account under which the service is running.</span></span> <span data-ttu-id="01325-113">Дополнительные сведения см. в разделе [задачи обслуживания учетной записи входа](logon-account-maintenance-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="01325-113">For more information, see [Logon Account Maintenance Tasks](logon-account-maintenance-tasks.md).</span></span>
2.  <span data-ttu-id="01325-114">Вызовите функцию [**рпксерверрегистераусинфо**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) для регистрации имени субъекта-службы в службе проверки подлинности RPC и укажите **RPC \_ C \_ AUTHN \_ GSS \_ Negotiate** как службу проверки подлинности для использования.</span><span class="sxs-lookup"><span data-stu-id="01325-114">Call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function to register the service SPN with the RPC authentication service, and specify **RPC\_C\_AUTHN\_GSS\_NEGOTIATE** as the authentication service to use.</span></span>

<span data-ttu-id="01325-115">Дополнительные сведения о выполнении взаимной проверки подлинности в службе RPC см. в разделе [написание сервера SSPI с проверкой подлинности](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span><span class="sxs-lookup"><span data-stu-id="01325-115">For more information about performing mutual authentication in an RPC service, see [Writing an Authenticated SSPI Server](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span></span>

<span data-ttu-id="01325-116">**Проверка подлинности службы с клиента**</span><span class="sxs-lookup"><span data-stu-id="01325-116">**To authenticate the service from the client**</span></span>

1.  <span data-ttu-id="01325-117">Извлеките имя узла из привязки RPC.</span><span class="sxs-lookup"><span data-stu-id="01325-117">Extract the host name from the RPC Binding.</span></span>
2.  <span data-ttu-id="01325-118">Создайте имя участника-службы для службы, вызвав функцию [**дсмакеспн**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) с классом службы, именем узла DNS и именем службы. это различающееся имя точки подключения в случае Рпкнс.</span><span class="sxs-lookup"><span data-stu-id="01325-118">Compose the SPN for the service by calling the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function with the service class, the DNS host name, and the service name; that is the distinguished name of the connection point in the case of RpcNs.</span></span>

    <span data-ttu-id="01325-119">Дополнительные сведения о создании имени субъекта-службы для службы Рпкнс см. в разделе [составление имен участников-служб для службы рпкнс](composing-spns-for-an-rpcns-service.md).</span><span class="sxs-lookup"><span data-stu-id="01325-119">For more information about composing an SPN for an RpcNs service, see [Composing SPNs for an RpcNs Service](composing-spns-for-an-rpcns-service.md).</span></span>

3.  <span data-ttu-id="01325-120">Настройте структуру [**\_ \_ QoS безопасности RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) для запроса взаимной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="01325-120">Set up an [**RPC\_SECURITY\_QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) structure to request mutual authentication.</span></span>
4.  <span data-ttu-id="01325-121">Вызовите функцию [**рпкбиндингсетаусинфоекс**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , чтобы задать данные проверки подлинности для привязки RPC.</span><span class="sxs-lookup"><span data-stu-id="01325-121">Call the [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function to set the authentication data for the RPC binding.</span></span> <span data-ttu-id="01325-122">Клиент должен запросить **\_ \_ \_ \_ \_ целостность PKT C AUTHN уровня RPC** , чтобы убедиться, что связь не была изменена.</span><span class="sxs-lookup"><span data-stu-id="01325-122">The client must request at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY** to ensure that communications have not been tampered.</span></span> <span data-ttu-id="01325-123">Для повышения безопасности клиент должен указать для шифрования запросов **RPC \_ C \_ AUTHN уровня " \_ \_ PKT \_** ".</span><span class="sxs-lookup"><span data-stu-id="01325-123">For increased security, the client should specify **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** to request encryption.</span></span>
5.  <span data-ttu-id="01325-124">Выполните вызов RPC.</span><span class="sxs-lookup"><span data-stu-id="01325-124">Perform the RPC call.</span></span>

<span data-ttu-id="01325-125">Дополнительные сведения о выполнении взаимной проверки подлинности в клиенте RPC см. в разделе [написание клиента SSPI с проверкой подлинности](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span><span class="sxs-lookup"><span data-stu-id="01325-125">For more information about performing mutual authentication in an RPC client, see [Writing an Authenticated SSPI Client](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span></span>

<span data-ttu-id="01325-126">**Проверка подлинности клиента из службы**</span><span class="sxs-lookup"><span data-stu-id="01325-126">**To authenticate the client from the service**</span></span>

1.  <span data-ttu-id="01325-127">Вызовите функцию [**рпкбиндингинкаусклиент**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) , чтобы проверить параметры проверки подлинности, заданные клиентом.</span><span class="sxs-lookup"><span data-stu-id="01325-127">Call the [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) function to verify the authentication parameters specified by the client.</span></span> <span data-ttu-id="01325-128">Если клиент не запрашивал нужный уровень проверки подлинности, отклоните вызов.</span><span class="sxs-lookup"><span data-stu-id="01325-128">If the client has not requested the desired level of authentication, reject the call.</span></span> <span data-ttu-id="01325-129">Имейте в виду, что служба RPC должна проверять уровень проверки подлинности, службу проверки подлинности и удостоверение клиента при каждом вызове, чтобы обеспечить правильную проверку подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="01325-129">Be aware that an RPC service must verify the authentication level, authentication service, and client identity on every call to ensure that the client has been properly authenticated.</span></span>
2.  <span data-ttu-id="01325-130">Вызовите функцию [**рпЦимперсонатеклиент**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) для олицетворения клиента.</span><span class="sxs-lookup"><span data-stu-id="01325-130">Call the [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) function to impersonate the client.</span></span>
3.  <span data-ttu-id="01325-131">Выполните запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="01325-131">Perform the requested operation.</span></span>
4.  <span data-ttu-id="01325-132">Вызовите функцию [**рпкреверттоселф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) , чтобы вернуться к контексту безопасности службы.</span><span class="sxs-lookup"><span data-stu-id="01325-132">Call the [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) function to revert to the service security context.</span></span>

<span data-ttu-id="01325-133">Дополнительные сведения об олицетворении клиента RPC см. в разделе [олицетворение](/windows/desktop/Rpc/client-impersonation)клиента.</span><span class="sxs-lookup"><span data-stu-id="01325-133">For more information about RPC client impersonation, see [Client Impersonation](/windows/desktop/Rpc/client-impersonation).</span></span>

<span data-ttu-id="01325-134">Дополнительные сведения можно найти в разделе</span><span class="sxs-lookup"><span data-stu-id="01325-134">For more information, see:</span></span>

-   [<span data-ttu-id="01325-135">Публикация с помощью службы имен RPC (Рпкнс)</span><span class="sxs-lookup"><span data-stu-id="01325-135">Publishing with the RPC Name Service (RpcNs)</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="01325-136">Основы безопасности RPC</span><span class="sxs-lookup"><span data-stu-id="01325-136">RPC Security Essentials</span></span>](/windows/desktop/Rpc/rpc-security-essentials)

 

 