---
description: Поскольку дубликаты являются дескрипторами сокетов, а не базовыми сокетами, все состояния, связанные с сокетом, хранятся в общих пределах для всех дескрипторов.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Несколько дескрипторов для одного сокета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692278"
---
# <a name="multiple-handles-to-a-single-socket"></a><span data-ttu-id="cea91-103">Несколько дескрипторов для одного сокета</span><span class="sxs-lookup"><span data-stu-id="cea91-103">Multiple Handles to a Single Socket</span></span>

<span data-ttu-id="cea91-104">Поскольку дубликаты являются дескрипторами сокетов, а не базовыми сокетами, все состояния, связанные с сокетом, хранятся в общих пределах для всех дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="cea91-104">Since what are duplicated are the socket descriptors and not the underlying sockets, all of the states associated with a socket are held in common across all the descriptors.</span></span> <span data-ttu-id="cea91-105">Например, операция [**вспсетсоккопт**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) , выполняемая с помощью одного дескриптора, впоследствии отображается с помощью [**вспжетсоккопт**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) из дескрипторов или всех.</span><span class="sxs-lookup"><span data-stu-id="cea91-105">For example a [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) operation performed using one descriptor is subsequently visible using a [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) from any or all descriptors.</span></span>

<span data-ttu-id="cea91-106">Уведомления на общих сокетах подчиняются обычным ограничениям [**вспасинкселект**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) и [**вспевентселект**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cea91-106">Notification on shared sockets is subject to the usual constraints of [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="cea91-107">При выдаче любого из этих вызовов с помощью любого из общих дескрипторов отменяется любая предыдущая регистрация событий для сокета, независимо от того, какой дескриптор использовался для выполнения этой регистрации.</span><span class="sxs-lookup"><span data-stu-id="cea91-107">Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration.</span></span> <span data-ttu-id="cea91-108">Таким образом, нельзя было бы иметь возможность обрабатывать события «получить ДЕМОна \ \ \_ чтение» и «обработка б» на получение \_ событий записи.</span><span class="sxs-lookup"><span data-stu-id="cea91-108">Thus, for example, it would not be possible to have process A receive FD\_READ events and process B receive FD\_WRITE events.</span></span> <span data-ttu-id="cea91-109">В ситуациях, когда требуется такая тесная координация, рекомендуется, чтобы разработчики рассматривали использование потоков вместо отдельных процессов.</span><span class="sxs-lookup"><span data-stu-id="cea91-109">For situations when such tight coordination is required, it is suggested that developers consider using threads instead of separate processes.</span></span>

 

 
