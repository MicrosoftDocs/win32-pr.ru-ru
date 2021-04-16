---
description: 32.dll Ws2 \_ (и многоуровневые протоколы) будут вызывать вспклеануп один раз для каждого вызова вспстартуп.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Очистка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692305"
---
# <a name="cleanup"></a><span data-ttu-id="aa523-103">Очистка</span><span class="sxs-lookup"><span data-stu-id="aa523-103">Cleanup</span></span>

<span data-ttu-id="aa523-104">32.dll Ws2 \_ (и многоуровневые протоколы) будут вызывать [**вспклеануп**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) один раз для каждого вызова [**вспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="aa523-104">The Ws2\_32.dll (and layered protocols) will call [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) once for each invocation of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span> <span data-ttu-id="aa523-105">При каждом вызове **вспклеануп** должен уменьшить счетчик ссылок на процесс, а когда счетчик достигнет нуля, поставщик услуг должен подготовиться к выгрузке из памяти.</span><span class="sxs-lookup"><span data-stu-id="aa523-105">On each invocation, **WSPCleanup** should decrement a per-process reference counter, and when the counter reaches zero, the service provider must prepare itself to be unloaded from memory.</span></span> <span data-ttu-id="aa523-106">Первый способ — завершить передачу неотправленных данных на сокеты, настроенные для корректного закрытия.</span><span class="sxs-lookup"><span data-stu-id="aa523-106">The first order of business is to finish transmitting any unsent data on sockets that are configured for a graceful close.</span></span> <span data-ttu-id="aa523-107">После этого все ресурсы, удерживаемые поставщиком, будут освобождены.</span><span class="sxs-lookup"><span data-stu-id="aa523-107">Thereafter, any and all resources held by the provider are to be freed.</span></span> <span data-ttu-id="aa523-108">Поставщик услуг должен оставаться в состоянии, где его можно немедленно повторно инициализировать с помощью вызова **вспстартуп**.</span><span class="sxs-lookup"><span data-stu-id="aa523-108">The service provider must be left in a state where it can be immediately reinitialized by a call to **WSPStartup**.</span></span>

 

 
