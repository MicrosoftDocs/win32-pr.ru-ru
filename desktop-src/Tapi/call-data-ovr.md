---
description: Данные вызова — это буфер размера вариабли, который можно использовать для накопления сведений о сеансе связи. Эти сведения становятся доступными для всех приложений, которые владеют и отслеживают сеанс.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Вызов данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344762"
---
# <a name="call-data"></a><span data-ttu-id="d9bbb-104">Вызов данных</span><span class="sxs-lookup"><span data-stu-id="d9bbb-104">Call Data</span></span>

<span data-ttu-id="d9bbb-105">Данные вызова — это буфер размера вариабли, который можно использовать для накопления сведений о сеансе связи.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-105">Call data is a variably sized buffer that can be used to accumulate information about a communications session.</span></span> <span data-ttu-id="d9bbb-106">Эти сведения становятся доступными для всех приложений, которые владеют и отслеживают сеанс.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-106">This information becomes available to all applications that own or monitor the session.</span></span>

<span data-ttu-id="d9bbb-107">Например, начальный обработчик входящего сеанса может запросить и ввести сведения об учетной записи клиента в буфер данных вызова, а затем последующим обработчикам не пришлось повторять запрос.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-107">For example, the initial handler of an incoming session might request and enter client account information into a call data buffer, and then subsequent handlers would not have to repeat the request.</span></span>

<span data-ttu-id="d9bbb-108">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="d9bbb-109">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**линесеткаллдата**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**двкаллдатасизе** and **Двкаллдатаоффсет** Members of [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**Line \_ каллинфо**](./line-callinfo.md) Message (*dwParam1* Set to LINECALLINFOSTATE \_ CALLDATA).</span><span class="sxs-lookup"><span data-stu-id="d9bbb-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_CALLDATA).</span></span>

<span data-ttu-id="d9bbb-110">**Интерфейс TAPI 3. x:** См [**. раздел иткаллинфо::p UT \_ каллинфобуффер**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**ЦИБ \_ каллдатабуффер** Member в [**каллинфо \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**Иткаллинфочанжеевент:: Get \_ Причина**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) Возвращает элемент **ЦИК \_ каллдата** из [**каллинфочанже \_ Причина**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).</span><span class="sxs-lookup"><span data-stu-id="d9bbb-110">**TAPI 3.x:** See [**ITCallInfo::put\_CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB\_CALLDATABUFFER** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) returns the **CIC\_CALLDATA** member of [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).</span></span>

 

 
