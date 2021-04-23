---
title: Используемый поставщик безопасности
description: Все остальные элементы равны, используйте RPC \_ c \_ AUTHN \_ GSS \_ Kerberos или RPC \_ c \_ AUTHN \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776106"
---
# <a name="which-security-provider-to-use"></a><span data-ttu-id="c1ed8-103">Используемый поставщик безопасности</span><span class="sxs-lookup"><span data-stu-id="c1ed8-103">Which Security Provider to Use</span></span>

<span data-ttu-id="c1ed8-104">Все остальные элементы равны, используйте RPC \_ c \_ AUTHN \_ GSS \_ Kerberos или RPC \_ c \_ AUTHN \_ GSS \_ Negotiate.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-104">All other things being equal, use RPC\_C\_AUTHN\_GSS\_KERBEROS or RPC\_C\_AUTHN\_GSS\_NEGOTIATE.</span></span> <span data-ttu-id="c1ed8-105">Каждый из них предоставляет наиболее масштабируемую и безопасную службу.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-105">Each provides the most scalable and secure service.</span></span> <span data-ttu-id="c1ed8-106">При использовании RPC \_ C \_ AUTHN GSS \_ для \_ согласования на сервере это позволяет клиентам нижнего уровня, таким как клиенты NTLM, подключаться к серверу.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-106">If you use RPC\_C\_AUTHN\_GSS\_NEGOTIATE on the server, this allows down-level clients, such as NTLM clients, to connect to your server.</span></span> <span data-ttu-id="c1ed8-107">Если это нежелательно, либо Ограничьте выбор \_ только RPC C \_ AUTHN \_ GSS \_ только Kerberos, либо вызовите [**рпкбиндингинкаусклиентекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) , чтобы определить, какой поставщик безопасности используется клиентом, и отклоните доступ к клиентам, использующим NTLM.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-107">If that is undesirable, either limit the choice to RPC\_C\_AUTHN\_GSS\_KERBEROS only, or call [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to determine which security provider the client is using, and deny access to clients using NTLM.</span></span> <span data-ttu-id="c1ed8-108">Предпочтительным способом установки поставщика безопасности, используемого клиентом, является функция [**рпксерверинккаллаттрибутес**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .</span><span class="sxs-lookup"><span data-stu-id="c1ed8-108">The preferred method of establishing which security provider the client is using is the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function.</span></span>

 

 




