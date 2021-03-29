---
title: Распространенная ошибка, допущенная Рпксерверрегистераусинфо, не позволяет неавторизованным пользователям вызывать сервер
description: Когда поставщики безопасности регистрируются на сервере с помощью функции Рпксерверрегистераусинфо, добавляется параметр, а не требование.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778875"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a><span data-ttu-id="f1b6b-103">Распространенная ошибка: допущение Рпксерверрегистераусинфо предотвращает вызов сервера неавторизованными пользователями</span><span class="sxs-lookup"><span data-stu-id="f1b6b-103">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>

<span data-ttu-id="f1b6b-104">Когда поставщики безопасности регистрируются на сервере с помощью функции [**рпксерверрегистераусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) , добавляется параметр, а не требование.</span><span class="sxs-lookup"><span data-stu-id="f1b6b-104">When security providers are registered on the server with the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function, an option is added, not a requirement.</span></span> <span data-ttu-id="f1b6b-105">Это означает, что предыдущие регистрации с **рпксерверрегистераусинфо** не заменяются.</span><span class="sxs-lookup"><span data-stu-id="f1b6b-105">This means previous registrations with **RpcServerRegisterAuthInfo** are not replaced.</span></span> <span data-ttu-id="f1b6b-106">Это также означает, что клиенты, не прошедшие проверку подлинности, могут подключаться.</span><span class="sxs-lookup"><span data-stu-id="f1b6b-106">This also means unauthenticated clients still can connect.</span></span> <span data-ttu-id="f1b6b-107">При вызове функции **рпксерверрегистераусинфо** клиенты, не прошедшие проверку подлинности, не могут быть разрешены. они по-прежнему могут подключаться, но вызовы функций, такие как [**рпЦимперсонатеклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) и [**рпкжетаусоризатионконтекстфорклиент**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) , завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f1b6b-107">By calling the **RpcServerRegisterAuthInfo** function, unauthenticated clients are not disallowed from connecting; they can still connect, but function calls such as [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) will fail.</span></span> <span data-ttu-id="f1b6b-108">Таким образом, при вызове функции **рпксерверрегистераусинфо** потенциальные злоумышленники не видед, а клиенты, которым требуется доступ, получают шанс подтвердить свою личность.</span><span class="sxs-lookup"><span data-stu-id="f1b6b-108">So when the **RpcServerRegisterAuthInfo** function is called, potential attackers have not been weeded out—rather, clients that ought to have access are given a chance to prove their identity.</span></span> <span data-ttu-id="f1b6b-109">Чтобы определить, пытаются ли подключиться потенциальные злоумышленники, необходимо выполнить проверку.</span><span class="sxs-lookup"><span data-stu-id="f1b6b-109">Checks must still be in place to determine whether potential attackers are attempting to connect.</span></span>

 

 




