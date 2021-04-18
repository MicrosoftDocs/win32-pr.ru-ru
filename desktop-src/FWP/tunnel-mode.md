---
title: Туннельный режим
description: Сценарий политики IPsec в туннельном режиме используется для применения защиты режима туннелирования IPsec для всего соответствующего трафика между двумя конечными точками туннеля.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331304"
---
# <a name="tunnel-mode"></a><span data-ttu-id="23bf7-103">Туннельный режим</span><span class="sxs-lookup"><span data-stu-id="23bf7-103">Tunnel Mode</span></span>

<span data-ttu-id="23bf7-104">Сценарий политики IPsec в туннельном режиме используется для применения защиты режима туннелирования IPsec для всего соответствующего трафика между двумя конечными точками туннеля.</span><span class="sxs-lookup"><span data-stu-id="23bf7-104">The Tunnel Mode IPsec policy scenario is used to apply IPsec tunnel mode protection for all matching traffic between two tunnel endpoints.</span></span>

<span data-ttu-id="23bf7-105">Этот сценарий политики обычно используется для защиты трафика между несколькими подсетями офиса филиала при пересылке между соответствующими шлюзами в Интернете.</span><span class="sxs-lookup"><span data-stu-id="23bf7-105">This policy scenario is typically used to protect traffic between multiple branch-office subnets, when it gets forwarded between the corresponding gateways on the Internet.</span></span> <span data-ttu-id="23bf7-106">Его также можно использовать для защиты сквозного обмена данными между двумя хост-компьютерами, которые также называются туннелями "точка — точка".</span><span class="sxs-lookup"><span data-stu-id="23bf7-106">It can also be used to secure end-to-end communication between two host machines, also referred to as point-to-point tunnels.</span></span>

<span data-ttu-id="23bf7-107">Чтобы реализовать политику режима туннелирования с помощью платформы фильтрации Windows (WFP), вызовите функцию [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) , которая создает экземпляры соответствующих фильтров туннельного режима на соответствующих уровнях от имени вызывающего.</span><span class="sxs-lookup"><span data-stu-id="23bf7-107">To implement Tunnel Mode policy using the Windows Filtering Platform (WFP), call the [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) function that instantiates the appropriate tunnel mode filters at the appropriate layers on behalf of the caller.</span></span> <span data-ttu-id="23bf7-108">Вызывающему объекту необходимо указать основной режим, контекст поставщика быстрого режима и условия фильтра, описывающие трафик, который должен быть защищен внутри туннеля.</span><span class="sxs-lookup"><span data-stu-id="23bf7-108">The caller needs to specify the Main Mode, Quick Mode provider contexts, and the filter conditions describing the traffic that should be secured inside the tunnel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23bf7-109">См. также</span><span class="sxs-lookup"><span data-stu-id="23bf7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23bf7-110">Пример кода: использование режима туннелирования</span><span class="sxs-lookup"><span data-stu-id="23bf7-110">Sample code: Using Tunnel Mode</span></span>](using-tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="23bf7-111">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="23bf7-111">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




