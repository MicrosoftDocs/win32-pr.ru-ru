---
title: Службы безопасности MSMQ
description: Синхронные сообщения RPC могут использовать любую из функций безопасности, доступных во время выполнения RPC. Дополнительные сведения см. в разделе Безопасность.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134219"
---
# <a name="msmq-security-services"></a><span data-ttu-id="e596b-104">Службы безопасности MSMQ</span><span class="sxs-lookup"><span data-stu-id="e596b-104">MSMQ Security Services</span></span>

<span data-ttu-id="e596b-105">Синхронные сообщения RPC могут использовать любую из функций безопасности, доступных во время выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="e596b-105">Synchronous RPC messages can use any of the security features available from the RPC run time.</span></span> <span data-ttu-id="e596b-106">Дополнительные сведения см. в разделе [Безопасность](security.md) .</span><span class="sxs-lookup"><span data-stu-id="e596b-106">See [Security](security.md) for more details.</span></span>

<span data-ttu-id="e596b-107">Асинхронные \[ [](/windows/desktop/Midl/message) \] вызовы сообщений не могут использовать безопасность RPC, так как между клиентом и сервером отсутствует подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e596b-107">Asynchronous \[ [message](/windows/desktop/Midl/message)\] calls cannot use RPC security because there is no handshake between client and server.</span></span> <span data-ttu-id="e596b-108">На самом деле сервер может даже не работать во время вызова.</span><span class="sxs-lookup"><span data-stu-id="e596b-108">In fact, the server may not even be running at the time of the call.</span></span> <span data-ttu-id="e596b-109">Для доступа к службам безопасности, предоставляемым службами очередей сообщений (MSMQ), клиентское приложение должно вызывать [**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) для управления уровнем проверки подлинности и конфиденциальности для своих вызовов к серверу.</span><span class="sxs-lookup"><span data-stu-id="e596b-109">To access the security services provided by Message Queuing Services (MSMQ), the client application should call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) to control the level of authentication and privacy for its calls to the server.</span></span>

<span data-ttu-id="e596b-110">Серверное приложение может вызвать [**рпкбиндингинкаусклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) из удаленного вызова процедуры, чтобы определить уровень безопасности для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e596b-110">The server application can call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) from within a remote procedure call to determine the security level for that call.</span></span> <span data-ttu-id="e596b-111">В следующей таблице приведены сопоставления между константами безопасности RPC и безопасностью MSMQ.</span><span class="sxs-lookup"><span data-stu-id="e596b-111">The mapping between RPC security constants and MSMQ security is shown in the following table.</span></span>



| <span data-ttu-id="e596b-112">Уровень безопасности RPC</span><span class="sxs-lookup"><span data-stu-id="e596b-112">RPC security level</span></span>                | <span data-ttu-id="e596b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e596b-113">Description</span></span>                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e596b-114">\_уровень RPC \_ AUTHN \_ None</span><span class="sxs-lookup"><span data-stu-id="e596b-114">RPC\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="e596b-115">Вызов не прошел проверку подлинности или не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="e596b-115">The call is not authenticated or encrypted.</span></span>                                                |
| <span data-ttu-id="e596b-116">\_ \_ \_ целостность PKT RPC уровня AUTHN \_</span><span class="sxs-lookup"><span data-stu-id="e596b-116">RPC\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="e596b-117">Вызов проходит проверку подлинности с помощью MSMQ Security.</span><span class="sxs-lookup"><span data-stu-id="e596b-117">The call is authenticated using MSMQ security.</span></span>                                             |
| <span data-ttu-id="e596b-118">\_Конфиденциальность RPC \_ уровня AUTHN \_ PKT \_</span><span class="sxs-lookup"><span data-stu-id="e596b-118">RPC\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="e596b-119">Вызов проходит проверку подлинности и шифруется при передаче между очередью клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="e596b-119">The call is authenticated and encrypted as it travels between the client and server queue.</span></span> |



 

<span data-ttu-id="e596b-120">Сервер также может принудительно вызывать проверку подлинности и шифрование, вызывая [**рпксерверусепротсекепекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) и устанавливая \_ Флаги RPC c \_ MQ \_ AUTHN \_ уровня \_ None, RPC \_ c \_ MQ \_ AUTHN \_ \_ \_ Integrity и RPC \_ c \_ MQ \_ AUTHN \_ \_ на уровне маркера \_ безопасности в структуре [**\_ политики RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) .</span><span class="sxs-lookup"><span data-stu-id="e596b-120">The server can also force call authentication and encryption by calling [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) and setting the RPC\_C\_MQ\_AUTHN\_LEVEL\_NONE, RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_INTEGRITY and RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_PRIVACY flags in the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure.</span></span>

 

 