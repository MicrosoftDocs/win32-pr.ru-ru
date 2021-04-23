---
title: Уровень проверки подлинности
description: Уровень проверки подлинности определяет степень безопасности, которую клиент или сервер должен получить от своего поставщика общих служб.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332640"
---
# <a name="authentication-level"></a><span data-ttu-id="47ddc-103">Уровень проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="47ddc-103">Authentication Level</span></span>

<span data-ttu-id="47ddc-104">Уровень проверки подлинности определяет степень безопасности, которую клиент или сервер должен получить от своего поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="47ddc-104">The authentication level controls how much security a client or server wants from its SSP.</span></span> <span data-ttu-id="47ddc-105">Уровень проверки подлинности задается путем передачи \_ соответствующего \_ значения уровня RPC C AUTHN \_ Level \_ xxx в [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) или [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) с помощью параметра *двауснлевел* .</span><span class="sxs-lookup"><span data-stu-id="47ddc-105">The authentication level is set by passing an appropriate RPC\_C\_AUTHN\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwAuthnLevel* parameter.</span></span> <span data-ttu-id="47ddc-106">Уровни проверки подлинности от клиента и сервера сравниваются во время подтверждения, а для соединения используется параметр защиты более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="47ddc-106">The authentication levels from the client and server are compared during the handshake, and the higher level security protection setting is used for the connection.</span></span>

<span data-ttu-id="47ddc-107">Различные уровни проверки подлинности описаны ниже, начиная с нижнего уровня защиты безопасности до самого высокого:</span><span class="sxs-lookup"><span data-stu-id="47ddc-107">The different authentication levels are described as follows, from lowest level security protection to highest:</span></span>

<dl> <dt>

<span data-ttu-id="47ddc-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>Нет ( \_ уровень RPC \_ C \_ AUTHN \_ None)</span><span class="sxs-lookup"><span data-stu-id="47ddc-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC\_C\_AUTHN\_LEVEL\_NONE)</span></span>
</dt> <dd>

<span data-ttu-id="47ddc-109">При обмене данными между клиентом и сервером не выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="47ddc-109">No authentication is performed during the communication between client and server.</span></span> <span data-ttu-id="47ddc-110">Все параметры безопасности игнорируются.</span><span class="sxs-lookup"><span data-stu-id="47ddc-110">All security settings are ignored.</span></span> <span data-ttu-id="47ddc-111">Этот уровень проверки подлинности можно задать только в том случае, если [уровень службы проверки подлинности](com-authentication-service-constants.md) — RPC \_ C \_ AUTHN \_ None.</span><span class="sxs-lookup"><span data-stu-id="47ddc-111">This authentication level can be set only if the [authentication service level](com-authentication-service-constants.md) is RPC\_C\_AUTHN\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="47ddc-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC \_ C \_ \_ \_ по умолчанию на уровне AUTHN)</span><span class="sxs-lookup"><span data-stu-id="47ddc-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC\_C\_AUTHN\_LEVEL\_DEFAULT)</span></span>
</dt> <dd>

<span data-ttu-id="47ddc-113">COM выбирает уровень проверки подлинности с помощью обычного согласования безопасности.</span><span class="sxs-lookup"><span data-stu-id="47ddc-113">COM chooses the authentication level by using its normal security blanket negotiation.</span></span> <span data-ttu-id="47ddc-114">Он никогда не будет выбирать уровень проверки подлинности None.</span><span class="sxs-lookup"><span data-stu-id="47ddc-114">It will never choose an authentication level of None.</span></span>

</dd> <dt>

<span data-ttu-id="47ddc-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC \_ C \_ AUTHN \_ Level \_ Connect)</span><span class="sxs-lookup"><span data-stu-id="47ddc-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC\_C\_AUTHN\_LEVEL\_CONNECT)</span></span>
</dt> <dd>

<span data-ttu-id="47ddc-116">Обычная проверка подлинности выполняется между клиентом и сервером, а сеансовый ключ устанавливается, но этот ключ никогда не используется для обмена данными между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="47ddc-116">The normal authentication handshake occurs between the client and server, and a session key is established but that key is never used for communication between the client and server.</span></span> <span data-ttu-id="47ddc-117">Все связи после подтверждения не являются безопасными.</span><span class="sxs-lookup"><span data-stu-id="47ddc-117">All communication after the handshake is nonsecure.</span></span>

</dd> <dt>

<span data-ttu-id="47ddc-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call ( \_ \_ вызов уровня RPC C AUTHN \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="47ddc-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC\_C\_AUTHN\_LEVEL\_CALL)</span></span>
</dt> <dd>

<span data-ttu-id="47ddc-119">Подписываются только заголовки начала каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="47ddc-119">Only the headers of the beginning of each call are signed.</span></span> <span data-ttu-id="47ddc-120">Остальные данные, которыми обмениваются клиент и сервер, не являются ни подписанными, ни зашифрованными.</span><span class="sxs-lookup"><span data-stu-id="47ddc-120">The rest of the data exchanged between the client and server is neither signed nor encrypted.</span></span> <span data-ttu-id="47ddc-121">Большинство SSP не поддерживают этот уровень проверки подлинности и без уведомления передаются в пакет.</span><span class="sxs-lookup"><span data-stu-id="47ddc-121">Most SSPs do not support this authentication level and silently promote it to Packet.</span></span>

</dd> <dt>

<span data-ttu-id="47ddc-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Пакет (RPC \_ C \_ уровня AUTHN на \_ уровне \_ маркера)</span><span class="sxs-lookup"><span data-stu-id="47ddc-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Packet (RPC\_C\_AUTHN\_LEVEL\_PKT)</span></span>
</dt> <dd>

<span data-ttu-id="47ddc-123">Заголовок каждого пакета подписывается, но не шифруется.</span><span class="sxs-lookup"><span data-stu-id="47ddc-123">The header of each packet is signed but not encrypted.</span></span> <span data-ttu-id="47ddc-124">Сами пакеты не подписываются и не шифруются.</span><span class="sxs-lookup"><span data-stu-id="47ddc-124">The packets themselves are not signed or encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="47ddc-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Целостность пакетов ( \_ RPC \_ C \_ AUTHN \_ уровня \_ целостности PKT)</span><span class="sxs-lookup"><span data-stu-id="47ddc-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Packet Integrity (RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY)</span></span>
</dt> <dd>

<span data-ttu-id="47ddc-126">Каждый пакет данных подписывается целиком, но не шифруется.</span><span class="sxs-lookup"><span data-stu-id="47ddc-126">Each packet of data is signed in its entirety but is not encrypted.</span></span> <span data-ttu-id="47ddc-127">Так как все данные подписаны отправителем, получатель может убедиться, что ни один из данных не был изменен во время передачи.</span><span class="sxs-lookup"><span data-stu-id="47ddc-127">Because all of the data is signed by the sender, the recipient can be certain that none of the data has been tampered with during transit.</span></span>

</dd> <dt>

<span data-ttu-id="47ddc-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Конфиденциальность пакетов (RPC \_ C \_ AUTHN \_ уровня \_ \_ "Конфиденциальность")</span><span class="sxs-lookup"><span data-stu-id="47ddc-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Packet Privacy (RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY)</span></span>
</dt> <dd>

<span data-ttu-id="47ddc-129">Каждый пакет данных подписывается и шифруется.</span><span class="sxs-lookup"><span data-stu-id="47ddc-129">Each data packet is signed and encrypted.</span></span> <span data-ttu-id="47ddc-130">Это помогает защитить весь обмен данными между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="47ddc-130">This helps protect the entire communication between the client and server.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="47ddc-131">См. также</span><span class="sxs-lookup"><span data-stu-id="47ddc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47ddc-132">аусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="47ddc-132">AuthenticationLevel</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="47ddc-133">легациаусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="47ddc-133">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
</dt> </dl>

 

 




