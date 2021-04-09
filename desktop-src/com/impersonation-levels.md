---
title: Уровни олицетворения (COM)
description: Если олицетворение завершилось успешно, это означает, что клиент принял согласие на то, чтобы сервер был клиентом в некоторой степени.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891101"
---
# <a name="impersonation-levels"></a><span data-ttu-id="bad33-103">Уровни олицетворения</span><span class="sxs-lookup"><span data-stu-id="bad33-103">Impersonation Levels</span></span>

<span data-ttu-id="bad33-104">Если олицетворение завершилось успешно, это означает, что клиент принял согласие на то, чтобы сервер был клиентом в некоторой степени.</span><span class="sxs-lookup"><span data-stu-id="bad33-104">If impersonation succeeds, it means that the client has agreed to let the server be the client to some degree.</span></span> <span data-ttu-id="bad33-105">Различные степени олицетворения называются *уровнями олицетворения*, и они указывают, сколько полномочий предоставляется серверу при олицетворении клиента.</span><span class="sxs-lookup"><span data-stu-id="bad33-105">The varying degrees of impersonation are called *impersonation levels*, and they indicate how much authority is given to the server when it is impersonating the client.</span></span>

<span data-ttu-id="bad33-106">В настоящее время существует четыре уровня олицетворения: *анонимные*, *выявление*, *олицетворение* и *Делегирование*.</span><span class="sxs-lookup"><span data-stu-id="bad33-106">Currently, there are four impersonation levels: *anonymous*, *identify*, *impersonate*, and *delegate*.</span></span> <span data-ttu-id="bad33-107">В следующем списке кратко описан каждый уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="bad33-107">The following list briefly describes each impersonation level:</span></span>

<dl> <dt>

<span data-ttu-id="bad33-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>Анонимный ( \_ \_ \_ Анонимный уровень RPC C \_ )</span><span class="sxs-lookup"><span data-stu-id="bad33-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC\_C\_IMP\_LEVEL\_ANONYMOUS)</span></span>
</dt> <dd>

<span data-ttu-id="bad33-109">Клиент анонимен по отношению к серверу.</span><span class="sxs-lookup"><span data-stu-id="bad33-109">The client is anonymous to the server.</span></span> <span data-ttu-id="bad33-110">Серверный процесс может олицетворять клиента, но маркер олицетворения не содержит никакой информации о клиенте.</span><span class="sxs-lookup"><span data-stu-id="bad33-110">The server process can impersonate the client, but the impersonation token does not contain any information about the client.</span></span> <span data-ttu-id="bad33-111">Этот уровень поддерживается только для локального межпроцессного транспорта взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="bad33-111">This level is only supported over the local interprocess communication transport.</span></span> <span data-ttu-id="bad33-112">Все остальные транспорты продают автоматическую роль этого уровня для распознавания.</span><span class="sxs-lookup"><span data-stu-id="bad33-112">All other transports silently promote this level to identify.</span></span>

</dd> <dt>

<span data-ttu-id="bad33-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>Identify ( \_ Обнаружение на \_ \_ уровне \_ идентификаторов RPC C)</span><span class="sxs-lookup"><span data-stu-id="bad33-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC\_C\_IMP\_LEVEL\_IDENTIFY)</span></span>
</dt> <dd>

<span data-ttu-id="bad33-114">Уровень, установленный в системе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bad33-114">The system default level.</span></span> <span data-ttu-id="bad33-115">Сервер может получать удостоверение клиента и олицетворять клиента, чтобы производить проверки списка управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="bad33-115">The server can obtain the client's identity, and the server can impersonate the client to do ACL checks.</span></span>

</dd> <dt>

<span data-ttu-id="bad33-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>олицетворять ( \_ \_ \_ олицетворение на уровне RPC C \_ )</span><span class="sxs-lookup"><span data-stu-id="bad33-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC\_C\_IMP\_LEVEL\_IMPERSONATE)</span></span>
</dt> <dd>

<span data-ttu-id="bad33-117">Сервер может олицетворять контекст безопасности клиента, пока действует от его лица.</span><span class="sxs-lookup"><span data-stu-id="bad33-117">The server can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="bad33-118">Сервер может получать доступ к локальным ресурсам в качестве клиента.</span><span class="sxs-lookup"><span data-stu-id="bad33-118">The server can access local resources as the client.</span></span> <span data-ttu-id="bad33-119">Если сервер является локальным, он может получить доступ к сетевым ресурсам в качестве клиента.</span><span class="sxs-lookup"><span data-stu-id="bad33-119">If the server is local, it can access network resources as the client.</span></span> <span data-ttu-id="bad33-120">Если сервер является удаленным, он может получить доступ только к тем ресурсам, которые находятся на том же компьютере, что и сервер.</span><span class="sxs-lookup"><span data-stu-id="bad33-120">If the server is remote, it can access only resources that are on the same computer as the server.</span></span>

</dd> <dt>

<span data-ttu-id="bad33-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>Delegate ( \_ \_ делегат уровня Imp RPC C \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="bad33-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC\_C\_IMP\_LEVEL\_DELEGATE)</span></span>
</dt> <dd>

<span data-ttu-id="bad33-122">Самый высокий уровень олицетворения.</span><span class="sxs-lookup"><span data-stu-id="bad33-122">The most powerful impersonation level.</span></span> <span data-ttu-id="bad33-123">Когда выбран этот уровень, сервер (локальный или удаленный) может олицетворять контекст безопасности клиента, пока действует от его лица.</span><span class="sxs-lookup"><span data-stu-id="bad33-123">When this level is selected, the server (whether local or remote) can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="bad33-124">Во время олицетворения учетные данные клиента (как локальных, так и сетевых) могут быть переданы на любое количество компьютеров.</span><span class="sxs-lookup"><span data-stu-id="bad33-124">During impersonation, the client's credentials (both local and network) can be passed to any number of computers.</span></span>

<span data-ttu-id="bad33-125">Чтобы олицетворение работало на уровне делегата, должны выполняться следующие требования.</span><span class="sxs-lookup"><span data-stu-id="bad33-125">For impersonation to work at the delegate level, the following requirements must be met:</span></span>

-   <span data-ttu-id="bad33-126">Клиент должен задать уровень олицетворения \_ \_ \_ делегата уровня "RPC C" \_ .</span><span class="sxs-lookup"><span data-stu-id="bad33-126">The client must set the impersonation level to RPC\_C\_IMP\_LEVEL\_DELEGATE.</span></span>
-   <span data-ttu-id="bad33-127">Учетная запись клиента не должна быть помечена как "учетная запись является конфиденциальной и не может быть делегирована" в службе Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bad33-127">The client account must not be marked "Account is sensitive and cannot be delegated" in the Active Directory Service.</span></span>
-   <span data-ttu-id="bad33-128">Учетная запись сервера должна быть помечена атрибутом "доверенный для делегирования" в службе Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bad33-128">The server account must be marked with the "Trusted for delegation" attribute in the Active Directory Service.</span></span>
-   <span data-ttu-id="bad33-129">Компьютеры, на которых размещается клиент, сервер и все нижестоящие серверы, должны работать в домене.</span><span class="sxs-lookup"><span data-stu-id="bad33-129">The computers hosting the client, the server, and any "downstream" servers must all be running in a domain.</span></span>

</dd> </dl>

<span data-ttu-id="bad33-130">Выбирая уровень олицетворения, клиент сообщает серверу, насколько далеко он может пройти через олицетворение клиента.</span><span class="sxs-lookup"><span data-stu-id="bad33-130">By choosing the impersonation level, the client tells the server how far it can go in impersonating the client.</span></span> <span data-ttu-id="bad33-131">Клиент устанавливает уровень олицетворения для прокси-сервера, который он использует для взаимодействия с сервером.</span><span class="sxs-lookup"><span data-stu-id="bad33-131">The client sets the impersonation level on the proxy it uses to communicate with the server.</span></span>

## <a name="setting-the-impersonation-level"></a><span data-ttu-id="bad33-132">Установка уровня олицетворения</span><span class="sxs-lookup"><span data-stu-id="bad33-132">Setting the Impersonation Level</span></span>

<span data-ttu-id="bad33-133">Задать уровень олицетворения можно двумя способами:</span><span class="sxs-lookup"><span data-stu-id="bad33-133">There are two ways to set the impersonation level:</span></span>

-   <span data-ttu-id="bad33-134">Клиент может задать процессвиде с помощью вызова [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="bad33-134">The client can set it processwide, through a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="bad33-135">Клиент может установить безопасность на уровне прокси-сервера для интерфейса удаленного объекта с помощью вызова [**иклиентсекурити:: сетбланкет**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (или вспомогательной функции [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span><span class="sxs-lookup"><span data-stu-id="bad33-135">A client can set proxy-level security on an interface of a remote object through a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (or the helper function [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span></span>

<span data-ttu-id="bad33-136">Уровень олицетворения задается путем передачи соответствующего значения "The RPC \_ C \_ "-Imp \_ \_ "XXX" в [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) или [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) с помощью параметра *двимплевел* .</span><span class="sxs-lookup"><span data-stu-id="bad33-136">You set the impersonation level by passing an appropriate RPC\_C\_IMP\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwImpLevel* parameter.</span></span>

<span data-ttu-id="bad33-137">Разные службы проверки подлинности поддерживают олицетворение на уровне делегата в различных экстентах.</span><span class="sxs-lookup"><span data-stu-id="bad33-137">Different authentication services support delegate-level impersonation to different extents.</span></span> <span data-ttu-id="bad33-138">Например, поставщик NTLMSSP поддерживает олицетворение на уровне делегата между потоками и между процессами, но не между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="bad33-138">For instance, NTLMSSP supports cross-thread and cross-process delegate-level impersonation, but not cross-computer.</span></span> <span data-ttu-id="bad33-139">С другой стороны, протокол Kerberos поддерживает олицетворение на уровне делегата на границах компьютеров, а SChannel не поддерживает олицетворение на уровне делегата.</span><span class="sxs-lookup"><span data-stu-id="bad33-139">On the other hand, the Kerberos protocol supports delegate-level impersonation across computer boundaries, while Schannel does not support any impersonation at the delegate level.</span></span> <span data-ttu-id="bad33-140">Если у вас есть прокси-сервер на уровне олицетворения, и вы хотите задать для уровня олицетворения значение Delegate, следует вызвать [**сетбланкет**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) , используя константы по умолчанию для каждого параметра, кроме уровня олицетворения.</span><span class="sxs-lookup"><span data-stu-id="bad33-140">If you have a proxy at impersonate level and you want to set the impersonation level to delegate, you should call [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) using the default constants for every parameter except the impersonation level.</span></span> <span data-ttu-id="bad33-141">COM выберет NTLM локально и протокол Kerberos удаленно (когда будет работать протокол Kerberos).</span><span class="sxs-lookup"><span data-stu-id="bad33-141">COM will choose NTLM locally and the Kerberos protocol remotely (when the Kerberos protocol will work).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bad33-142">См. также</span><span class="sxs-lookup"><span data-stu-id="bad33-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bad33-143">Делегирование и олицетворение</span><span class="sxs-lookup"><span data-stu-id="bad33-143">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 