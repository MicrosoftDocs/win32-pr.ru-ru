---
title: Сведения об API узла устройства
description: API хоста устройств с технологией UPnP — это платформа для реализации функций устройств на основе UPnP на платформе Windows.
ms.assetid: fa716c59-d3f0-4cd4-b92d-939b258b0102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c751328696d6524208dc95a0b7961829f8ee231c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411286"
---
# <a name="about-the-device-host-api"></a><span data-ttu-id="3496b-103">Сведения об API узла устройства</span><span class="sxs-lookup"><span data-stu-id="3496b-103">About the Device Host API</span></span>

<span data-ttu-id="3496b-104">API хоста устройств с технологией UPnP — это платформа для реализации функций устройств на основе UPnP на платформе Windows.</span><span class="sxs-lookup"><span data-stu-id="3496b-104">The Device Host API with UPnP technology is a framework for implementing UPnP-based device functionality on the Windows platform.</span></span> <span data-ttu-id="3496b-105">Разработчики, создающие устройства с помощью API узла устройства с технологией UPnP (называемые [*размещенными устройствами*](h-gly.md)), должны только реализовать основные функциональные возможности устройства.</span><span class="sxs-lookup"><span data-stu-id="3496b-105">Developers who are creating devices by using the Device Host API with UPnP technology (referred to as [*hosted devices*](h-gly.md)) need only implement the device's core functionality.</span></span> <span data-ttu-id="3496b-106">Разработчики могут полагаться на узел устройства для работы с специфичными для UPnP сведениями об обнаружении, описании, управлении, событиях и презентации.</span><span class="sxs-lookup"><span data-stu-id="3496b-106">Developers can rely on the device host to handle the UPnP-specific details of discovery, description, control, eventing, and presentation.</span></span> <span data-ttu-id="3496b-107">Узел устройства проверяет входящие данные от клиентов, основанных на UPnP, и форматирует все исходящие данные с размещенных устройств в соответствии с архитектурой UPnP-устройств.</span><span class="sxs-lookup"><span data-stu-id="3496b-107">The device host validates incoming data from UPnP-based clients and formats all outgoing data from hosted devices according to the UPnP device architecture.</span></span>

<span data-ttu-id="3496b-108">В следующих разделах подробно описано, как работает узел устройств UPnP.</span><span class="sxs-lookup"><span data-stu-id="3496b-108">The following sections explain, in general, how the UPnP device host works:</span></span>

-   [<span data-ttu-id="3496b-109">Реализация размещенного устройства</span><span class="sxs-lookup"><span data-stu-id="3496b-109">Implementing a Hosted Device</span></span>](implementing-a-hosted-device.md)
-   [<span data-ttu-id="3496b-110">Регистрация размещенного устройства на узле устройства</span><span class="sxs-lookup"><span data-stu-id="3496b-110">Registering a Hosted Device with the Device Host</span></span>](registering-a-hosted-device-with-the-device-host.md)
-   [<span data-ttu-id="3496b-111">Поставщики устройств</span><span class="sxs-lookup"><span data-stu-id="3496b-111">Device Providers</span></span>](device-providers.md)
-   [<span data-ttu-id="3496b-112">Обработка событий</span><span class="sxs-lookup"><span data-stu-id="3496b-112">Eventing</span></span>](eventing.md)
-   [<span data-ttu-id="3496b-113">Уровень представления</span><span class="sxs-lookup"><span data-stu-id="3496b-113">Presentation</span></span>](presentation.md)

 

 




