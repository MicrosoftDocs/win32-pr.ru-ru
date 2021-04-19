---
title: транспортный режим
description: В сценарии политики IPsec режима транспорта требуется защита режима транспорта IPsec для всего соответствующего трафика.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8335854c80850e44b860530bbebab05aa3f14273
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314937"
---
# <a name="transport-mode"></a><span data-ttu-id="49131-103">транспортный режим</span><span class="sxs-lookup"><span data-stu-id="49131-103">Transport Mode</span></span>

<span data-ttu-id="49131-104">В сценарии политики IPsec режима транспорта требуется защита режима транспорта IPsec для всего соответствующего трафика.</span><span class="sxs-lookup"><span data-stu-id="49131-104">The Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="49131-105">Любой соответствующий трафик с открытым текстом удаляется до успешного завершения согласования IKE или AuthIP.</span><span class="sxs-lookup"><span data-stu-id="49131-105">Any matching clear text traffic is dropped until the IKE or AuthIP negotiation has completed successfully.</span></span> <span data-ttu-id="49131-106">В случае сбоя согласования подключение с соответствующим IP-адресом останется неработоспособным.</span><span class="sxs-lookup"><span data-stu-id="49131-106">If the negotiation fails, connectivity with the corresponding IP address will remain broken.</span></span>

<span data-ttu-id="49131-107">Примером возможного режима транспорта может быть "защита всего трафика одноадресных данных, за исключением ICMP, с использованием транспортного режима IPsec".</span><span class="sxs-lookup"><span data-stu-id="49131-107">An example of a possible Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode."</span></span>

<span data-ttu-id="49131-108">Чтобы реализовать этот пример программно, используйте следующую конфигурацию платформы WFP.</span><span class="sxs-lookup"><span data-stu-id="49131-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="49131-109">**В ФВПМ \_ Layer \_ IKEEXT \_ V {4 \| 6} Настройка политики согласования mm**</span><span class="sxs-lookup"><span data-stu-id="49131-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="49131-110">Добавьте один или оба следующих контекста поставщика политики MM.</span><span class="sxs-lookup"><span data-stu-id="49131-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="49131-111">Для IKE — контекст поставщика политики типа **фвпм \_ IPSec \_ IKE \_ mm \_**.</span><span class="sxs-lookup"><span data-stu-id="49131-111">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="49131-112">Для AuthIP — контекст поставщика политики типа **фвпм \_ IPSec \_ AuthIP \_ mm \_**.</span><span class="sxs-lookup"><span data-stu-id="49131-112">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="49131-113">Будет согласовываться общий модуль ключа, и будет применена соответствующая политика MM.</span><span class="sxs-lookup"><span data-stu-id="49131-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="49131-114">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="49131-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="49131-115">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="49131-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="49131-116">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="49131-116">Filter property</span></span>        | <span data-ttu-id="49131-117">Значение</span><span class="sxs-lookup"><span data-stu-id="49131-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="49131-118">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="49131-118">Filtering conditions</span></span>   | <span data-ttu-id="49131-119">Пустой.</span><span class="sxs-lookup"><span data-stu-id="49131-119">Empty.</span></span> <span data-ttu-id="49131-120">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="49131-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="49131-121">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="49131-121">**providerContextKey**</span></span> | <span data-ttu-id="49131-122">Идентификатор GUID контекста поставщика MM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="49131-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="49131-123">**На уровне \_ фвпм \_ IPSec \_ V {4 \| 6} Настройка политики СОГЛАСОВАНия QM и EM**</span><span class="sxs-lookup"><span data-stu-id="49131-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="49131-124">Добавьте один или оба следующих контекста поставщика политики транспортного режима QM.</span><span class="sxs-lookup"><span data-stu-id="49131-124">Add one or both of the following QM transport mode policy provider contexts.</span></span>  
    -   <span data-ttu-id="49131-125">Для IKE — контекст поставщика политики типа **фвпм \_ IPSec \_ IKE \_ QM \_ Transport \_**.</span><span class="sxs-lookup"><span data-stu-id="49131-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="49131-126">Для AuthIP — контекст поставщика политики типа **фвпм \_ IPSec \_ AuthIP \_ QM \_ Transport \_**.</span><span class="sxs-lookup"><span data-stu-id="49131-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="49131-127">Этот контекст может дополнительно содержать политику согласования расширенного режима AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="49131-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="49131-128">Будет выполнено согласование общего модуля ключа, и будет применена соответствующая политика QM.</span><span class="sxs-lookup"><span data-stu-id="49131-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="49131-129">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="49131-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="49131-130">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="49131-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="49131-131">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="49131-131">Filter property</span></span>        | <span data-ttu-id="49131-132">Значение</span><span class="sxs-lookup"><span data-stu-id="49131-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="49131-133">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="49131-133">Filtering conditions</span></span>   | <span data-ttu-id="49131-134">Пустой.</span><span class="sxs-lookup"><span data-stu-id="49131-134">Empty.</span></span> <span data-ttu-id="49131-135">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="49131-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="49131-136">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="49131-136">**providerContextKey**</span></span> | <span data-ttu-id="49131-137">Идентификатор GUID контекста поставщика QM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="49131-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="49131-138">**На уровне \_ фвпм \_ входящий \_ транспорт \_ V {4 \| 6} Настройка входящих правил фильтрации для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="49131-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="49131-139">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="49131-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="49131-140">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="49131-140">Filter property</span></span>                                                   | <span data-ttu-id="49131-141">Значение</span><span class="sxs-lookup"><span data-stu-id="49131-141">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="49131-142">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="49131-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="49131-143">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="49131-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="49131-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="49131-144">**action.type**</span></span>                                                   | <span data-ttu-id="49131-145">\_ \_ Завершение вызова действия \_ FWP</span><span class="sxs-lookup"><span data-stu-id="49131-145">FWP\_ACTION\_CALLOUT\_TERMINATING</span></span>                             |
    | <span data-ttu-id="49131-146">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="49131-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="49131-147">ФВПМ \_ выноска \_ \_ входящего \_ транспорта IPSec \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="49131-147">FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>             |

        
2.  <span data-ttu-id="49131-148">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="49131-148">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="49131-149">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="49131-149">Filter property</span></span>                                                  | <span data-ttu-id="49131-150">Значение</span><span class="sxs-lookup"><span data-stu-id="49131-150">Value</span></span>                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | <span data-ttu-id="49131-151">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="49131-151">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="49131-152">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="49131-152">NlatUnicast</span></span>                                                               |
    | <span data-ttu-id="49131-153">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="49131-153">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>            | <span data-ttu-id="49131-154">ИППРОТО \_ ICMP {V6} эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="49131-154">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/>    |
    | <span data-ttu-id="49131-155">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="49131-155">**action.type**</span></span>                                                  | <span data-ttu-id="49131-156">\_разрешение действия \_ FWP</span><span class="sxs-lookup"><span data-stu-id="49131-156">FWP\_ACTION\_PERMIT</span></span>                                                       |
    | <span data-ttu-id="49131-157">**weight**</span><span class="sxs-lookup"><span data-stu-id="49131-157">**weight**</span></span>                                                       | [<span data-ttu-id="49131-158">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="49131-158">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md) |

        

<span data-ttu-id="49131-159">**На уровне \_ \_ исходящего \_ транспорта уровня фвпм \_ V {4 \| 6} Настройка правил фильтрации исходящих пакетов для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="49131-159">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="49131-160">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="49131-160">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="49131-161">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="49131-161">Filter property</span></span>                                                   | <span data-ttu-id="49131-162">Значение</span><span class="sxs-lookup"><span data-stu-id="49131-162">Value</span></span>                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | <span data-ttu-id="49131-163">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="49131-163">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="49131-164">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="49131-164">NlatUnicast</span></span>                                        |
    | <span data-ttu-id="49131-165">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="49131-165">**action.type**</span></span>                                                   | <span data-ttu-id="49131-166">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="49131-166">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>              |
    | <span data-ttu-id="49131-167">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="49131-167">**action.calloutKey**</span></span>                                             | <span data-ttu-id="49131-168">\_Исходящий транспорт IPSec для фвпм выноски \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="49131-168">FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span> |

        
2.  <span data-ttu-id="49131-169">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="49131-169">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="49131-170">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="49131-170">Filter property</span></span>                                                   | <span data-ttu-id="49131-171">Значение</span><span class="sxs-lookup"><span data-stu-id="49131-171">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="49131-172">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="49131-172">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="49131-173">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="49131-173">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="49131-174">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="49131-174">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="49131-175">ИППРОТО \_ ICMP {V6} эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="49131-175">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="49131-176">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="49131-176">**action.type**</span></span>                                                   | <span data-ttu-id="49131-177">\_разрешение действия \_ FWP</span><span class="sxs-lookup"><span data-stu-id="49131-177">FWP\_ACTION\_PERMIT</span></span>                                                    |
    | <span data-ttu-id="49131-178">**weight**</span><span class="sxs-lookup"><span data-stu-id="49131-178">**weight**</span></span>                                                        | <span data-ttu-id="49131-179">\_ \_ исключения IKE для диапазона веса \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="49131-179">FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="49131-180">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="49131-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49131-181">Пример кода: использование транспортного режима</span><span class="sxs-lookup"><span data-stu-id="49131-181">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="49131-182">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="49131-182">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="49131-183">**Типы контекста поставщика**</span><span class="sxs-lookup"><span data-stu-id="49131-183">**Provider Context Types**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[<span data-ttu-id="49131-184">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="49131-184">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="49131-185">**ФВПМ \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="49131-185">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="49131-186">**Встроенные идентификаторы выноски**</span><span class="sxs-lookup"><span data-stu-id="49131-186">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> </dl>

 

