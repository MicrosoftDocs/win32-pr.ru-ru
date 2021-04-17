---
title: Пакеты безопасности и COM
description: Windows поддерживает NTLMSSP (поставщик поддержки безопасности LAN Manager), протокол проверки подлинности Kerberos V5 и пакет безопасности SChannel, который предоставляет протоколы PCT 1,0, SSL 2,0, SSL 3,0 и TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710053"
---
# <a name="com-and-security-packages"></a><span data-ttu-id="78daa-103">Пакеты безопасности и COM</span><span class="sxs-lookup"><span data-stu-id="78daa-103">COM and Security Packages</span></span>

<span data-ttu-id="78daa-104">Windows поддерживает NTLMSSP (поставщик поддержки безопасности LAN Manager), протокол проверки подлинности Kerberos V5 и пакет безопасности SChannel, который предоставляет протоколы PCT 1,0, SSL 2,0, SSL 3,0 и TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="78daa-104">Windows supports NTLMSSP (LAN Manager Security Support Provider), the Kerberos v5 authentication protocol, and the Schannel security package, which provides the PCT 1.0, SSL 2.0, SSL 3.0, and TLS 1.0 protocols.</span></span> <span data-ttu-id="78daa-105">Также поддерживается снего, который проверяет наличие доступных пакетов безопасности и выбирает наиболее подходящий из них.</span><span class="sxs-lookup"><span data-stu-id="78daa-105">Also supported is Snego, which checks for available security packages and selects the most appropriate one.</span></span>

<span data-ttu-id="78daa-106">В следующей таблице показаны уровни проверки подлинности, поддерживаемые различными пакетами безопасности.</span><span class="sxs-lookup"><span data-stu-id="78daa-106">The following table shows the levels of authentication supported by the various security packages.</span></span>



| <span data-ttu-id="78daa-107">Проверка подлинности сервера или клиента</span><span class="sxs-lookup"><span data-stu-id="78daa-107">Server/Client Authentication</span></span>                                                                                           | <span data-ttu-id="78daa-108">Поддержка пакетов безопасности</span><span class="sxs-lookup"><span data-stu-id="78daa-108">Security Package Support</span></span>                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="78daa-109">Ни один из них не может получить имя другого.</span><span class="sxs-lookup"><span data-stu-id="78daa-109">Neither can get the name of the other.</span></span><br/>                                                                      | <span data-ttu-id="78daa-110">Нет</span><span class="sxs-lookup"><span data-stu-id="78daa-110">None</span></span><br/>                                                  |
| <span data-ttu-id="78daa-111">Клиент может проверить подлинность сервера, но не наоборот.</span><span class="sxs-lookup"><span data-stu-id="78daa-111">The client can authenticate the server, but not vice versa.</span></span><br/>                                                 | <span data-ttu-id="78daa-112">Schannel</span><span class="sxs-lookup"><span data-stu-id="78daa-112">Schannel</span></span><br/>                                              |
| <span data-ttu-id="78daa-113">Клиенту не удается обнаружить сервер, но сервер может получить идентификатор пользователя клиента.</span><span class="sxs-lookup"><span data-stu-id="78daa-113">The client cannot discover the server, but the server can get the user ID of the client.</span></span><br/>                    | <span data-ttu-id="78daa-114">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="78daa-114">NTLMSSP</span></span><br/>                                               |
| <span data-ttu-id="78daa-115">Взаимная проверка подлинности. как клиент, так и сервер могут узнавать имя другого, если предоставлено разрешение.</span><span class="sxs-lookup"><span data-stu-id="78daa-115">Mutual authentication: Both the client and server can know the name of the other, if permission is granted.</span></span><br/> | <span data-ttu-id="78daa-116">Поставщик NTLMSSP (локально), протокол Kerberos V5 и SChannel</span><span class="sxs-lookup"><span data-stu-id="78daa-116">NTLMSSP (locally), Kerberos v5 protocol, and Schannel</span></span><br/> |



 

<span data-ttu-id="78daa-117">Дополнительные сведения об этих пакетах безопасности см. в следующих подразделах этого раздела:</span><span class="sxs-lookup"><span data-stu-id="78daa-117">For more information about these security packages, see the following topics in this section:</span></span>

-   [<span data-ttu-id="78daa-118">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="78daa-118">NTLMSSP</span></span>](ntlmssp.md)
-   [<span data-ttu-id="78daa-119">Протокол Kerberos V5</span><span class="sxs-lookup"><span data-stu-id="78daa-119">Kerberos v5 Protocol</span></span>](kerberos-v5-protocol.md)
-   [<span data-ttu-id="78daa-120">Schannel</span><span class="sxs-lookup"><span data-stu-id="78daa-120">Schannel</span></span>](schannel.md)
-   [<span data-ttu-id="78daa-121">снего</span><span class="sxs-lookup"><span data-stu-id="78daa-121">Snego</span></span>](snego.md)

## <a name="related-topics"></a><span data-ttu-id="78daa-122">См. также</span><span class="sxs-lookup"><span data-stu-id="78daa-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78daa-123">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="78daa-123">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 





