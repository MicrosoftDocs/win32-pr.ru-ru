---
description: Вызываемая идентификация идентифицирует исходный адрес назначения для сеанса. В ситуациях, когда сеанс был перенаправлен, переадресован или передан, он будет отличаться от подключенной идентификации.
ms.assetid: a03286eb-83a9-4170-b514-e8899fd04c74
title: Вызываемая идентификация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f862d18fb3deb661cb8379c90a4b3e70caab1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911212"
---
# <a name="called-identification"></a><span data-ttu-id="3f783-104">Вызываемая идентификация</span><span class="sxs-lookup"><span data-stu-id="3f783-104">Called Identification</span></span>

<span data-ttu-id="3f783-105">Вызываемая идентификация идентифицирует исходный адрес назначения для сеанса.</span><span class="sxs-lookup"><span data-stu-id="3f783-105">Called identification identifies the original destination address for a session.</span></span> <span data-ttu-id="3f783-106">В ситуациях, когда сеанс был перенаправлен, переадресован или передан, он будет отличаться от [подключенной идентификации](connected-identification-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="3f783-106">In situations where a session was redirected, forwarded, or transferred, this will be different than the [connected identification](connected-identification-ovr.md).</span></span>

<span data-ttu-id="3f783-107">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="3f783-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="3f783-108">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**двкалледидфлагс**, **двкалледидсизе**, **двкалледидоффсет**, **двкалледиднамесизе**, **dwCalledIDNameOffset** и **dwCalledIDAddressType** lpCallInfo *).*</span><span class="sxs-lookup"><span data-stu-id="3f783-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCalledIDFlags**, **dwCalledIDSize**, **dwCalledIDOffset**, **dwCalledIDNameSize**, **dwCalledIDNameOffset**, and **dwCalledIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="3f783-109">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ калледидаддресстипе** член [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**иткаллинфо:: Get \_ каллинфостринг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ калледиднаме** и **CI \_ CALLEDIDNAME** CALLINFO [**\_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="3f783-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLEDIDNAME** and **CIS\_CALLEDIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
