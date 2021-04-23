---
title: Выбор уровня проверки подлинности
description: При выборе уровня проверки подлинности используйте следующие рекомендации.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486737"
---
# <a name="choosing-an-authentication-level"></a><span data-ttu-id="cb894-103">Выбор уровня проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="cb894-103">Choosing an Authentication Level</span></span>

<span data-ttu-id="cb894-104">При выборе уровня проверки подлинности используйте следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="cb894-104">When choosing an authentication level, use the following guideline.</span></span> <span data-ttu-id="cb894-105">Если не имеет значения, могут ли передаваемые данные перехватываться и изменяться, а полученные данные можно перехватывать или изменять, используйте RPC \_ C \_ AUTHN \_ Level \_ None, который является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb894-105">If it does not matter whether the data being sent can be intercepted and modified, and the data received can be intercepted or modified, use RPC\_C\_AUTHN\_LEVEL\_NONE, which is the default.</span></span> <span data-ttu-id="cb894-106">Если данные не должны изменяться, а частные данные не отправляются и не принимаются, \_ Используйте \_ \_ целостность PKT на уровне RPC C AUTHN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cb894-106">If the data should not be modified, and private data is not being sent or received, use RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY.</span></span> <span data-ttu-id="cb894-107">Во всех остальных случаях используйте безопасность RPC \_ C \_ AUTHN \_ Level \_ PKT \_ .</span><span class="sxs-lookup"><span data-stu-id="cb894-107">In all other cases, use RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

<span data-ttu-id="cb894-108">Не используйте \_ \_ параметры по умолчанию на уровне RPC c AUTHN \_ \_ , RPC \_ c \_ AUTHN \_ \_ Connect, RPC \_ c \_ AUTHN Level \_ \_ или \_ RPC \_ c \_ AUTHN \_ Pkt.</span><span class="sxs-lookup"><span data-stu-id="cb894-108">Do not use RPC\_C\_AUTHN\_LEVEL\_DEFAULT, RPC\_C\_AUTHN\_LEVEL\_CONNECT, RPC\_C\_AUTHN\_LEVEL\_CALL or RPC\_C\_AUTHN\_LEVEL\_PKT.</span></span> <span data-ttu-id="cb894-109">Сложный злоумышленник может разрушить эти уровни проверки подлинности и визуализировать их неэффективно.</span><span class="sxs-lookup"><span data-stu-id="cb894-109">A sophisticated attacker can break these authentication levels and render them ineffective.</span></span> <span data-ttu-id="cb894-110">Каждый из этих уровней усложняет работу злоумышленника для перехвата и изменения данных, а также для олицетворения, но безопасность на самом деле не достигается.</span><span class="sxs-lookup"><span data-stu-id="cb894-110">Each of these levels does make it slightly more difficult for an attacker to intercept and modify data, and to impersonate, but security is not really achieved.</span></span> <span data-ttu-id="cb894-111">Поскольку уровень сложности злоумышленника является редко известным, это не является разумным выбором.</span><span class="sxs-lookup"><span data-stu-id="cb894-111">Since the sophistication level of an attacker is rarely known, these are not wise choices.</span></span>

 

 




