---
description: Когда приложение перенаправляет сеанс, TAPI оставляет идентификационную информацию о расположении, которое перенаправляет сеанс, и расположении, в которое оно было перенаправлено.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Идентификация перенаправления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8316b7d1566a24ead21f7b1fdf2d16b1c48a2b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684670"
---
# <a name="redirect-identification"></a><span data-ttu-id="33a57-103">Идентификация перенаправления</span><span class="sxs-lookup"><span data-stu-id="33a57-103">Redirect Identification</span></span>

<span data-ttu-id="33a57-104">Когда приложение [перенаправляет](redirect-ovr.md) сеанс, TAPI оставляет идентификационную информацию о расположении, которое перенаправляет сеанс, и расположении, в которое оно было перенаправлено.</span><span class="sxs-lookup"><span data-stu-id="33a57-104">When an application [redirects](redirect-ovr.md) a session, TAPI retains identification information about the location that redirected the session and the location to which it was redirected.</span></span>

<span data-ttu-id="33a57-105">"Перенаправление" относится к расположению, вызвавшему операцию перенаправления.</span><span class="sxs-lookup"><span data-stu-id="33a57-105">"Redirecting" refers to the location that invoked the redirect operation.</span></span> <span data-ttu-id="33a57-106">"Перенаправление" определяет новое назначение для сеанса.</span><span class="sxs-lookup"><span data-stu-id="33a57-106">"Redirection" identifies the new destination for the session.</span></span>

<span data-ttu-id="33a57-107">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="33a57-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="33a57-108">\* \* TAPI 2. x: \* \*[**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двредиректионидсизе**, **двредиректионидоффсет**, **двредиректиониднамесизе**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** и **dwRedirectingIDNameOffset** члены [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="33a57-108">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwRedirectionIDSize**, **dwRedirectionIDOffset**, **dwRedirectionIDNameSize**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize**, and **dwRedirectingIDNameOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="33a57-109">\* \* TAPI 3. x: \* \*[**иткаллинфо:: Get \_ каллинфостринг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)с именем **CI \_ редиректиониднаме**, **CIS \_ редиректиониднумбер**, **CIS \_ редиректингиднаме** или **CI \_ REDIRECTINGIDNUMBER** в [**\_ строке CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span><span class="sxs-lookup"><span data-stu-id="33a57-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)called with the **CIS\_REDIRECTIONIDNAME**, **CIS\_REDIRECTIONIDNUMBER**, **CIS\_REDIRECTINGIDNAME**, or **CIS\_REDIRECTINGIDNUMBER** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)</span></span>

 

 
