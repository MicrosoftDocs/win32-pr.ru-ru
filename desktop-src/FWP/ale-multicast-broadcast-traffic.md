---
title: Многоадресный или широковещательный трафик ALE
description: Весь входящий многоадресный и широковещательный трафик на уровнях применения уровня приложения (ALE) сопоставляется с одним глобальным потоком ALE.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329707"
---
# <a name="ale-multicastbroadcast-traffic"></a><span data-ttu-id="2556d-103">Многоадресный или широковещательный трафик ALE</span><span class="sxs-lookup"><span data-stu-id="2556d-103">ALE Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="2556d-104">Весь входящий многоадресный и широковещательный трафик на уровнях применения уровня приложения (ALE) сопоставляется с одним глобальным [потоком ALE](ale-stateful-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="2556d-104">All inbound multicast and broadcast traffic at the Application Layer Enforcement (ALE) layers is mapped to one global [ALE flow](ale-stateful-filtering.md).</span></span> <span data-ttu-id="2556d-105">Трафик ответа для входящих многоадресных и широковещательных пакетов классифицируется на уровне [**\_ \_ \_ проверки подлинности \_ подключения ALE \_ V {4 \| 6} уровня фвпм**](management-filtering-layer-identifiers-.md) , и для каждого ответа создаются отдельные потоки Ale.</span><span class="sxs-lookup"><span data-stu-id="2556d-105">Response traffic for inbound multicast and broadcast packets is classified at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and separate ALE flows are created for each response.</span></span>

<span data-ttu-id="2556d-106">Исходящий трафик многоадресной и широковещательной рассылки на уровнях ALE создает 4-секундный поток ALE.</span><span class="sxs-lookup"><span data-stu-id="2556d-106">Outbound multicast and broadcast traffic at the ALE layers creates a 4-second ALE flow.</span></span> <span data-ttu-id="2556d-107">По умолчанию проверка подлинности исходящего пакета ALE или многоадресной рассылки будет разрешать входящий трафик, будь то одноадресный, многоадресный или широковещательный, с любого удаленного адреса в течение 4 секунд.</span><span class="sxs-lookup"><span data-stu-id="2556d-107">By default, the authorization of an outbound multicast or broadcast ALE packet will permit inbound traffic, whether unicast, multicast, or broadcast, from any remote address for up to 4 seconds.</span></span> <span data-ttu-id="2556d-108">Такой поток ALE может обновляться или храниться только при последующем исходящем трафике, соответствующем потоку ALE.</span><span class="sxs-lookup"><span data-stu-id="2556d-108">Such an ALE flow can only be refreshed or kept alive by subsequent outbound traffic that matches the ALE flow.</span></span>

> [!Note]  
> <span data-ttu-id="2556d-109">Время существования, равное 4 секундам, определяется встроенным [**\_ вызываемым выноски фвпм \_ параметры SET Authentication \_ \_ \_ Connect \_ Layer \_ V {4 \| 6}**](built-in-callout-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="2556d-109">The 4-second lifetime is specified by the built-in callout [**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}**](built-in-callout-identifiers.md).</span></span> <span data-ttu-id="2556d-110">Чтобы изменить время существования по умолчанию — 4 секунды, добавьте фильтр, ссылающийся на **фвпм \_ выноски \_ \_ Параметры Authentication \_ \_ Connect \_ Layer \_ V {4 \| 6}** .</span><span class="sxs-lookup"><span data-stu-id="2556d-110">To alter the 4-second default lifetime, add a filter that references the **FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}** callout.</span></span> <span data-ttu-id="2556d-111">Дополнительные сведения см. в разделе [Настройка потока ALE](ale-flow-customization.md) .</span><span class="sxs-lookup"><span data-stu-id="2556d-111">See [ALE Flow Customization](ale-flow-customization.md) for more information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2556d-112">См. также</span><span class="sxs-lookup"><span data-stu-id="2556d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2556d-113">Принудительное применение уровня приложения (ALE)</span><span class="sxs-lookup"><span data-stu-id="2556d-113">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="2556d-114">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="2556d-114">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="2556d-115">Фильтрация с отслеживанием состояния ALE</span><span class="sxs-lookup"><span data-stu-id="2556d-115">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="2556d-116">Повторная авторизация ALE</span><span class="sxs-lookup"><span data-stu-id="2556d-116">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="2556d-117">Настройка потока ALE</span><span class="sxs-lookup"><span data-stu-id="2556d-117">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 




