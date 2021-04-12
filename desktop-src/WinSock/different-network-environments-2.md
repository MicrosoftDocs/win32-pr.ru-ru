---
description: Несколько сетевых сред влияют на поведение приложения в сети.
ms.assetid: 4a530a17-5e61-4730-95f5-233261b4ceb0
title: Разные сетевые среды
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dca7eacd48973a9106e6a1e3a4eb5959afcfef
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104273215"
---
# <a name="different-network-environments"></a><span data-ttu-id="df3d7-103">Разные сетевые среды</span><span class="sxs-lookup"><span data-stu-id="df3d7-103">Different Network Environments</span></span>

<span data-ttu-id="df3d7-104">Несколько сетевых сред влияют на поведение приложения в сети.</span><span class="sxs-lookup"><span data-stu-id="df3d7-104">Several network environments affect the networked behavior of an application.</span></span> <span data-ttu-id="df3d7-105">Свойства, отличающие сетевые среды, имеют низкую и высокую пропускную способность, а низкая и высокая.</span><span class="sxs-lookup"><span data-stu-id="df3d7-105">Properties that differentiate network environments include low versus high bandwidth, and low versus high RTT.</span></span> <span data-ttu-id="df3d7-106">Сетевые среды влияют на транзакционные и потоковые приложения различными способами.</span><span class="sxs-lookup"><span data-stu-id="df3d7-106">Network environments affect transactional and streaming applications in different ways.</span></span> <span data-ttu-id="df3d7-107">Транзакционные приложения более чувствительны к RTT; Потоковая передача приложений более важна для продуктов с задержкой пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="df3d7-107">Transactional applications are more sensitive to RTT; streaming applications are more sensitive to bandwidth-delay products.</span></span>

![Схема, показывающая, как различные сетевые среды влияют на поведение приложения в сети.](images/hperf-1.png)

<span data-ttu-id="df3d7-109">Коммутируемые сети и некоторые беспроводные сети имеют переменное время приема-передачи.</span><span class="sxs-lookup"><span data-stu-id="df3d7-109">Dial-up networks and some wireless networks have a variable RTT.</span></span> <span data-ttu-id="df3d7-110">У вспомогательных сетей обычно есть асимметричная пропускная способность между вышестоящей и нисходящей.</span><span class="sxs-lookup"><span data-stu-id="df3d7-110">Satellite networks generally have an asymmetric bandwidth between upstream and downstream.</span></span> <span data-ttu-id="df3d7-111">Беспроводные локальные сети и Ксдсл являются хорошим примером сетей с продуктами задержки пропускной способности, такими как Fast Ethernet.</span><span class="sxs-lookup"><span data-stu-id="df3d7-111">Wireless LAN and xDSL are good examples of networks with bandwidth-delay products similar to that of Fast Ethernet.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df3d7-112">См. также</span><span class="sxs-lookup"><span data-stu-id="df3d7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df3d7-113">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="df3d7-113">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="df3d7-114">Измерения производительности</span><span class="sxs-lookup"><span data-stu-id="df3d7-114">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



