---
description: Идентификация вызывающей стороны предоставляет сведения о вызывающей стороне при получении входящего сеанса. Приложение обычно использует эти данные как часть сообщения о состоянии пользователю.
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: Идентификация звонящего
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911211"
---
# <a name="caller-identification"></a><span data-ttu-id="f1d25-104">Идентификация звонящего</span><span class="sxs-lookup"><span data-stu-id="f1d25-104">Caller Identification</span></span>

<span data-ttu-id="f1d25-105">Идентификация вызывающей стороны предоставляет сведения о вызывающей стороне при получении входящего сеанса.</span><span class="sxs-lookup"><span data-stu-id="f1d25-105">Caller identification provides information on the calling party when receiving an incoming session.</span></span> <span data-ttu-id="f1d25-106">Приложение обычно использует эти данные как часть сообщения о состоянии пользователю.</span><span class="sxs-lookup"><span data-stu-id="f1d25-106">An application typically uses this data as part of a status message to a user.</span></span>

<span data-ttu-id="f1d25-107">Эта информация не всегда доступна немедленно.</span><span class="sxs-lookup"><span data-stu-id="f1d25-107">This information is not always available immediately.</span></span> <span data-ttu-id="f1d25-108">Приложение, желающее использовать эти сведения и проверило, что поставщик услуг поддерживает его, должен проверить несколько раз, прежде чем предположить, что информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="f1d25-108">An application that wants to use this information and has verified that the service provider supports it should check several times before assuming that the information is not available.</span></span>

<span data-ttu-id="f1d25-109">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f1d25-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f1d25-110">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**двкаллеридфлагс**, **двкаллеридсизе**, **двкаллеридоффсет**, **двкаллериднамесизе**, **dwCallerIDNameOffset** и **dwCallerIDAddressType** lpCallInfo *).*</span><span class="sxs-lookup"><span data-stu-id="f1d25-110">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset**, and **dwCallerIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="f1d25-111">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ каллеридаддресстипе** член [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**иткаллинфо:: Get \_ каллинфостринг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ каллериднаме** и **CI \_ CALLERIDNAME** CALLINFO [**\_ String**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span><span class="sxs-lookup"><span data-stu-id="f1d25-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLERIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLERIDNAME** and **CIS\_CALLERIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
