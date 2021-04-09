---
title: Создание безопасного клиента или сервера RPC
description: В этом разделе приводятся рекомендации по написанию безопасного клиента RPC или сервера.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- Удаленный вызов процедур RPC, рекомендации, написание безопасного клиента или сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070367"
---
# <a name="writing-a-secure-rpc-client-or-server"></a><span data-ttu-id="01e46-104">Создание безопасного клиента или сервера RPC</span><span class="sxs-lookup"><span data-stu-id="01e46-104">Writing a Secure RPC Client or Server</span></span>

<span data-ttu-id="01e46-105">В этом разделе приводятся рекомендации по написанию безопасного клиента RPC или сервера.</span><span class="sxs-lookup"><span data-stu-id="01e46-105">This section provides best practice recommendations for writing a secure RPC client or server.</span></span>

<span data-ttu-id="01e46-106">Сведения в этом разделе относятся к Windows 2000 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="01e46-106">The information in this section applies to Windows 2000 and Windows XP.</span></span> <span data-ttu-id="01e46-107">Этот раздел относится ко всем последовательностям протоколов, включая [**нкалрпк**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="01e46-107">This section applies to all protocol sequences, including [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="01e46-108">Разработчики, как правило, считают, что **нкалрпк** не является потенциальной целью для атаки, что неверно на сервере терминалов, где потенциально сотни пользователей имеют доступ к службе, что может привести к появлению дополнительного доступа.</span><span class="sxs-lookup"><span data-stu-id="01e46-108">Developers tend to think **ncalrpc** is not a probable target for an attack, which is not true on a terminal server where potentially hundreds of users have access to a service, and compromising or even bringing down a service can lead to acquiring extra access.</span></span>

<span data-ttu-id="01e46-109">Этот раздел состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="01e46-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="01e46-110">Используемый поставщик безопасности</span><span class="sxs-lookup"><span data-stu-id="01e46-110">Which Security Provider To Use</span></span>](which-security-provider-to-use.md)
-   [<span data-ttu-id="01e46-111">Управление проверкой подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="01e46-111">Controlling Client Authentication</span></span>](controlling-client-authentication.md)
-   [<span data-ttu-id="01e46-112">Выбор уровня проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="01e46-112">Choosing an Authentication Level</span></span>](choosing-an-authentication-level.md)
-   [<span data-ttu-id="01e46-113">Выбор параметров качества обслуживания для системы безопасности</span><span class="sxs-lookup"><span data-stu-id="01e46-113">Choosing Security QOS Options</span></span>](choosing-security-qos-options.md)
-   [<span data-ttu-id="01e46-114">Распространенная ошибка: допущение Рпксерверрегистераусинфо предотвращает вызов сервера неавторизованными пользователями</span><span class="sxs-lookup"><span data-stu-id="01e46-114">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [<span data-ttu-id="01e46-115">Обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="01e46-115">Callbacks</span></span>](callbacks.md)
-   [<span data-ttu-id="01e46-116">Сеансы со значением NULL</span><span class="sxs-lookup"><span data-stu-id="01e46-116">Null Sessions</span></span>](null-sessions.md)
-   [<span data-ttu-id="01e46-117">Использование флага/robust</span><span class="sxs-lookup"><span data-stu-id="01e46-117">Use the /robust Flag</span></span>](use-the-robust-flag.md)
-   [<span data-ttu-id="01e46-118">Методы IDL для лучшего проектирования интерфейсов и методов</span><span class="sxs-lookup"><span data-stu-id="01e46-118">IDL Techniques for Better Interface and Method Design</span></span>](idl-techniques-for-better-interface-and-method-design.md)
-   [<span data-ttu-id="01e46-119">Строгое и строго типизированные дескрипторы контекста</span><span class="sxs-lookup"><span data-stu-id="01e46-119">Strict and Type Strict Context Handles</span></span>](strict-and-type-strict-context-handles.md)
-   [<span data-ttu-id="01e46-120">Не доверять одноранговому узлу</span><span class="sxs-lookup"><span data-stu-id="01e46-120">Do Not Trust Your Peer</span></span>](do-not-trust-your-peer.md)
-   [<span data-ttu-id="01e46-121">Не использовать безопасность конечных точек</span><span class="sxs-lookup"><span data-stu-id="01e46-121">Do Not Use Endpoint Security</span></span>](do-not-use-endpoint-security.md)
-   [<span data-ttu-id="01e46-122">Будьте осторожны с другими конечными точками RPC, работающими в том же процессе</span><span class="sxs-lookup"><span data-stu-id="01e46-122">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [<span data-ttu-id="01e46-123">Убедитесь, что сервер требует утверждения</span><span class="sxs-lookup"><span data-stu-id="01e46-123">Verify The Server Is Who It Claims To Be</span></span>](verify-the-server-is-who-it-claims-to-be.md)
-   [<span data-ttu-id="01e46-124">Использование основных последовательностей протоколов</span><span class="sxs-lookup"><span data-stu-id="01e46-124">Use Mainstream Protocol Sequences</span></span>](use-mainstream-protocol-sequences.md)
-   [<span data-ttu-id="01e46-125">Насколько защищен мой RPC-сервер?</span><span class="sxs-lookup"><span data-stu-id="01e46-125">How Secure is my RPC Server Now?</span></span>](how-secure-is-my-rpc-server-now.md)

 

 