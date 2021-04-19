---
title: Транспортный режим обнаружения согласований
description: Для сценария политики IPsec "режим транспорта обнаружения согласования" требуется защита режима транспорта IPsec для всего соответствующего входящего трафика и запрос защиты IPsec для сопоставления исходящего трафика.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216fec869eca28dc0661a37d44cce3a1fd05b80a
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314817"
---
# <a name="negotiation-discovery-transport-mode"></a><span data-ttu-id="06a41-103">Транспортный режим обнаружения согласований</span><span class="sxs-lookup"><span data-stu-id="06a41-103">Negotiation Discovery Transport Mode</span></span>

<span data-ttu-id="06a41-104">Для сценария политики IPsec "режим транспорта обнаружения согласования" требуется защита режима транспорта IPsec для всего соответствующего входящего трафика и запрос защиты IPsec для сопоставления исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="06a41-104">The Negotiation Discovery Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching inbound traffic, and requests IPsec protection for matching outbound traffic.</span></span> <span data-ttu-id="06a41-105">Поэтому исходящие подключения могут переключаться на незашифрованный текст, а входящие — нет.</span><span class="sxs-lookup"><span data-stu-id="06a41-105">Therefore, outbound connections are allowed to fallback to clear-text while inbound connections are not.</span></span>

<span data-ttu-id="06a41-106">Если эта политика используется, когда хост-компьютер пытается создать новое исходящее подключение и отсутствует существующее сопоставление безопасности IPsec, соответствующее этому трафику, узел отправляет пакеты в виде открытого текста и запускает согласование IKE или AuthIP.</span><span class="sxs-lookup"><span data-stu-id="06a41-106">With this policy, when the host machine attempts a new outbound connection and there is no existing IPsec SA matching the traffic, the host simultaneously sends the packets in clear-text and starts an IKE or AuthIP negotiation.</span></span> <span data-ttu-id="06a41-107">В случае успешности согласования подключение обновляется до защищенного IPsec.</span><span class="sxs-lookup"><span data-stu-id="06a41-107">If the negotiation succeeds, the connection is upgraded to IPsec-protected.</span></span> <span data-ttu-id="06a41-108">В противном случае соединение остается в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="06a41-108">Otherwise, the connection stays in clear-text.</span></span> <span data-ttu-id="06a41-109">После защиты с помощью IPsec соединение не может быть переустановлено на незашифрованный текст.</span><span class="sxs-lookup"><span data-stu-id="06a41-109">Once IPsec-protected, a connection can never be downgraded to clear-text.</span></span>

<span data-ttu-id="06a41-110">Транспортный режим обнаружения согласований обычно используется в средах, в которых используются компьютеры с поддержкой IPsec и без IPsec.</span><span class="sxs-lookup"><span data-stu-id="06a41-110">Negotiation Discovery Transport Mode is typically used in environments that include both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="06a41-111">Пример возможных режимов транспортного режима обнаружения согласования: "защита всего трафика одноадресных данных, за исключением ICMP, использование транспортного режима IPsec и Включение обнаружения согласований".</span><span class="sxs-lookup"><span data-stu-id="06a41-111">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, and enable negotiation discovery."</span></span>

<span data-ttu-id="06a41-112">Чтобы реализовать этот пример программно, используйте следующую конфигурацию платформы WFP.</span><span class="sxs-lookup"><span data-stu-id="06a41-112">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="06a41-113">**В ФВПМ \_ слоя \_ " \_ V {4 \| 6} Настройка политики согласования mm"**</span><span class="sxs-lookup"><span data-stu-id="06a41-113">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} set up MM negotiation policy**</span></span>  

1.  <span data-ttu-id="06a41-114">Добавьте один или оба следующих контекста поставщика политики MM.</span><span class="sxs-lookup"><span data-stu-id="06a41-114">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="06a41-115">Для IKE — контекст поставщика политики типа **фвпм \_ IPSec \_ IKE \_ mm \_**.</span><span class="sxs-lookup"><span data-stu-id="06a41-115">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="06a41-116">Для AuthIP — контекст поставщика политики типа **фвпм \_ IPSec \_ AuthIP \_ mm \_**.</span><span class="sxs-lookup"><span data-stu-id="06a41-116">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="06a41-117">Будет согласовываться общий модуль ключа, и будет применена соответствующая политика MM.</span><span class="sxs-lookup"><span data-stu-id="06a41-117">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="06a41-118">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="06a41-118">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="06a41-119">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="06a41-119">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="06a41-120">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="06a41-120">Filter property</span></span>        | <span data-ttu-id="06a41-121">Значение</span><span class="sxs-lookup"><span data-stu-id="06a41-121">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="06a41-122">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="06a41-122">Filtering conditions</span></span>   | <span data-ttu-id="06a41-123">Пустой.</span><span class="sxs-lookup"><span data-stu-id="06a41-123">Empty.</span></span> <span data-ttu-id="06a41-124">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="06a41-124">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="06a41-125">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="06a41-125">**providerContextKey**</span></span> | <span data-ttu-id="06a41-126">Идентификатор GUID контекста поставщика MM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="06a41-126">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="06a41-127">**На уровне \_ фвпм \_ IPSec \_ V {4 \| 6} Настройте политику СОГЛАСОВАНия QM и EM**</span><span class="sxs-lookup"><span data-stu-id="06a41-127">**At FWPM\_LAYER\_IPSEC\_V{4\|6} set up QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="06a41-128">Добавьте один или оба следующих контекста поставщика политики транспортного режима QM и установите флаг [**\_ политики IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="06a41-128">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="06a41-129">Для IKE — контекст поставщика политики типа ФВПМ \_ IPSec \_ IKE \_ QM \_ Transport \_ .</span><span class="sxs-lookup"><span data-stu-id="06a41-129">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT.</span></span>
    -   <span data-ttu-id="06a41-130">Для AuthIP — контекст поставщика политики типа ФВПМ \_ IPSec \_ AuthIP \_ QM \_ Transport \_ .</span><span class="sxs-lookup"><span data-stu-id="06a41-130">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT.</span></span> <span data-ttu-id="06a41-131">Этот контекст может дополнительно содержать политику согласования расширенного режима AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="06a41-131">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="06a41-132">Будет выполнено согласование общего модуля ключа, и будет применена соответствующая политика QM.</span><span class="sxs-lookup"><span data-stu-id="06a41-132">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="06a41-133">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="06a41-133">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="06a41-134">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="06a41-134">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="06a41-135">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="06a41-135">Filter property</span></span>        | <span data-ttu-id="06a41-136">Значение</span><span class="sxs-lookup"><span data-stu-id="06a41-136">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="06a41-137">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="06a41-137">Filtering conditions</span></span>   | <span data-ttu-id="06a41-138">Пустой.</span><span class="sxs-lookup"><span data-stu-id="06a41-138">Empty.</span></span> <span data-ttu-id="06a41-139">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="06a41-139">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="06a41-140">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="06a41-140">**providerContextKey**</span></span> | <span data-ttu-id="06a41-141">Идентификатор GUID контекста поставщика QM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="06a41-141">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="06a41-142">**На \_ \_ входящем \_ транспортном транспорте уровня фвпм \_ V {4 \| 6} Настройте правила фильтрации входящих пакетов.**</span><span class="sxs-lookup"><span data-stu-id="06a41-142">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} set up inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="06a41-143">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="06a41-143">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="06a41-144">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="06a41-144">Filter property</span></span>                                                   | <span data-ttu-id="06a41-145">Значение</span><span class="sxs-lookup"><span data-stu-id="06a41-145">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="06a41-146">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-146">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="06a41-147">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="06a41-147">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="06a41-148">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="06a41-148">**action.type**</span></span>                                                   | <span data-ttu-id="06a41-149">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="06a41-149">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="06a41-150">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="06a41-150">**action.calloutKey**</span></span>                                             | <span data-ttu-id="06a41-151">**ФВПМ \_ выноска \_ \_ входящего \_ транспорта IPSec \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="06a41-151">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="06a41-152">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="06a41-152">**rawContext**</span></span>                                                    | [<span data-ttu-id="06a41-153">**\_Безопасность контекста фвпм \_ IPSec для \_ входящего \_ \_ подключения PERSIST \_**</span><span class="sxs-lookup"><span data-stu-id="06a41-153">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="06a41-154">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="06a41-154">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="06a41-155">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="06a41-155">Filter property</span></span>                                                   | <span data-ttu-id="06a41-156">Значение</span><span class="sxs-lookup"><span data-stu-id="06a41-156">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="06a41-157">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-157">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="06a41-158">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="06a41-158">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="06a41-159">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-159">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="06a41-160">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="06a41-160">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="06a41-161">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="06a41-161">**action.type**</span></span>                                                   | <span data-ttu-id="06a41-162">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="06a41-162">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="06a41-163">**weight**</span><span class="sxs-lookup"><span data-stu-id="06a41-163">**weight**</span></span>                                                        | [<span data-ttu-id="06a41-164">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="06a41-164">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="06a41-165">**На уровне \_ \_ исходящего \_ транспорта фвпм Layer \_ V {4 \| 6} Настройте правила фильтрации исходящих пакетов.**</span><span class="sxs-lookup"><span data-stu-id="06a41-165">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} set up outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="06a41-166">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="06a41-166">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="06a41-167">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="06a41-167">Filter property</span></span>                                                   | <span data-ttu-id="06a41-168">Значение</span><span class="sxs-lookup"><span data-stu-id="06a41-168">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="06a41-169">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-169">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="06a41-170">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="06a41-170">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="06a41-171">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="06a41-171">**action.type**</span></span>                                                   | <span data-ttu-id="06a41-172">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="06a41-172">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="06a41-173">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="06a41-173">**action.calloutKey**</span></span>                                             | <span data-ttu-id="06a41-174">**\_Исходящий транспорт IPSec для фвпм выноски \_ \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="06a41-174">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="06a41-175">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="06a41-175">**rawContext**</span></span>                                                    | [<span data-ttu-id="06a41-176">**ФВПМ \_ контекст \_ IPSec для \_ исходящей \_ согласованности \_ обнаружения**</span><span class="sxs-lookup"><span data-stu-id="06a41-176">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="06a41-177">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="06a41-177">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="06a41-178">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="06a41-178">Filter property</span></span>                                                   | <span data-ttu-id="06a41-179">Значение</span><span class="sxs-lookup"><span data-stu-id="06a41-179">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="06a41-180">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-180">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="06a41-181">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="06a41-181">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="06a41-182">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-182">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="06a41-183">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="06a41-183">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="06a41-184">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="06a41-184">**action.type**</span></span>                                                   | <span data-ttu-id="06a41-185">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="06a41-185">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="06a41-186">**weight**</span><span class="sxs-lookup"><span data-stu-id="06a41-186">**weight**</span></span>                                                        | <span data-ttu-id="06a41-187">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="06a41-187">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="06a41-188">**На уровне \_ фвпм \_ \_ Проверка подлинности \_ recv \_ Accept \_ V {4 \| 6} Настройте правила фильтрации входящих подключений.**</span><span class="sxs-lookup"><span data-stu-id="06a41-188">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} set up inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="06a41-189">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="06a41-189">Add a filter with the following properties.</span></span> <span data-ttu-id="06a41-190">Этот фильтр разрешает входящие попытки подключения только в том случае, если они защищены протоколом IPsec.</span><span class="sxs-lookup"><span data-stu-id="06a41-190">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="06a41-191">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="06a41-191">Filter property</span></span>                                                   | <span data-ttu-id="06a41-192">Значение</span><span class="sxs-lookup"><span data-stu-id="06a41-192">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="06a41-193">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-193">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="06a41-194">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="06a41-194">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="06a41-195">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="06a41-195">**action.type**</span></span>                                                   | <span data-ttu-id="06a41-196">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="06a41-196">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="06a41-197">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="06a41-197">**action.calloutKey**</span></span>                                             | <span data-ttu-id="06a41-198">**ФВПМ \_ выноска \_ IPSec для \_ входящего трафика \_ инициирующее \_ безопасное \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="06a41-198">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="06a41-199">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="06a41-199">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="06a41-200">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="06a41-200">Filter property</span></span>                                                   | <span data-ttu-id="06a41-201">Значение</span><span class="sxs-lookup"><span data-stu-id="06a41-201">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="06a41-202">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-202">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="06a41-203">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="06a41-203">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="06a41-204">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="06a41-204">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="06a41-205">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="06a41-205">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="06a41-206">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="06a41-206">**action.type**</span></span>                                                   | <span data-ttu-id="06a41-207">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="06a41-207">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="06a41-208">**weight**</span><span class="sxs-lookup"><span data-stu-id="06a41-208">**weight**</span></span>                                                        | <span data-ttu-id="06a41-209">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="06a41-209">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="06a41-210">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="06a41-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06a41-211">Пример кода: использование транспортного режима</span><span class="sxs-lookup"><span data-stu-id="06a41-211">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="06a41-212">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="06a41-212">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="06a41-213">**Встроенные идентификаторы выноски**</span><span class="sxs-lookup"><span data-stu-id="06a41-213">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="06a41-214">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="06a41-214">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="06a41-215">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="06a41-215">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="06a41-216">**ФВПМ \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="06a41-216">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="06a41-217">**\_ \_ тип контекста поставщика \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="06a41-217">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

