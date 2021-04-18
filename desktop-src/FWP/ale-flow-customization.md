---
title: Настройка потока ALE
description: Сетевую фильтрацию на уровнях уровня приложения (ALE) для платформы фильтрации Windows (WFP) можно настроить, добавив фильтры с конкретными параметрами классификации.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104336452"
---
# <a name="ale-flow-customization"></a><span data-ttu-id="2d083-103">Настройка потока ALE</span><span class="sxs-lookup"><span data-stu-id="2d083-103">ALE Flow Customization</span></span>

<span data-ttu-id="2d083-104">Сетевую фильтрацию на уровнях уровня приложения (ALE) для платформы фильтрации Windows (WFP) можно настроить, добавив фильтры с конкретными параметрами классификации.</span><span class="sxs-lookup"><span data-stu-id="2d083-104">Network filtering at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) can be customized by adding filters with specific classify options.</span></span>

## <a name="multicastbroadcast-traffic"></a><span data-ttu-id="2d083-105">Многоадресный или широковещательный трафик</span><span class="sxs-lookup"><span data-stu-id="2d083-105">Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="2d083-106">Чтобы заблокировать входящий трафик на основе исходящих многоадресных или широковещательных состояний, добавьте фильтр, который разрешает исходящий трафик многоадресной и широковещательной рассылки и имеет параметр [**FWP \_ классификация \_ \_ многоадресного \_ состояния**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) , установленный в **\_ значение FWP параметр \_ \_ запретить \_ многоадресное \_ состояние**.</span><span class="sxs-lookup"><span data-stu-id="2d083-106">To block inbound traffic based on outbound multicast or broadcast states, add a filter that authorizes outbound multicast and broadcast traffic and that has the [**FWP\_CLASSIFY\_OPTION\_MULTICAST\_STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_DENY\_MULTICAST\_STATE**.</span></span>

## <a name="remote-peers"></a><span data-ttu-id="2d083-107">Удаленные одноранговые узлы</span><span class="sxs-lookup"><span data-stu-id="2d083-107">Remote Peers</span></span>

<span data-ttu-id="2d083-108">Чтобы добавить пакеты ответов из разных узлов в один и тот же поток ALE, добавьте фильтр, у которого параметр [**FWP \_ классифицировать \_ параметр \_ неплотного \_ \_ сопоставления источника**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) имеет значение **FWP \_ параметр \_ \_ включить \_ свободное \_ \_ Сопоставление источника**.</span><span class="sxs-lookup"><span data-stu-id="2d083-108">To add response packets from different peers to the same ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_LOOSE\_SOURCE\_MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_ENABLE\_LOOSE\_SOURCE\_MAPPING**.</span></span>

<span data-ttu-id="2d083-109">См. раздел [Использование параметров классификации](using-classify-options.md) для примера кода.</span><span class="sxs-lookup"><span data-stu-id="2d083-109">See [Using Classify Options](using-classify-options.md) for code sample.</span></span>

## <a name="ale-flow-lifetime"></a><span data-ttu-id="2d083-110">Время существования потока ALE</span><span class="sxs-lookup"><span data-stu-id="2d083-110">ALE Flow Lifetime</span></span>

<span data-ttu-id="2d083-111">Чтобы изменить значения времени ожидания простоя для потока ALE, добавьте фильтр с параметром [**FWP \_ классифицировать \_ \_ мкаст \_ бкаст \_ Lifetime**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) и/или в параметре FWP значение времени **\_ \_ \_ \_ жизни одноадресной рассылки** , равным требуемому значению времени ожидания простоя.</span><span class="sxs-lookup"><span data-stu-id="2d083-111">To modify the idle timeout values for an ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_MCAST\_BCAST\_LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option and/or the **FWP\_CLASSIFY\_OPTION\_UNICAST\_LIFETIME** option set to the desired idle timeout value.</span></span>

<span data-ttu-id="2d083-112">См. раздел [Использование параметров классификации](using-classify-options.md) для примера кода.</span><span class="sxs-lookup"><span data-stu-id="2d083-112">See [Using Classify Options](using-classify-options.md) for a code sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d083-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2d083-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d083-114">Принудительное применение уровня приложения (ALE)</span><span class="sxs-lookup"><span data-stu-id="2d083-114">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="2d083-115">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="2d083-115">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="2d083-116">Фильтрация с отслеживанием состояния ALE</span><span class="sxs-lookup"><span data-stu-id="2d083-116">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="2d083-117">Многоадресный или широковещательный трафик ALE</span><span class="sxs-lookup"><span data-stu-id="2d083-117">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="2d083-118">Повторная авторизация ALE</span><span class="sxs-lookup"><span data-stu-id="2d083-118">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="2d083-119">Использование параметров классификации</span><span class="sxs-lookup"><span data-stu-id="2d083-119">Using Classify Options</span></span>](using-classify-options.md)
</dt> </dl>

 

 




