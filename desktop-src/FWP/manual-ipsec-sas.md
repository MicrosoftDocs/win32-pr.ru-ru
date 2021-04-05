---
title: SA вручную
description: Сценарий политики IPsec для сопоставления безопасности вручную позволяет вызывающим объектам обходить встроенные модули ключей IPsec (IKE и AuthIP), напрямую указывая SAs IPsec для защиты любого сетевого трафика.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161447ff5cfd98878ab4ee0f4b18cbcc3a53643
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987414"
---
# <a name="manual-sa"></a><span data-ttu-id="71ee4-103">SA вручную</span><span class="sxs-lookup"><span data-stu-id="71ee4-103">Manual SA</span></span>

<span data-ttu-id="71ee4-104">Сценарий политики IPsec для сопоставления безопасности вручную позволяет вызывающим объектам обходить встроенные модули ключей IPsec (IKE и AuthIP), напрямую указывая SAs IPsec для защиты любого сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="71ee4-104">The Manual Security Association (SA) IPsec policy scenario allows callers to bypass the built-in IPsec keying modules (IKE and AuthIP) by directly specifying IPsec SAs to secure any network traffic.</span></span>

<span data-ttu-id="71ee4-105">Пример возможного ручного сопоставления безопасности: "добавить пару IPsec SA для защиты всего трафика одноадресных данных между IP-адресами 1.1.1.1 & 2.2.2.2, за исключением ICMP, с использованием транспортного режима IPsec".</span><span class="sxs-lookup"><span data-stu-id="71ee4-105">An example of a possible Manual SA scenario is "Add an IPsec SA pair to secure all unicast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode."</span></span>

> [!Note]  
> <span data-ttu-id="71ee4-106">Следующие шаги должны выполняться на обоих компьютерах с соответствующим образом настроенными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="71ee4-106">The following steps must be executed on both machines with IP addresses appropriately set.</span></span>

 

<span data-ttu-id="71ee4-107">Чтобы реализовать этот пример программно, используйте следующую конфигурацию платформы WFP.</span><span class="sxs-lookup"><span data-stu-id="71ee4-107">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="71ee4-108">**На уровне \_ фвпм \_ входящий \_ транспорт \_ V {4 \| 6} Настройка входящих правил фильтрации для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="71ee4-108">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="71ee4-109">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="71ee4-109">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="71ee4-110">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="71ee4-110">Filter property</span></span>                                                   | <span data-ttu-id="71ee4-111">Значение</span><span class="sxs-lookup"><span data-stu-id="71ee4-111">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="71ee4-112">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="71ee4-112">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="71ee4-113">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="71ee4-113">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="71ee4-114">**\_ \_ локальный IP- \_ \_ адрес условия фвпм**</span><span class="sxs-lookup"><span data-stu-id="71ee4-114">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS**</span></span>                           | <span data-ttu-id="71ee4-115">Соответствующий локальный адрес (1.1.1.1 или 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="71ee4-115">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>           |
    | <span data-ttu-id="71ee4-116">**\_ \_ Удаленный IP- \_ \_ адрес условия фвпм**</span><span class="sxs-lookup"><span data-stu-id="71ee4-116">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS**</span></span>                          | <span data-ttu-id="71ee4-117">Соответствующий удаленный адрес (1.1.1.1 или 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="71ee4-117">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>          |
    | <span data-ttu-id="71ee4-118">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="71ee4-118">**action.type**</span></span>                                                   | <span data-ttu-id="71ee4-119">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="71ee4-119">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                         |
    | <span data-ttu-id="71ee4-120">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="71ee4-120">**action.calloutKey**</span></span>                                             | <span data-ttu-id="71ee4-121">**ФВПМ \_ выноска \_ \_ входящего \_ транспорта IPSec \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="71ee4-121">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>         |

        
2.  <span data-ttu-id="71ee4-122">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="71ee4-122">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="71ee4-123">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="71ee4-123">Filter property</span></span>                                                   | <span data-ttu-id="71ee4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="71ee4-124">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="71ee4-125">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="71ee4-125">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="71ee4-126">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="71ee4-126">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="71ee4-127">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="71ee4-127">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="71ee4-128">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="71ee4-128">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="71ee4-129">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="71ee4-129">**action.type**</span></span>                                                   | <span data-ttu-id="71ee4-130">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="71ee4-130">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="71ee4-131">**weight**</span><span class="sxs-lookup"><span data-stu-id="71ee4-131">**weight**</span></span>                                                        | [<span data-ttu-id="71ee4-132">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="71ee4-132">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="71ee4-133">**На уровне \_ \_ исходящего \_ транспорта уровня фвпм \_ V {4 \| 6} Настройка правил фильтрации исходящих пакетов для каждого пакета**</span><span class="sxs-lookup"><span data-stu-id="71ee4-133">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="71ee4-134">Добавьте фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="71ee4-134">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="71ee4-135">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="71ee4-135">Filter property</span></span>                                                   | <span data-ttu-id="71ee4-136">Значение</span><span class="sxs-lookup"><span data-stu-id="71ee4-136">Value</span></span>                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="71ee4-137">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="71ee4-137">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="71ee4-138">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="71ee4-138">NlatUnicast</span></span>                                            |
    | <span data-ttu-id="71ee4-139">**Фвпм \_ Условие \_ фильтрации \_ локального \_ IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="71ee4-139">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS** filtering condition</span></span>       | <span data-ttu-id="71ee4-140">Соответствующий локальный адрес (1.1.1.1 или 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="71ee4-140">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>    |
    | <span data-ttu-id="71ee4-141">**Фвпм \_ Условие \_ фильтрации \_ удаленных \_ IP-адресов условия**</span><span class="sxs-lookup"><span data-stu-id="71ee4-141">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS** filtering condition</span></span>      | <span data-ttu-id="71ee4-142">Соответствующий удаленный адрес (1.1.1.1 или 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="71ee4-142">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>   |
    | <span data-ttu-id="71ee4-143">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="71ee4-143">**action.type**</span></span>                                                   | <span data-ttu-id="71ee4-144">**\_ \_ Завершение вызова действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="71ee4-144">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                  |
    | <span data-ttu-id="71ee4-145">**Action. Каллауткэй**</span><span class="sxs-lookup"><span data-stu-id="71ee4-145">**action.calloutKey**</span></span>                                             | <span data-ttu-id="71ee4-146">**\_Исходящий транспорт IPSec для фвпм выноски \_ \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="71ee4-146">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="71ee4-147">Исключите ICMP-трафик из IPsec, добавив фильтр со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="71ee4-147">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="71ee4-148">Свойство Filter</span><span class="sxs-lookup"><span data-stu-id="71ee4-148">Filter property</span></span>                                                   | <span data-ttu-id="71ee4-149">Значение</span><span class="sxs-lookup"><span data-stu-id="71ee4-149">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="71ee4-150">**Фвпм \_ Условие \_ фильтрации \_ \_ \_ типа ЛОКАЛЬНОГО IP-адреса условия**</span><span class="sxs-lookup"><span data-stu-id="71ee4-150">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="71ee4-151">нлатуникаст</span><span class="sxs-lookup"><span data-stu-id="71ee4-151">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="71ee4-152">**Фвпм \_ Условие фильтрации \_ IP- \_ протокола условия**</span><span class="sxs-lookup"><span data-stu-id="71ee4-152">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="71ee4-153">**Иппрото \_ ICMP {V6}** эти константы определены в Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="71ee4-153">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="71ee4-154">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="71ee4-154">**action.type**</span></span>                                                   | <span data-ttu-id="71ee4-155">**\_разрешение действия \_ FWP**</span><span class="sxs-lookup"><span data-stu-id="71ee4-155">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="71ee4-156">**weight**</span><span class="sxs-lookup"><span data-stu-id="71ee4-156">**weight**</span></span>                                                        | <span data-ttu-id="71ee4-157">**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="71ee4-157">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="71ee4-158">**Настройка входящих и исходящих сопоставлений безопасности**</span><span class="sxs-lookup"><span data-stu-id="71ee4-158">**Setup inbound and outbound security associations**</span></span>

1.  <span data-ttu-id="71ee4-159">Вызовите [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), указав параметр *аутбаундтраффик* , содержащий IP-адреса 1.1.1.1 & 2.2.2.2, и **ипсекфилтерид** в качестве LUID фильтра выноски IPSec исходящего транспортного уровня, добавленного выше.</span><span class="sxs-lookup"><span data-stu-id="71ee4-159">Call [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), with the *outboundTraffic* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the outbound transport layer IPsec callout filter added above.</span></span>
2.  <span data-ttu-id="71ee4-160">Вызовите [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)с параметром *ID* , содержащим идентификатор контекста, возвращенный из [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), и параметр *жетспи* , содержащий IP-адреса 1.1.1.1 & 2.2.2.2, и **ипсекфилтерид** в качестве LUID фильтра выноски IPSec транспортного уровня, добавленного выше.</span><span class="sxs-lookup"><span data-stu-id="71ee4-160">Call [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *getSpi* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the inbound transport layer IPsec callout filter added above.</span></span> <span data-ttu-id="71ee4-161">Возвращенное значение SPI предназначено для использования в качестве SPI входящего SA на локальном компьютере и в качестве исходящего SPI сопоставления безопасности на соответствующем удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="71ee4-161">The returned SPI value is meant to be used as the inbound SA SPI by the local machine and as the outbound SA SPI by the corresponding remote machine.</span></span> <span data-ttu-id="71ee4-162">Оба компьютера должны использовать некоторые нестандартные средства для обмена значениями SPI.</span><span class="sxs-lookup"><span data-stu-id="71ee4-162">Both machines must use some out-of-band means to exchange the SPI values.</span></span>
3.  <span data-ttu-id="71ee4-163">Вызовите [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)с параметром *ID* , содержащим идентификатор контекста, возвращенный из [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), и параметр *ИНБАУНДБУНДЛЕ* , описывающий свойства входящего пакета SA (входящего SA, тип преобразования, типы алгоритмов, ключи и т. д.).</span><span class="sxs-lookup"><span data-stu-id="71ee4-163">Call [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *inboundBundle* parameter describing the properties of the inbound SA bundle (such as the inbound SA SPI, transform type, algorithm types, keys, etc).</span></span>
4.  <span data-ttu-id="71ee4-164">Вызовите [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)с параметром *ID* , содержащим идентификатор контекста, возвращенный из [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), и параметр *аутбаундбундле* , описывающий свойства исходящего пакета SA (например, исходящий SPI SA, тип преобразования, типы алгоритмов, ключи и т. д.).</span><span class="sxs-lookup"><span data-stu-id="71ee4-164">Call [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *outboundBundle* parameter describing the properties of the outbound SA bundle (such as the outbound SA SPI, transform type, algorithm types, keys, etc).</span></span>

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="71ee4-165">См. также</span><span class="sxs-lookup"><span data-stu-id="71ee4-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ee4-166">Пример кода: ключ SA вручную</span><span class="sxs-lookup"><span data-stu-id="71ee4-166">Sample code: Manual SA Keying</span></span>](manual-sa-keying.md)
</dt> <dt>

[<span data-ttu-id="71ee4-167">**Встроенные идентификаторы выноски**</span><span class="sxs-lookup"><span data-stu-id="71ee4-167">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="71ee4-168">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="71ee4-168">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="71ee4-169">**ФВПМ \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="71ee4-169">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

