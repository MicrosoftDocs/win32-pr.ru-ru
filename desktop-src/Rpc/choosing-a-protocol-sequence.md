---
title: Выбор последовательности протокола
description: Рекомендации по выбору последовательности протоколов предполагают использование нкакн \_ IP \_ TCP и нкалрпк, а не нкакн \_ NP, нкакн \_ SPX и нкадг \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3dea44868b96361ccaddc6e339f94fde92704f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070537"
---
# <a name="choosing-a-protocol-sequence"></a><span data-ttu-id="2cb39-103">Выбор последовательности протокола</span><span class="sxs-lookup"><span data-stu-id="2cb39-103">Choosing a Protocol Sequence</span></span>

<span data-ttu-id="2cb39-104">**Рекомендации:** При удаленном вызове используйте [**нкакн \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) .</span><span class="sxs-lookup"><span data-stu-id="2cb39-104">**Best practice:** Use [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) when making a remote call.</span></span> <span data-ttu-id="2cb39-105">Используйте [**нкалрпк**](/windows/desktop/Midl/ncalrpc) для локальных вызовов.</span><span class="sxs-lookup"><span data-stu-id="2cb39-105">Use [**ncalrpc**](/windows/desktop/Midl/ncalrpc) for local calls.</span></span> <span data-ttu-id="2cb39-106">Не используйте [**нкакн \_ NP**](/windows/desktop/Midl/ncacn-np), [**нкакн \_ SPX**](/windows/desktop/Midl/ncacn-spx)или любую из последовательностей протокола **нкадг \_ \*** . они менее эффективны и имеют более низкий уровень возможностей.</span><span class="sxs-lookup"><span data-stu-id="2cb39-106">Do not use [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), [**ncacn\_spx**](/windows/desktop/Midl/ncacn-spx), or any of the **ncadg\_\*** protocol sequences; they are less efficient and have inferior capabilities.</span></span>

 

 