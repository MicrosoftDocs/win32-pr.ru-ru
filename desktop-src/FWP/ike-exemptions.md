---
title: Исключения IKE/AuthIP
description: Для работы протокол IKE (IKE) и протокола IP с проверкой подлинности (AuthIP) необходимо исключить сетевой трафик из фильтрации IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412573"
---
# <a name="ikeauthip-exemptions"></a><span data-ttu-id="61e3e-103">Исключения IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="61e3e-103">IKE/AuthIP Exemptions</span></span>

<span data-ttu-id="61e3e-104">Для работы модулей ключей IPsec, протокол IKE (IKE) и протокола IP с проверкой подлинности (AuthIP) необходимо исключить сетевой трафик из фильтрации IPsec.</span><span class="sxs-lookup"><span data-stu-id="61e3e-104">The Internet Protocol security (IPsec) keying modules, Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP), in order to function, need to exempt their network traffic from the IPsec filtering.</span></span>

<span data-ttu-id="61e3e-105">В платформе фильтрации Windows (WFP) модуль базовой фильтрации (BFE) автоматически добавляет фильтры исключения IKE и AuthIP при добавлении первого фильтра политики IKE или AuthIP (MM) и удаляет их при удалении последнего фильтра политики IKE или AuthIP MM.</span><span class="sxs-lookup"><span data-stu-id="61e3e-105">In Windows Filtering Platform (WFP) the Base Filtering Engine (BFE) automatically adds IKE and AuthIP exemption filters when the first IKE or AuthIP main mode (MM) policy filter is added and deletes them when the last IKE or AuthIP MM policy filter is deleted.</span></span> <span data-ttu-id="61e3e-106">Таким образом поставщики политик не должны управлять исключениями фильтрации IKE и AuthIP по отдельности.</span><span class="sxs-lookup"><span data-stu-id="61e3e-106">This way, the policy providers do not have to manage IKE and AuthIP filtering exemptions individually.</span></span>

<span data-ttu-id="61e3e-107">Фильтр политики IKE MM — это фильтр в [**фвпм \_ слоя ядра \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , который ссылается на контекст поставщика в [**контексте типа фвпм \_ IPSec \_ IKE \_ mm \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="61e3e-107">An IKE MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_IKE\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="61e3e-108">Фильтр политики AuthIP MM — это фильтр в Фвпм слоя подсистемы уровня ядра [**\_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , который ссылается на контекст поставщика в [**контексте типа фвпм \_ IPSec \_ AuthIP \_ mm \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="61e3e-108">An AuthIP MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="61e3e-109">Фильтр исключения IKE или AuthIP — это фильтр на уровне модуля [**фвпм " \_ \_ входящий \_ транспорт \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) или **фвпм" \_ \_ исходящий транспорт v \_ {4 \_ \| 6}** с автоматической плотностью в диапазоне весовых коэффициентов [**\_ \_ \_ \_ исключения IKE диапазона фвпм**](filter-weight-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="61e3e-109">An IKE or AuthIP exemption filter is a filter in the engine layer [**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}**](management-filtering-layer-identifiers-.md) or **FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}** auto-weighted in the [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md) weight range.</span></span>

<span data-ttu-id="61e3e-110">Исключения IKE и AuthIP, реализованные с помощью BFE, приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="61e3e-110">The IKE and AuthIP exemptions implemented by BFE are as follows.</span></span>

| <span data-ttu-id="61e3e-111">Версия IP</span><span class="sxs-lookup"><span data-stu-id="61e3e-111">IP version</span></span>      | <span data-ttu-id="61e3e-112">Порт</span><span class="sxs-lookup"><span data-stu-id="61e3e-112">Port</span></span>                        | <span data-ttu-id="61e3e-113">Исключение</span><span class="sxs-lookup"><span data-stu-id="61e3e-113">Exemption</span></span>                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e3e-114">IPv4</span><span class="sxs-lookup"><span data-stu-id="61e3e-114">IPv4</span></span><br/> | <span data-ttu-id="61e3e-115">UDP: 500 UDP: 4500</span><span class="sxs-lookup"><span data-stu-id="61e3e-115">UDP:500 UDP:4500</span></span><br/> | <span data-ttu-id="61e3e-116">Разрешите трафик IKE и AuthIP на входящем транспортном уровне и на исходящем транспортном уровне.</span><span class="sxs-lookup"><span data-stu-id="61e3e-116">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="61e3e-117">Разрешите трафик IKE и AuthIP на уровнях получения, принятия и подключения ALE, но ограничьте его локальной системой.</span><span class="sxs-lookup"><span data-stu-id="61e3e-117">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |
| <span data-ttu-id="61e3e-118">IPv6;</span><span class="sxs-lookup"><span data-stu-id="61e3e-118">IPv6</span></span><br/> | <span data-ttu-id="61e3e-119">UDP: 500</span><span class="sxs-lookup"><span data-stu-id="61e3e-119">UDP:500</span></span><br/>          | <span data-ttu-id="61e3e-120">Разрешите трафик IKE и AuthIP на входящем транспортном уровне и на исходящем транспортном уровне.</span><span class="sxs-lookup"><span data-stu-id="61e3e-120">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="61e3e-121">Разрешите трафик IKE и AuthIP на уровнях получения, принятия и подключения ALE, но ограничьте его локальной системой.</span><span class="sxs-lookup"><span data-stu-id="61e3e-121">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |



 

<span data-ttu-id="61e3e-122">Фильтры исключения IKE и AuthIP открыты для всех адресов.</span><span class="sxs-lookup"><span data-stu-id="61e3e-122">The IKE and AuthIP exemption filters are open to all addresses.</span></span> <span data-ttu-id="61e3e-123">Чтобы реализовать брандмауэр с более детализированным контролем, поставщики политик должны добавить фильтры в диапазоне веса выше, чем [**фвпм с \_ диапазоном весовых коэффициентов \_ \_ IKE \_**](filter-weight-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="61e3e-123">To implement a firewall with more granular control, policy providers should add filters in a weight range higher than [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61e3e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="61e3e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61e3e-125">Конфигурация IPsec</span><span class="sxs-lookup"><span data-stu-id="61e3e-125">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="61e3e-126">Назначение весов фильтрам</span><span class="sxs-lookup"><span data-stu-id="61e3e-126">Filter Weight Assignment</span></span>](filter-weight-assignment.md)
</dt> </dl>

 

 





