---
title: Транспортный режим обнаружения согласований в режиме границ
description: Режим транспорта обнаружения согласования в сценарии политики IPsec в режиме граничного режима запрашивает защиту режима транспорта IPsec для всего соответствующего трафика.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9f4168eee38165125c2455bc80dae29c1c6794
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487704"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a><span data-ttu-id="2fe2c-103">Транспортный режим обнаружения согласований в режиме границ</span><span class="sxs-lookup"><span data-stu-id="2fe2c-103">Negotiation Discovery Transport Mode in Boundary Mode</span></span>

<span data-ttu-id="2fe2c-104">Режим транспорта обнаружения согласования в сценарии политики IPsec в режиме граничного режима запрашивает защиту режима транспорта IPsec для всего соответствующего трафика.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-104">The Negotiation Discovery Transport Mode in Boundary Mode IPsec policy scenario requests IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="2fe2c-105">В случае сбоя согласования IKE/AuthIP для входящих и исходящих соединений разрешается переход на незашифрованный текст.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-105">If the IKE/AuthIP negotiation fails, both inbound and outbound connections are allowed to fallback to clear-text .</span></span>

<span data-ttu-id="2fe2c-106">Эта политика IPsec обычно используется на компьютерах, доступ к которым осуществляется на компьютерах с поддержкой IPsec и без IPsec.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-106">This IPsec policy is typically used on machines that are accessed by both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="2fe2c-107">Примером возможного режима транспорта обнаружения согласования является защита всего трафика одноадресных данных, за исключением ICMP, использование транспортного режима IPsec и Включение обнаружения согласований в режиме границ.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-107">An example of a potential Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode and enable negotiation discovery in boundary mode."</span></span>

<span data-ttu-id="2fe2c-108">Чтобы реализовать этот пример программно, используйте следующую конфигурацию платформы WFP.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="2fe2c-109">**В ФВПМ \_ Layer \_ IKEEXT \_ V {4 \| 6} Настройка политики согласования mm**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="2fe2c-110">Добавьте один или оба следующих контекста поставщика политики MM.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="2fe2c-111">Для IKE — контекст поставщика политики типа ФВПМ \_ IPSec \_ IKE \_ mm \_ .</span><span class="sxs-lookup"><span data-stu-id="2fe2c-111">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="2fe2c-112">Для AuthIP — контекст поставщика политики типа ФВПМ \_ IPSec \_ AuthIP \_ mm \_ .</span><span class="sxs-lookup"><span data-stu-id="2fe2c-112">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="2fe2c-113">Будет согласовываться общий модуль ключа, и будет применена соответствующая политика MM.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="2fe2c-114">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="2fe2c-115">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span>
    | <span data-ttu-id="2fe2c-116">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2fe2c-116">Filter property</span></span>        | <span data-ttu-id="2fe2c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2fe2c-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="2fe2c-118">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="2fe2c-118">Filtering conditions</span></span>   | <span data-ttu-id="2fe2c-119">Пустой.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-119">Empty.</span></span> <span data-ttu-id="2fe2c-120">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="2fe2c-121">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-121">**providerContextKey**</span></span> | <span data-ttu-id="2fe2c-122">Идентификатор GUID контекста поставщика MM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="2fe2c-123">**На уровне \_ фвпм \_ IPSec \_ V {4 \| 6} Настройка политики СОГЛАСОВАНия QM и EM**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="2fe2c-124">Добавьте один или оба следующих контекста поставщика политики транспортного режима QM и установите флаг [**политики IPSec « \_ \_ \_ ND \_ периметра**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) ».</span><span class="sxs-lookup"><span data-stu-id="2fe2c-124">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_BOUNDARY**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="2fe2c-125">Для IKE — контекст поставщика политики типа **фвпм \_ IPSec \_ IKE \_ QM \_ Transport \_**.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="2fe2c-126">Для AuthIP — контекст поставщика политики типа **фвпм \_ IPSec \_ AuthIP \_ QM \_ Transport \_**.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="2fe2c-127">Этот контекст может дополнительно содержать политику согласования расширенного режима AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="2fe2c-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="2fe2c-128">Будет выполнено согласование общего модуля ключа, и будет применена соответствующая политика QM.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="2fe2c-129">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="2fe2c-130">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span>
    | <span data-ttu-id="2fe2c-131">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2fe2c-131">Filter property</span></span>        | <span data-ttu-id="2fe2c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2fe2c-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="2fe2c-133">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="2fe2c-133">Filtering conditions</span></span>   | <span data-ttu-id="2fe2c-134">Пустой.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-134">Empty.</span></span> <span data-ttu-id="2fe2c-135">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="2fe2c-136">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-136">**providerContextKey**</span></span> | <span data-ttu-id="2fe2c-137">Идентификатор GUID контекста поставщика QM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="2fe2c-138">**На уровне \_ фвпм \_ входящий \_ транспорт \_ V {4 \| 6} Настройка входящих правил фильтрации для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="2fe2c-139">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-139">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="2fe2c-140">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2fe2c-140">Filter property</span></span>                                                   | <span data-ttu-id="2fe2c-141">Значение</span><span class="sxs-lookup"><span data-stu-id="2fe2c-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2fe2c-142">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="2fe2c-143">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2fe2c-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="2fe2c-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-144">**action.type**</span></span>                                                   | <span data-ttu-id="2fe2c-145">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="2fe2c-146">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="2fe2c-147">**ФВПМ \_ выноска \_ \_ входящего \_ транспорта IPSec \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="2fe2c-148">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="2fe2c-149">**\_Безопасность контекста фвпм \_ IPSec для \_ входящего \_ \_ подключения PERSIST \_**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="2fe2c-150">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="2fe2c-151">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2fe2c-151">Filter property</span></span>                                                   | <span data-ttu-id="2fe2c-152">Значение</span><span class="sxs-lookup"><span data-stu-id="2fe2c-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="2fe2c-153">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2fe2c-154">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2fe2c-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="2fe2c-155">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="2fe2c-156">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="2fe2c-157">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-157">**action.type**</span></span>                                                   | <span data-ttu-id="2fe2c-158">\_разрешение действия \_ FWP</span><span class="sxs-lookup"><span data-stu-id="2fe2c-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="2fe2c-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-159">**weight**</span></span>                                                        | [<span data-ttu-id="2fe2c-160">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="2fe2c-161">**На уровне \_ \_ исходящего \_ транспорта уровня фвпм \_ V {4 \| 6} Настройка правил фильтрации исходящих пакетов для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="2fe2c-162">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-162">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="2fe2c-163">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2fe2c-163">Filter property</span></span>                                                   | <span data-ttu-id="2fe2c-164">Значение</span><span class="sxs-lookup"><span data-stu-id="2fe2c-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2fe2c-165">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2fe2c-166">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2fe2c-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="2fe2c-167">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-167">**action.type**</span></span>                                                   | <span data-ttu-id="2fe2c-168">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="2fe2c-169">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="2fe2c-170">**\_Исходящий транспорт IPSec для фвпм выноски \_ \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="2fe2c-171">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="2fe2c-172">**ФВПМ \_ контекст \_ IPSec для \_ исходящей \_ согласованности \_ обнаружения**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="2fe2c-173">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="2fe2c-174">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2fe2c-174">Filter property</span></span>                                                   | <span data-ttu-id="2fe2c-175">Значение</span><span class="sxs-lookup"><span data-stu-id="2fe2c-175">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="2fe2c-176">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2fe2c-177">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2fe2c-177">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="2fe2c-178">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="2fe2c-179">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-179">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="2fe2c-180">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-180">**action.type**</span></span>                                                   | <span data-ttu-id="2fe2c-181">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-181">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="2fe2c-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-182">**weight**</span></span>                                                        | <span data-ttu-id="2fe2c-183">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

> [!Note]  
> <span data-ttu-id="2fe2c-184">В противоположность транспортному режиму обнаружения согласования для транспортного режима обнаружения согласования в политике режима границы нет необходимости добавлять фильтр на **уровне \_ фвпм \_ \_ проверки подлинности " \_ recv \_ Accept \_ V {4 \| 6}** ", так как эта политика разрешает входящие незащищенные соединения с открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="2fe2c-184">As opposed to Negotiation Discovery Transport Mode, for Negotiation Discovery Transport Mode in Boundary Mode policy there is no need to add a filter at the **FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}** layers because this policy allows inbound unprotected clear-text connections.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2fe2c-185">См. также</span><span class="sxs-lookup"><span data-stu-id="2fe2c-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fe2c-186">Пример кода: использование транспортного режима</span><span class="sxs-lookup"><span data-stu-id="2fe2c-186">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="2fe2c-187">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="2fe2c-187">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="2fe2c-188">**Встроенные идентификаторы выноски**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-188">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="2fe2c-189">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="2fe2c-189">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="2fe2c-190">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-190">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="2fe2c-191">**ФВПМ \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-191">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="2fe2c-192">**\_ \_ тип контекста поставщика \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="2fe2c-192">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

