---
title: Изменение наилучшего маршрута к сети
description: Изменение любого из следующих значений для лучшего маршрута к указанной целевой сети приводит к тому, что диспетчер таблиц маршрутизации создает уведомление, отправляемое каждому зарегистрированному клиенту и серверам пересылки.
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672125"
---
# <a name="changes-to-the-best-route-to-a-network"></a><span data-ttu-id="b504c-103">Изменение наилучшего маршрута к сети</span><span class="sxs-lookup"><span data-stu-id="b504c-103">Changes to the Best Route to a Network</span></span>

<span data-ttu-id="b504c-104">**Windows Server 2003:** Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b504c-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="b504c-105">Новые приложения должны использовать API диспетчера таблиц маршрутизации версии 2.</span><span class="sxs-lookup"><span data-stu-id="b504c-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="b504c-106">Изменение любого из следующих значений для лучшего маршрута к указанной целевой сети приводит к тому, что диспетчер таблиц маршрутизации создает сообщение уведомления, отправляемое каждому зарегистрированному клиенту и серверам пересылки:</span><span class="sxs-lookup"><span data-stu-id="b504c-106">A change in any of the following values for the best route to a given destination network causes the routing table manager to generate a notification message sent to each registered client and to the forwarders:</span></span>

-   <span data-ttu-id="b504c-107">Идентификатор протокола</span><span class="sxs-lookup"><span data-stu-id="b504c-107">Protocol identifier</span></span>
-   <span data-ttu-id="b504c-108">Индекс интерфейса</span><span class="sxs-lookup"><span data-stu-id="b504c-108">Interface index</span></span>
-   <span data-ttu-id="b504c-109">Адрес маршрутизатора следующего прыжка</span><span class="sxs-lookup"><span data-stu-id="b504c-109">Address of next-hop router</span></span>
-   <span data-ttu-id="b504c-110">Сведения о семействе протоколов, включающие метрики маршрута</span><span class="sxs-lookup"><span data-stu-id="b504c-110">Protocol family-specific data that includes route metrics</span></span>

<span data-ttu-id="b504c-111">Изменение в идентификаторе протокола, индексе интерфейса или адресе маршрутизатора следующего прыжка происходит при добавлении новой, более подходящей записи или в случае удаления или устаревания текущей записи наилучшего маршрута, а другой маршрут — в качестве нового лучшего маршрута.</span><span class="sxs-lookup"><span data-stu-id="b504c-111">A change in protocol identifier, interface index, or next-hop router address occurs when a new, better-route entry is added, or when the current best-route entry is deleted or aged out, and leaves another route as the new best route.</span></span>

 

 




