---
title: Реализация размещенного устройства
description: 'Узел устройства с технологией UPnP реализует основные протоколы UPnP: обнаружение, описание, управление и события.'
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779112"
---
# <a name="implementing-a-hosted-device"></a><span data-ttu-id="87121-103">Реализация размещенного устройства</span><span class="sxs-lookup"><span data-stu-id="87121-103">Implementing a Hosted Device</span></span>

<span data-ttu-id="87121-104">Узел устройства с технологией UPnP реализует основные протоколы UPnP: обнаружение, описание, управление и события.</span><span class="sxs-lookup"><span data-stu-id="87121-104">The device host with UPnP technology implements the core UPnP protocols: discovery, description, control, and eventing.</span></span> <span data-ttu-id="87121-105">Разработчик, реализующий размещенное устройство, должен предоставить:</span><span class="sxs-lookup"><span data-stu-id="87121-105">The developer who implements a hosted device only needs to provide:</span></span>

-   <span data-ttu-id="87121-106">Описание устройства и его служб.</span><span class="sxs-lookup"><span data-stu-id="87121-106">A description of the device and its services.</span></span>
-   <span data-ttu-id="87121-107">Реализация функциональности устройства.</span><span class="sxs-lookup"><span data-stu-id="87121-107">An implementation of the device's functionality.</span></span>

<span data-ttu-id="87121-108">Например, разработчик устройства для работы с часами должен предоставлять для него описания устройств и служб на основе UPnP, а также реализацию функций часов (таких как время, Настройка времени и реагирование на запросы в течение текущего времени).</span><span class="sxs-lookup"><span data-stu-id="87121-108">For example, the developer of a clock device must provide UPnP-based device and service descriptions for it, and an implementation of the clock functions (such as keeping time, setting time, and responding to queries for the current time).</span></span> <span data-ttu-id="87121-109">Узел устройства:</span><span class="sxs-lookup"><span data-stu-id="87121-109">The device host:</span></span>

-   <span data-ttu-id="87121-110">Объявляет об устройстве в соответствии с протоколом обнаружения UPnP.</span><span class="sxs-lookup"><span data-stu-id="87121-110">Announces the device according to the UPnP discovery protocol.</span></span>
-   <span data-ttu-id="87121-111">Реагирует на запросы для описания устройства.</span><span class="sxs-lookup"><span data-stu-id="87121-111">Responds to queries for the device's description.</span></span>
-   <span data-ttu-id="87121-112">Направляет запросы на управление в часть кода устройства, реализующего функции часов.</span><span class="sxs-lookup"><span data-stu-id="87121-112">Routes control requests to the part of the device's code that implements the clock functions.</span></span>
-   <span data-ttu-id="87121-113">Поддерживает подписки на события служб.</span><span class="sxs-lookup"><span data-stu-id="87121-113">Maintains event subscriptions to services.</span></span>
-   <span data-ttu-id="87121-114">Отправляет уведомления о событиях подписчикам при изменении состояния службы.</span><span class="sxs-lookup"><span data-stu-id="87121-114">Sends event notifications to subscribers when the service's state changes.</span></span>

 

 




