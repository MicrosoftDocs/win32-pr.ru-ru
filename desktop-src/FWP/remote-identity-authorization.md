---
title: Удаленная авторизация идентификации
description: В сценарии политики IPsec для авторизации удаленных удостоверений требуется, чтобы входящие подключения поступили от определенного набора удаленных субъектов безопасности, указанных в списке управления доступом (SD) дескриптора безопасности Windows.
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57287a0dd9af4686b1a2dab162677912213559a7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314837"
---
# <a name="remote-identity-authorization"></a><span data-ttu-id="76dcc-103">Удаленная авторизация идентификации</span><span class="sxs-lookup"><span data-stu-id="76dcc-103">Remote Identity Authorization</span></span>

<span data-ttu-id="76dcc-104">В сценарии политики IPsec для авторизации удаленных удостоверений требуется, чтобы входящие подключения поступили от определенного набора удаленных субъектов безопасности, указанных в списке управления доступом (SD) дескриптора безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="76dcc-104">The Remote Identity Authorization IPsec policy scenario requires that inbound connections come from a specific set of remote security principals which are specified in a Windows security descriptor (SD) access control list (ACL).</span></span> <span data-ttu-id="76dcc-105">Если удаленное удостоверение (определяемое протоколом IPsec) не соответствует набору разрешенных удостоверений, соединение будет удалено.</span><span class="sxs-lookup"><span data-stu-id="76dcc-105">If the remote identity (as determined by IPsec) does not match the set of allowed identities, the connection will be dropped.</span></span> <span data-ttu-id="76dcc-106">Эта политика должна быть указана в сочетании с одним из параметров политики транспортного режима.</span><span class="sxs-lookup"><span data-stu-id="76dcc-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="76dcc-107">Если протокол AuthIP включен, можно указать два дескриптора безопасности, один из которых соответствует основному режиму AuthIP, а другой — к расширенному режиму AuthIP.</span><span class="sxs-lookup"><span data-stu-id="76dcc-107">If AuthIP is enabled, two security descriptors can be specified, one corresponding to AuthIP main mode, and the other corresponding to AuthIP extended mode.</span></span>

<span data-ttu-id="76dcc-108">Примером возможного режима транспорта обнаружения согласования является "защита всего трафика одноадресных данных, за исключением ICMP, использование транспортного режима IPsec, Включение обнаружения согласований и ограничение входящего доступа к удаленным удостоверениям, разрешенное в соответствии с дескриптором безопасности SD1 (в основном режиме IKE/AuthIP) и дескриптором безопасности SD2 (соответствующий расширенному режиму AuthIP), для всего одно5555 адрес</span><span class="sxs-lookup"><span data-stu-id="76dcc-108">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and restrict inbound access to remote identities allowed as per security descriptor SD1 (corresponding to IKE/AuthIP main mode) and security descriptor SD2 (corresponding to AuthIP extended mode), for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="76dcc-109">Чтобы реализовать этот пример программно, используйте следующую конфигурацию платформы WFP.</span><span class="sxs-lookup"><span data-stu-id="76dcc-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="76dcc-110">**В ФВПМ \_ Layer \_ IKEEXT \_ V {4 \| 6} Настройка политики согласования mm**</span><span class="sxs-lookup"><span data-stu-id="76dcc-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="76dcc-111">Добавьте один или оба следующих контекста поставщика политики MM.</span><span class="sxs-lookup"><span data-stu-id="76dcc-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="76dcc-112">Для IKE — контекст поставщика политики типа **фвпм \_ IPSec \_ IKE \_ mm \_**.</span><span class="sxs-lookup"><span data-stu-id="76dcc-112">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="76dcc-113">Для AuthIP — контекст поставщика политики типа **фвпм \_ IPSec \_ AuthIP \_ mm \_**.</span><span class="sxs-lookup"><span data-stu-id="76dcc-113">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="76dcc-114">Будет согласовываться общий модуль ключа, и будет применена соответствующая политика MM.</span><span class="sxs-lookup"><span data-stu-id="76dcc-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="76dcc-115">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="76dcc-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="76dcc-116">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="76dcc-117">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-117">Filter property</span></span>        | <span data-ttu-id="76dcc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="76dcc-119">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="76dcc-119">Filtering conditions</span></span>   | <span data-ttu-id="76dcc-120">Пустой.</span><span class="sxs-lookup"><span data-stu-id="76dcc-120">Empty.</span></span> <span data-ttu-id="76dcc-121">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="76dcc-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="76dcc-122">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="76dcc-122">**providerContextKey**</span></span> | <span data-ttu-id="76dcc-123">Идентификатор GUID контекста поставщика MM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="76dcc-124">**На уровне \_ фвпм \_ IPSec \_ V {4 \| 6} Настройка политики СОГЛАСОВАНия QM и EM**</span><span class="sxs-lookup"><span data-stu-id="76dcc-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="76dcc-125">Добавьте один или оба следующих контекста поставщика политики транспортного режима QM и установите флаг [**\_ политики IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="76dcc-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="76dcc-126">Для IKE — контекст поставщика политики типа **фвпм \_ IPSec \_ IKE \_ QM \_ Transport \_**.</span><span class="sxs-lookup"><span data-stu-id="76dcc-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="76dcc-127">Для AuthIP — контекст поставщика политики типа **фвпм \_ IPSec \_ AuthIP \_ QM \_ \_** , который содержит политику согласования расширенного режима AuthIP (EM).</span><span class="sxs-lookup"><span data-stu-id="76dcc-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT** that contains the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="76dcc-128">Будет выполнено согласование общего модуля ключа, и будет применена соответствующая политика QM.</span><span class="sxs-lookup"><span data-stu-id="76dcc-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="76dcc-129">AuthIP — предпочтительный модуль создания ключей, если поддерживаются IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="76dcc-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="76dcc-130">Для каждого контекста, добавленного на шаге 1, добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="76dcc-131">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-131">Filter property</span></span>        | <span data-ttu-id="76dcc-132">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="76dcc-133">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="76dcc-133">Filtering conditions</span></span>   | <span data-ttu-id="76dcc-134">Пустой.</span><span class="sxs-lookup"><span data-stu-id="76dcc-134">Empty.</span></span> <span data-ttu-id="76dcc-135">Весь трафик будет соответствовать фильтру.</span><span class="sxs-lookup"><span data-stu-id="76dcc-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="76dcc-136">**провидерконтексткэй**</span><span class="sxs-lookup"><span data-stu-id="76dcc-136">**providerContextKey**</span></span> | <span data-ttu-id="76dcc-137">Идентификатор GUID контекста поставщика QM, добавленного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="76dcc-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="76dcc-138">**На уровне \_ фвпм \_ входящий \_ транспорт \_ V {4 \| 6} Настройка входящих правил фильтрации для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="76dcc-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="76dcc-139">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="76dcc-140">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-140">Filter property</span></span>                                                   | <span data-ttu-id="76dcc-141">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="76dcc-142">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="76dcc-143">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="76dcc-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="76dcc-144">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="76dcc-144">**action.type**</span></span>                                                   | <span data-ttu-id="76dcc-145">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="76dcc-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="76dcc-146">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="76dcc-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="76dcc-147">**ФВПМ \_ выноска \_ \_ входящего \_ транспорта IPSec \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="76dcc-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="76dcc-148">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="76dcc-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="76dcc-149">**\_Безопасность контекста фвпм \_ IPSec для \_ входящего \_ \_ подключения PERSIST \_**</span><span class="sxs-lookup"><span data-stu-id="76dcc-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="76dcc-150">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="76dcc-151">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-151">Filter property</span></span>                                                   | <span data-ttu-id="76dcc-152">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="76dcc-153">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="76dcc-154">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="76dcc-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="76dcc-155">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="76dcc-156">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="76dcc-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="76dcc-157">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="76dcc-157">**action.type**</span></span>                                                   | <span data-ttu-id="76dcc-158">\_разрешение действия \_ FWP</span><span class="sxs-lookup"><span data-stu-id="76dcc-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="76dcc-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="76dcc-159">**weight**</span></span>                                                        | [<span data-ttu-id="76dcc-160">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="76dcc-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="76dcc-161">**На уровне \_ \_ исходящего \_ транспорта уровня фвпм \_ V {4 \| 6} Настройка правил фильтрации исходящих пакетов для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="76dcc-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="76dcc-162">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-162">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="76dcc-163">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-163">Filter property</span></span>                                                   | <span data-ttu-id="76dcc-164">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="76dcc-165">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="76dcc-166">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="76dcc-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="76dcc-167">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="76dcc-167">**action.type**</span></span>                                                   | <span data-ttu-id="76dcc-168">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="76dcc-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="76dcc-169">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="76dcc-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="76dcc-170">**\_Исходящий транспорт IPSec для фвпм выноски \_ \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="76dcc-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="76dcc-171">**равконтекст**</span><span class="sxs-lookup"><span data-stu-id="76dcc-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="76dcc-172">**ФВПМ \_ контекст \_ IPSec для \_ исходящей \_ согласованности \_ обнаружения**</span><span class="sxs-lookup"><span data-stu-id="76dcc-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="76dcc-173">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="76dcc-174">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-174">Filter property</span></span>                                                   | <span data-ttu-id="76dcc-175">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-175">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="76dcc-176">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="76dcc-177">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="76dcc-177">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="76dcc-178">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="76dcc-179">ИППРОТО \_ ICMP {V6} эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="76dcc-179">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="76dcc-180">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="76dcc-180">**action.type**</span></span>                                                   | <span data-ttu-id="76dcc-181">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="76dcc-181">**FWP\_ACTION\_PERMIT**</span></span>                                                |
    | <span data-ttu-id="76dcc-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="76dcc-182">**weight**</span></span>                                                        | <span data-ttu-id="76dcc-183">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="76dcc-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                               |

        

<span data-ttu-id="76dcc-184">**На уровне \_ фвпм \_ \_ Проверка подлинности \_ recv \_ Accept \_ V {4 \| 6} Настройка входящих правил фильтрации для подключения**</span><span class="sxs-lookup"><span data-stu-id="76dcc-184">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="76dcc-185">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-185">Add a filter with the following properties.</span></span> <span data-ttu-id="76dcc-186">Этот фильтр разрешает входящие попытки подключения только в том случае, если они защищены протоколом IPsec.</span><span class="sxs-lookup"><span data-stu-id="76dcc-186">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="76dcc-187">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-187">Filter property</span></span>                                                   | <span data-ttu-id="76dcc-188">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-188">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="76dcc-189">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-189">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="76dcc-190">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="76dcc-190">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="76dcc-191">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="76dcc-191">**action.type**</span></span>                                                   | <span data-ttu-id="76dcc-192">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="76dcc-192">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="76dcc-193">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="76dcc-193">**action.calloutKey**</span></span>                                             | <span data-ttu-id="76dcc-194">**ФВПМ \_ выноска \_ IPSec для \_ входящего трафика \_ инициирующее \_ безопасное \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="76dcc-194">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="76dcc-195">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-195">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="76dcc-196">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-196">Filter property</span></span>                                                   | <span data-ttu-id="76dcc-197">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-197">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="76dcc-198">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-198">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="76dcc-199">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="76dcc-199">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="76dcc-200">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-200">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="76dcc-201">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="76dcc-201">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="76dcc-202">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="76dcc-202">**action.type**</span></span>                                                   | <span data-ttu-id="76dcc-203">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="76dcc-203">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="76dcc-204">**weight**</span><span class="sxs-lookup"><span data-stu-id="76dcc-204">**weight**</span></span>                                                        | <span data-ttu-id="76dcc-205">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="76dcc-205">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="76dcc-206">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-206">Add a filter with the following properties.</span></span> <span data-ttu-id="76dcc-207">Этот фильтр разрешает входящие подключения к TCP-порту 5555, если соответствующие удаленные удостоверения разрешены как SD1, так и SD2.</span><span class="sxs-lookup"><span data-stu-id="76dcc-207">This filter will permit inbound connections to TCP port 5555 if the corresponding remote identities are allowed by both SD1 and SD2.</span></span> 

    | <span data-ttu-id="76dcc-208">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-208">Filter property</span></span>                                                   | <span data-ttu-id="76dcc-209">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-209">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="76dcc-210">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-210">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="76dcc-211">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="76dcc-211">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="76dcc-212">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-212">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="76dcc-213">**Иппрото \_ TCP** Эта константа определена в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="76dcc-213">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="76dcc-214">**Фвпм \_ Условие \_ фильтрации \_ локальных \_ портов IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-214">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="76dcc-215">5555</span><span class="sxs-lookup"><span data-stu-id="76dcc-215">5555</span></span>                                                               |
    | <span data-ttu-id="76dcc-216">**\_ \_ \_ \_ идентификатор удаленного компьютера ALE \_ фвпм Condition**</span><span class="sxs-lookup"><span data-stu-id="76dcc-216">**FWPM\_CONDITION\_ALE\_REMOTE\_MACHINE\_ID**</span></span>                     | <span data-ttu-id="76dcc-217">SD1</span><span class="sxs-lookup"><span data-stu-id="76dcc-217">SD1</span></span>                                                                |
    | <span data-ttu-id="76dcc-218">**\_ \_ \_ \_ идентификатор удаленного пользователя ALE условия \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="76dcc-218">**FWPM\_CONDITION\_ALE\_REMOTE\_USER\_ID**</span></span>                        | <span data-ttu-id="76dcc-219">SD2</span><span class="sxs-lookup"><span data-stu-id="76dcc-219">SD2</span></span>                                                                |
    | <span data-ttu-id="76dcc-220">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="76dcc-220">**action.type**</span></span>                                                   | <span data-ttu-id="76dcc-221">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="76dcc-221">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                              |
    | <span data-ttu-id="76dcc-222">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="76dcc-222">**action.calloutKey**</span></span>                                             | <span data-ttu-id="76dcc-223">**ФВПМ \_ выноска \_ IPSec для \_ входящего трафика \_ инициирующее \_ безопасное \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="76dcc-223">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>       |

        
4.  <span data-ttu-id="76dcc-224">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="76dcc-224">Add a filter with the following properties.</span></span> <span data-ttu-id="76dcc-225">Этот фильтр блокирует все остальные входящие подключения к TCP-порту 5555, не совпадающему с предыдущим фильтром.</span><span class="sxs-lookup"><span data-stu-id="76dcc-225">This filter will block any other inbound connections to TCP port 5555 that did not match the previous filter.</span></span> 

    | <span data-ttu-id="76dcc-226">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="76dcc-226">Filter property</span></span>                                                   | <span data-ttu-id="76dcc-227">Значение</span><span class="sxs-lookup"><span data-stu-id="76dcc-227">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="76dcc-228">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="76dcc-229">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="76dcc-229">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="76dcc-230">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="76dcc-231">**Иппрото \_ TCP** Эта константа определена в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="76dcc-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="76dcc-232">**Фвпм \_ Условие \_ фильтрации \_ локальных \_ портов IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="76dcc-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="76dcc-233">5555</span><span class="sxs-lookup"><span data-stu-id="76dcc-233">5555</span></span>                                                               |
    | <span data-ttu-id="76dcc-234">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="76dcc-234">**action.type**</span></span>                                                   | <span data-ttu-id="76dcc-235">**\_блок действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="76dcc-235">**FWP\_ACTION\_BLOCK**</span></span>                                             |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="76dcc-236">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="76dcc-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76dcc-237">Пример кода: использование транспортного режима</span><span class="sxs-lookup"><span data-stu-id="76dcc-237">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="76dcc-238">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="76dcc-238">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="76dcc-239">**Встроенные идентификаторы выноски**</span><span class="sxs-lookup"><span data-stu-id="76dcc-239">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="76dcc-240">Условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="76dcc-240">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="76dcc-241">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="76dcc-241">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="76dcc-242">**ФВПМ \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="76dcc-242">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="76dcc-243">**\_ \_ тип контекста поставщика \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="76dcc-243">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

