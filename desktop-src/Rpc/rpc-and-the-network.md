---
title: RPC и сеть
description: В этом разделе рассматривается работа с сетью унрелиабилити при использовании RPC и объясняется, как интерфейсы API уровня RPC преобразуются в сетевые операции. Раздел относится только к \_ \_ \_ последовательностью протокола HTTP нкакн IP TCP и нкакн.
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- Удаленный вызов процедур RPC, рекомендации, RPC и сеть
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134330"
---
# <a name="rpc-and-the-network"></a><span data-ttu-id="b08b0-105">RPC и сеть</span><span class="sxs-lookup"><span data-stu-id="b08b0-105">RPC and the Network</span></span>

<span data-ttu-id="b08b0-106">В этом разделе рассматривается работа с сетью унрелиабилити при использовании RPC и объясняется, как интерфейсы API уровня RPC преобразуются в сетевые операции.</span><span class="sxs-lookup"><span data-stu-id="b08b0-106">This section discusses how to deal with network unreliability when using RPC, and explains how RPC-level APIs translate into network activity.</span></span> <span data-ttu-id="b08b0-107">Раздел относится только к последовательностью протокола [**\_ http**](/windows/desktop/Midl/ncacn-http) [**нкакн \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) и нкакн.</span><span class="sxs-lookup"><span data-stu-id="b08b0-107">The section refers only to the [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) and [**ncacn\_http**](/windows/desktop/Midl/ncacn-http) protocol sequences.</span></span>

<span data-ttu-id="b08b0-108">Этот раздел состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="b08b0-108">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="b08b0-109">Разработка и развертывание в сети</span><span class="sxs-lookup"><span data-stu-id="b08b0-109">Development Versus Deployment in the Network</span></span>](development-versus-deployment-in-the-network.md)
-   [<span data-ttu-id="b08b0-110">Предотвращение Client-Side зависаний</span><span class="sxs-lookup"><span data-stu-id="b08b0-110">Preventing Client-Side Hangs</span></span>](preventing-client-side-hangs.md)
-   [<span data-ttu-id="b08b0-111">Управление наборами сетевых подключений (ассоциациями)</span><span class="sxs-lookup"><span data-stu-id="b08b0-111">Managing Network Connection Sets (Associations)</span></span>](managing-network-connection-sets-associations-.md)
-   [<span data-ttu-id="b08b0-112">Очистка бездействующего подключения</span><span class="sxs-lookup"><span data-stu-id="b08b0-112">Idle Connection Cleanup</span></span>](idle-connection-cleanup.md)
-   [<span data-ttu-id="b08b0-113">Работа с потерей подключения</span><span class="sxs-lookup"><span data-stu-id="b08b0-113">Dealing with Loss of Connectivity</span></span>](dealing-with-loss-of-connectivity.md)
-   [<span data-ttu-id="b08b0-114">Очистка на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="b08b0-114">Server Side Cleanup</span></span>](server-side-cleanup.md)

 

 