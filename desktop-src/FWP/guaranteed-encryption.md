---
title: Гарантированное шифрование
description: В сценарии политики IPsec с гарантированным шифрованием требуется шифрование IPsec для всего соответствующего трафика. Эта политика должна быть указана в сочетании с одним из параметров политики транспортного режима.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbffa3d78a9e178850f3afaa4d6b7fa9831be875
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314647"
---
# <a name="guaranteed-encryption"></a><span data-ttu-id="2f364-104">Гарантированное шифрование</span><span class="sxs-lookup"><span data-stu-id="2f364-104">Guaranteed Encryption</span></span>

<span data-ttu-id="2f364-105">В сценарии политики IPsec с гарантированным шифрованием требуется шифрование IPsec для всего соответствующего трафика.</span><span class="sxs-lookup"><span data-stu-id="2f364-105">The Guaranteed Encryption IPsec policy scenario requires IPsec encryption for all matching traffic.</span></span> <span data-ttu-id="2f364-106">Эта политика должна быть указана в сочетании с одним из параметров политики транспортного режима.</span><span class="sxs-lookup"><span data-stu-id="2f364-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="2f364-107">Гарантированное шифрование обычно используется для шифрования конфиденциального трафика на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="2f364-107">Guaranteed Encryption is typically used to encrypt sensitive traffic on a per application basis.</span></span>

<span data-ttu-id="2f364-108">Примером возможного сценария шифрования является защита всего трафика одноадресных данных, за исключением ICMP, использование транспортного режима IPsec, Включение обнаружения согласований и обязательное шифрование для всего одноадресного трафика, соответствующего TCP-порту 5555.</span><span class="sxs-lookup"><span data-stu-id="2f364-108">An example of a possible Guaranteed Encryption scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and require guaranteed encryption for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="2f364-109">Чтобы реализовать этот пример программно, используйте следующую конфигурацию платформы WFP.</span><span class="sxs-lookup"><span data-stu-id="2f364-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="2f364-110">**В ФВПМ \_ Layer \_ IKEEXT \_ V {4 \| 6} Настройка политики согласования mm**</span><span class="sxs-lookup"><span data-stu-id="2f364-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="2f364-111">Добавьте один или оба следующих контекста поставщика политики MM.</span><span class="sxs-lookup"><span data-stu-id="2f364-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="2f364-112">Для IKE — контекст поставщика политики типа ФВПМ \_ IPSec \_ IKE \_ mm \_ .</span><span class="sxs-lookup"><span data-stu-id="2f364-112">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="2f364-113">Для AuthIP — контекст поставщика политики типа ФВПМ \_ IPSec \_ AuthIP \_ mm \_ .</span><span class="sxs-lookup"><span data-stu-id="2f364-113">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="2f364-114">Будет согласовываться общий модуль ключа, и будет применена соответствующая политика MM.</span><span class="sxs-lookup"><span data-stu-id="2f364-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="2f364-115">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="2f364-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="2f364-116">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="2f364-117">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-117">Filter property</span></span>        | <span data-ttu-id="2f364-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="2f364-119">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="2f364-119">Filtering conditions</span></span>   | <span data-ttu-id="2f364-120">Пустой.</span><span class="sxs-lookup"><span data-stu-id="2f364-120">Empty.</span></span> <span data-ttu-id="2f364-121">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="2f364-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="2f364-122">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="2f364-122">**providerContextKey**</span></span> | <span data-ttu-id="2f364-123">Идентификатор GUID контекста поставщика MM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="2f364-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="2f364-124">**На уровне \_ фвпм \_ IPSec \_ V {4 \| 6} Настройка политики СОГЛАСОВАНия QM и EM**</span><span class="sxs-lookup"><span data-stu-id="2f364-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="2f364-125">Добавьте один или оба следующих контекста поставщика политики транспортного режима QM и установите флаг [**\_ политики IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="2f364-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="2f364-126">Для IKE — контекст поставщика политики типа **фвпм \_ IPSec \_ IKE \_ QM \_ Transport \_**.</span><span class="sxs-lookup"><span data-stu-id="2f364-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="2f364-127">Для AuthIP — контекст поставщика политики типа **фвпм \_ IPSec \_ AuthIP \_ QM \_ Transport \_**.</span><span class="sxs-lookup"><span data-stu-id="2f364-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="2f364-128">Этот контекст может дополнительно содержать политику согласования расширенного режима AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="2f364-128">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="2f364-129">Будет выполнено согласование общего модуля ключа, и будет применена соответствующая политика QM.</span><span class="sxs-lookup"><span data-stu-id="2f364-129">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="2f364-130">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="2f364-130">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="2f364-131">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-131">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="2f364-132">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-132">Filter property</span></span>        | <span data-ttu-id="2f364-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-133">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="2f364-134">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="2f364-134">Filtering conditions</span></span>   | <span data-ttu-id="2f364-135">Пустой.</span><span class="sxs-lookup"><span data-stu-id="2f364-135">Empty.</span></span> <span data-ttu-id="2f364-136">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="2f364-136">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="2f364-137">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="2f364-137">**providerContextKey**</span></span> | <span data-ttu-id="2f364-138">Идентификатор GUID контекста поставщика QM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="2f364-138">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="2f364-139">**На уровне \_ фвпм \_ входящий \_ транспорт \_ V {4 \| 6} Настройка входящих правил фильтрации для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="2f364-139">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="2f364-140">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-140">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="2f364-141">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-141">Filter property</span></span>                                               | <span data-ttu-id="2f364-142">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-142">Value</span></span>                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2f364-143">Условие \_ \_ \_ \_ фильтрации типа локального IP-адреса условия \_ фвпм</span><span class="sxs-lookup"><span data-stu-id="2f364-143">FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE filtering condition</span></span> | [<span data-ttu-id="2f364-144">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2f364-144">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="2f364-145">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2f364-145">**action.type**</span></span>                                               | <span data-ttu-id="2f364-146">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2f364-146">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="2f364-147">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="2f364-147">**action.calloutKey**</span></span>                                         | <span data-ttu-id="2f364-148">**ФВПМ \_ выноска \_ \_ входящего \_ транспорта IPSec \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="2f364-148">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="2f364-149">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="2f364-149">**rawContext**</span></span>                                                | [<span data-ttu-id="2f364-150">**\_Безопасность контекста фвпм \_ IPSec для \_ входящего \_ \_ подключения PERSIST \_**</span><span class="sxs-lookup"><span data-stu-id="2f364-150">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="2f364-151">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-151">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="2f364-152">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-152">Filter property</span></span>                                                   | <span data-ttu-id="2f364-153">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-153">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="2f364-154">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-154">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2f364-155">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2f364-155">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="2f364-156">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-156">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="2f364-157">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="2f364-157">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="2f364-158">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2f364-158">**action.type**</span></span>                                                   | <span data-ttu-id="2f364-159">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2f364-159">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="2f364-160">**weight**</span><span class="sxs-lookup"><span data-stu-id="2f364-160">**weight**</span></span>                                                        | [<span data-ttu-id="2f364-161">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="2f364-161">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="2f364-162">**На уровне \_ \_ исходящего \_ транспорта уровня фвпм \_ V {4 \| 6} Настройка правил фильтрации исходящих пакетов для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="2f364-162">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="2f364-163">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-163">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="2f364-164">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-164">Filter property</span></span>                                                   | <span data-ttu-id="2f364-165">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-165">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2f364-166">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-166">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2f364-167">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2f364-167">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="2f364-168">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2f364-168">**action.type**</span></span>                                                   | <span data-ttu-id="2f364-169">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2f364-169">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="2f364-170">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="2f364-170">**action.calloutKey**</span></span>                                             | <span data-ttu-id="2f364-171">**\_Исходящий транспорт IPSec для фвпм выноски \_ \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="2f364-171">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="2f364-172">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="2f364-172">**rawContext**</span></span>                                                    | [<span data-ttu-id="2f364-173">**ФВПМ \_ контекст \_ IPSec для \_ исходящей \_ согласованности \_ обнаружения**</span><span class="sxs-lookup"><span data-stu-id="2f364-173">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="2f364-174">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-174">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="2f364-175">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-175">Filter property</span></span>                                                   | <span data-ttu-id="2f364-176">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-176">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="2f364-177">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-177">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2f364-178">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2f364-178">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="2f364-179">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-179">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="2f364-180">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="2f364-180">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="2f364-181">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2f364-181">**action.type**</span></span>                                                   | <span data-ttu-id="2f364-182">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2f364-182">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="2f364-183">**weight**</span><span class="sxs-lookup"><span data-stu-id="2f364-183">**weight**</span></span>                                                        | <span data-ttu-id="2f364-184">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="2f364-184">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="2f364-185">**На уровне \_ фвпм \_ \_ Проверка подлинности \_ recv \_ Accept \_ V {4 \| 6} Настройка входящих правил фильтрации для подключения**</span><span class="sxs-lookup"><span data-stu-id="2f364-185">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="2f364-186">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-186">Add a filter with the following properties.</span></span> <span data-ttu-id="2f364-187">Этот фильтр разрешает входящие попытки подключения только в том случае, если они защищены протоколом IPsec.</span><span class="sxs-lookup"><span data-stu-id="2f364-187">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="2f364-188">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-188">Filter property</span></span>                                                   | <span data-ttu-id="2f364-189">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-189">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="2f364-190">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-190">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2f364-191">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2f364-191">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="2f364-192">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2f364-192">**action.type**</span></span>                                                   | <span data-ttu-id="2f364-193">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2f364-193">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="2f364-194">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="2f364-194">**action.calloutKey**</span></span>                                             | <span data-ttu-id="2f364-195">**ФВПМ \_ выноска \_ IPSec для \_ входящего трафика \_ инициирующее \_ безопасное \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="2f364-195">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="2f364-196">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-196">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="2f364-197">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-197">Filter property</span></span>                                                   | <span data-ttu-id="2f364-198">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-198">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="2f364-199">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-199">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2f364-200">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2f364-200">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="2f364-201">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-201">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="2f364-202">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="2f364-202">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="2f364-203">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2f364-203">**action.type**</span></span>                                                   | <span data-ttu-id="2f364-204">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2f364-204">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="2f364-205">**weight**</span><span class="sxs-lookup"><span data-stu-id="2f364-205">**weight**</span></span>                                                        | <span data-ttu-id="2f364-206">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="2f364-206">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="2f364-207">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-207">Add a filter with the following properties.</span></span> <span data-ttu-id="2f364-208">Этот фильтр разрешит только входящие подключения к TCP-порту 5555, если они зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="2f364-208">This filter will only permit inbound connections to TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="2f364-209">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-209">Filter property</span></span>                                                   | <span data-ttu-id="2f364-210">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-210">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2f364-211">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-211">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2f364-212">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2f364-212">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="2f364-213">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-213">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="2f364-214">**Иппрото \_ TCP** Эта константа определена в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="2f364-214">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="2f364-215">**Фвпм \_ Условие \_ фильтрации \_ локальных \_ портов IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-215">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="2f364-216">5555</span><span class="sxs-lookup"><span data-stu-id="2f364-216">5555</span></span>                                                                                                  |
    | <span data-ttu-id="2f364-217">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2f364-217">**action.type**</span></span>                                                   | <span data-ttu-id="2f364-218">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2f364-218">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="2f364-219">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="2f364-219">**action.calloutKey**</span></span>                                             | <span data-ttu-id="2f364-220">**ФВПМ \_ выноска \_ IPSec для \_ входящего трафика \_ инициирующее \_ безопасное \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="2f364-220">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>                                          |
    | <span data-ttu-id="2f364-221">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="2f364-221">**rawContext**</span></span>                                                    | [<span data-ttu-id="2f364-222">**для \_ \_ \_ подключения к набору ALE контекста фвпм \_ \_ требуется \_ \_ шифрование IPSec**</span><span class="sxs-lookup"><span data-stu-id="2f364-222">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

        

<span data-ttu-id="2f364-223">**На сайте ФВПМ \_ Layer Authentication \_ \_ \_ \_ Connection V {4 \| 6} Настройка правил фильтрации исходящих подключений для каждого подключения**</span><span class="sxs-lookup"><span data-stu-id="2f364-223">**At FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6} setup outbound per-connection filtering rules**</span></span>

-   <span data-ttu-id="2f364-224">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2f364-224">Add a filter with the following properties.</span></span> <span data-ttu-id="2f364-225">Этот фильтр разрешает только исходящие подключения с TCP-порта 5555, если они зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="2f364-225">This filter will only permit outbound connections from TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="2f364-226">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="2f364-226">Filter property</span></span>                                                   | <span data-ttu-id="2f364-227">Значение</span><span class="sxs-lookup"><span data-stu-id="2f364-227">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2f364-228">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="2f364-229">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="2f364-229">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="2f364-230">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="2f364-231">**Иппрото \_ TCP** Эта константа определена в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="2f364-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="2f364-232">**Фвпм \_ Условие \_ фильтрации \_ локальных \_ портов IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="2f364-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="2f364-233">5555</span><span class="sxs-lookup"><span data-stu-id="2f364-233">5555</span></span>                                                                                                  |
    | <span data-ttu-id="2f364-234">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="2f364-234">**action.type**</span></span>                                                   | <span data-ttu-id="2f364-235">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="2f364-235">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="2f364-236">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="2f364-236">**action.calloutKey**</span></span>                                             | <span data-ttu-id="2f364-237">**ФВПМ \_ выноска \_ \_ ALE IPSec \_ Connect \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="2f364-237">**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V{4\|6}**</span></span>                                                       |
    | <span data-ttu-id="2f364-238">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="2f364-238">**rawContext**</span></span>                                                    | [<span data-ttu-id="2f364-239">**для \_ \_ \_ подключения к набору ALE контекста фвпм \_ \_ требуется \_ \_ шифрование IPSec**</span><span class="sxs-lookup"><span data-stu-id="2f364-239">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="2f364-240">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2f364-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f364-241">Пример кода: использование транспортного режима</span><span class="sxs-lookup"><span data-stu-id="2f364-241">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="2f364-242">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="2f364-242">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="2f364-243">**Встроенные идентификаторы выноски**</span><span class="sxs-lookup"><span data-stu-id="2f364-243">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="2f364-244">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="2f364-244">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="2f364-245">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="2f364-245">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="2f364-246">**ФВПМ \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="2f364-246">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="2f364-247">**\_ \_ тип контекста поставщика \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="2f364-247">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

