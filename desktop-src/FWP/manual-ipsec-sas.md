---
title: SA вручную
description: Сценарий политики IPsec для сопоставления безопасности вручную позволяет вызывающим объектам обходить встроенные модули ключей IPsec (IKE и AuthIP), напрямую указывая SAs IPsec для защиты любого сетевого трафика.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beeef4486e3a07dea2e83d924c2354a3dabca241
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314577"
---
# <a name="manual-sa"></a><span data-ttu-id="edd72-103">SA вручную</span><span class="sxs-lookup"><span data-stu-id="edd72-103">Manual SA</span></span>

<span data-ttu-id="edd72-104">Сценарий политики IPsec для сопоставления безопасности вручную позволяет вызывающим объектам обходить встроенные модули ключей IPsec (IKE и AuthIP), напрямую указывая SAs IPsec для защиты любого сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="edd72-104">The Manual Security Association (SA) IPsec policy scenario allows callers to bypass the built-in IPsec keying modules (IKE and AuthIP) by directly specifying IPsec SAs to secure any network traffic.</span></span>

<span data-ttu-id="edd72-105">Пример возможного ручного сопоставления безопасности: "добавить пару IPsec SA для защиты всего трафика одноадресных данных между IP-адресами 1.1.1.1 & 2.2.2.2, за исключением ICMP, с использованием транспортного режима IPsec".</span><span class="sxs-lookup"><span data-stu-id="edd72-105">An example of a possible Manual SA scenario is "Add an IPsec SA pair to secure all unicast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode."</span></span>

> [!Note]  
> <span data-ttu-id="edd72-106">Следующие шаги должны выполняться на обоих компьютерах с соответствующим образом настроенными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="edd72-106">The following steps must be executed on both machines with IP addresses appropriately set.</span></span>

 

<span data-ttu-id="edd72-107">Чтобы реализовать этот пример программно, используйте следующую конфигурацию платформы WFP.</span><span class="sxs-lookup"><span data-stu-id="edd72-107">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="edd72-108">**На уровне \_ фвпм \_ входящий \_ транспорт \_ V {4 \| 6} Настройка входящих правил фильтрации для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="edd72-108">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="edd72-109">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="edd72-109">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="edd72-110">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="edd72-110">Filter property</span></span>                                                   | <span data-ttu-id="edd72-111">Значение</span><span class="sxs-lookup"><span data-stu-id="edd72-111">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="edd72-112">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="edd72-112">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="edd72-113">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="edd72-113">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="edd72-114">**\_ \_ локальный IP- \_ \_ адрес условия фвпм**</span><span class="sxs-lookup"><span data-stu-id="edd72-114">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS**</span></span>                           | <span data-ttu-id="edd72-115">Соответствующий локальный адрес (1.1.1.1 или 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="edd72-115">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>           |
    | <span data-ttu-id="edd72-116">**\_ \_ Удаленный IP- \_ \_ адрес условия фвпм**</span><span class="sxs-lookup"><span data-stu-id="edd72-116">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS**</span></span>                          | <span data-ttu-id="edd72-117">Соответствующий удаленный адрес (1.1.1.1 или 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="edd72-117">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>          |
    | <span data-ttu-id="edd72-118">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="edd72-118">**action.type**</span></span>                                                   | <span data-ttu-id="edd72-119">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="edd72-119">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                         |
    | <span data-ttu-id="edd72-120">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="edd72-120">**action.calloutKey**</span></span>                                             | <span data-ttu-id="edd72-121">**ФВПМ \_ выноска \_ \_ входящего \_ транспорта IPSec \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="edd72-121">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>         |

        
2.  <span data-ttu-id="edd72-122">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="edd72-122">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="edd72-123">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="edd72-123">Filter property</span></span>                                                   | <span data-ttu-id="edd72-124">Значение</span><span class="sxs-lookup"><span data-stu-id="edd72-124">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="edd72-125">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="edd72-125">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="edd72-126">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="edd72-126">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="edd72-127">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="edd72-127">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="edd72-128">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="edd72-128">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="edd72-129">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="edd72-129">**action.type**</span></span>                                                   | <span data-ttu-id="edd72-130">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="edd72-130">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="edd72-131">**weight**</span><span class="sxs-lookup"><span data-stu-id="edd72-131">**weight**</span></span>                                                        | [<span data-ttu-id="edd72-132">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="edd72-132">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="edd72-133">**На уровне \_ \_ исходящего \_ транспорта уровня фвпм \_ V {4 \| 6} Настройка правил фильтрации исходящих пакетов для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="edd72-133">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="edd72-134">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="edd72-134">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="edd72-135">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="edd72-135">Filter property</span></span>                                                   | <span data-ttu-id="edd72-136">Значение</span><span class="sxs-lookup"><span data-stu-id="edd72-136">Value</span></span>                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="edd72-137">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="edd72-137">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="edd72-138">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="edd72-138">NlatUnicast</span></span>                                            |
    | <span data-ttu-id="edd72-139">**Фвпм \_ Условие \_ фильтрации \_ локального \_ IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="edd72-139">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS** filtering condition</span></span>       | <span data-ttu-id="edd72-140">Соответствующий локальный адрес (1.1.1.1 или 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="edd72-140">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>    |
    | <span data-ttu-id="edd72-141">**Фвпм \_ Условие \_ фильтрации \_ удаленных \_ IP-адресов условия**</span><span class="sxs-lookup"><span data-stu-id="edd72-141">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS** filtering condition</span></span>      | <span data-ttu-id="edd72-142">Соответствующий удаленный адрес (1.1.1.1 или 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="edd72-142">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>   |
    | <span data-ttu-id="edd72-143">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="edd72-143">**action.type**</span></span>                                                   | <span data-ttu-id="edd72-144">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="edd72-144">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                  |
    | <span data-ttu-id="edd72-145">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="edd72-145">**action.calloutKey**</span></span>                                             | <span data-ttu-id="edd72-146">**\_Исходящий транспорт IPSec для фвпм выноски \_ \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="edd72-146">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="edd72-147">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="edd72-147">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="edd72-148">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="edd72-148">Filter property</span></span>                                                   | <span data-ttu-id="edd72-149">Значение</span><span class="sxs-lookup"><span data-stu-id="edd72-149">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="edd72-150">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="edd72-150">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="edd72-151">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="edd72-151">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="edd72-152">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="edd72-152">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="edd72-153">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="edd72-153">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="edd72-154">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="edd72-154">**action.type**</span></span>                                                   | <span data-ttu-id="edd72-155">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="edd72-155">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="edd72-156">**weight**</span><span class="sxs-lookup"><span data-stu-id="edd72-156">**weight**</span></span>                                                        | <span data-ttu-id="edd72-157">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="edd72-157">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="edd72-158">**Настройка входящих и исходящих сопоставлений безопасности**</span><span class="sxs-lookup"><span data-stu-id="edd72-158">**Setup inbound and outbound security associations**</span></span>

1.  <span data-ttu-id="edd72-159">Вызовите [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), указав параметр *аутбаундтраффик* , содержащий IP-адреса 1.1.1.1 & 2.2.2.2, и **ипсекфилтерид** в качестве LUID фильтра выноски IPSec исходящего транспортного уровня, добавленного выше.</span><span class="sxs-lookup"><span data-stu-id="edd72-159">Call [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), with the *outboundTraffic* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the outbound transport layer IPsec callout filter added above.</span></span>
2.  <span data-ttu-id="edd72-160">Вызовите [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)с параметром *ID* , содержащим идентификатор контекста, возвращенный из [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), и параметр *жетспи* , содержащий IP-адреса 1.1.1.1 & 2.2.2.2, и **ипсекфилтерид** в качестве LUID фильтра выноски IPSec транспортного уровня, добавленного выше.</span><span class="sxs-lookup"><span data-stu-id="edd72-160">Call [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *getSpi* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the inbound transport layer IPsec callout filter added above.</span></span> <span data-ttu-id="edd72-161">Возвращенное значение SPI предназначено для использования в качестве SPI входящего SA на локальном компьютере и в качестве исходящего SPI сопоставления безопасности на соответствующем удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="edd72-161">The returned SPI value is meant to be used as the inbound SA SPI by the local machine and as the outbound SA SPI by the corresponding remote machine.</span></span> <span data-ttu-id="edd72-162">Оба компьютера должны использовать некоторые нестандартные средства для обмена значениями SPI.</span><span class="sxs-lookup"><span data-stu-id="edd72-162">Both machines must use some out-of-band means to exchange the SPI values.</span></span>
3.  <span data-ttu-id="edd72-163">Вызовите [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)с параметром *ID* , содержащим идентификатор контекста, возвращенный из [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), и параметр *ИНБАУНДБУНДЛЕ* , описывающий свойства входящего пакета SA (входящего SA, тип преобразования, типы алгоритмов, ключи и т. д.).</span><span class="sxs-lookup"><span data-stu-id="edd72-163">Call [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *inboundBundle* parameter describing the properties of the inbound SA bundle (such as the inbound SA SPI, transform type, algorithm types, keys, etc).</span></span>
4.  <span data-ttu-id="edd72-164">Вызовите [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)с параметром *ID* , содержащим идентификатор контекста, возвращенный из [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), и параметр *аутбаундбундле* , описывающий свойства исходящего пакета SA (например, исходящий SPI SA, тип преобразования, типы алгоритмов, ключи и т. д.).</span><span class="sxs-lookup"><span data-stu-id="edd72-164">Call [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *outboundBundle* parameter describing the properties of the outbound SA bundle (such as the outbound SA SPI, transform type, algorithm types, keys, etc).</span></span>

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="edd72-165">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="edd72-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edd72-166">Пример кода: ключ SA вручную</span><span class="sxs-lookup"><span data-stu-id="edd72-166">Sample code: Manual SA Keying</span></span>](manual-sa-keying.md)
</dt> <dt>

[<span data-ttu-id="edd72-167">**Встроенные идентификаторы выноски**</span><span class="sxs-lookup"><span data-stu-id="edd72-167">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="edd72-168">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="edd72-168">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="edd72-169">**ФВПМ \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="edd72-169">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

