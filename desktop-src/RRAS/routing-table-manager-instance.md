---
title: Экземпляр диспетчера таблиц маршрутизации
description: Экземпляр — это отдельная таблица, используемая диспетчером таблиц маршрутизации для обслуживания сведений маршрутизации о подмножестве интерфейсов.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067876"
---
# <a name="routing-table-manager-instance"></a><span data-ttu-id="270b7-103">Экземпляр диспетчера таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="270b7-103">Routing Table Manager Instance</span></span>

<span data-ttu-id="270b7-104">Экземпляр — это отдельная таблица, используемая диспетчером таблиц маршрутизации для обслуживания сведений маршрутизации о подмножестве интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="270b7-104">An instance is a separate table that the routing table manager uses to maintain routing information about a subset of interfaces.</span></span> <span data-ttu-id="270b7-105">Экземпляры обычно используются, чтобы позволить физическому маршрутизатору действовать как набор виртуальных маршрутизаторов — по одному виртуальному маршрутизатору на логическую сеть.</span><span class="sxs-lookup"><span data-stu-id="270b7-105">Instances are typically used to enable a physical router to act as a set of virtual routers – one virtual router per logical network.</span></span>

<span data-ttu-id="270b7-106">В настоящее время диспетчер таблиц маршрутизации поддерживает только один экземпляр (по умолчанию равен нулю).</span><span class="sxs-lookup"><span data-stu-id="270b7-106">Currently, the routing table manager supports only one instance (identified as zero, the default).</span></span> <span data-ttu-id="270b7-107">Клиент может зарегистрироваться в других экземплярах, но ни один из виртуальных маршрутизаторов, кроме значения по умолчанию, распознается или используется диспетчером маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="270b7-107">The client can register with other instances, but no virtual router except the default one is recognized or used by the router manager.</span></span>

 

 




