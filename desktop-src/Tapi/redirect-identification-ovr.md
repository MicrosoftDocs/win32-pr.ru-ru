---
description: Когда приложение перенаправляет сеанс, TAPI оставляет идентификационную информацию о расположении, которое перенаправляет сеанс, и расположении, в которое оно было перенаправлено.
ms.assetid: 08484b38-7c97-4acc-921e-0f566b2d3415
title: Идентификация перенаправления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa7648167e6f60dc2e8593a576053df9a0ff54eb0fadc9a446a66127b435e5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060452"
---
# <a name="redirect-identification"></a>Идентификация перенаправления

Когда приложение [перенаправляет](redirect-ovr.md) сеанс, TAPI оставляет идентификационную информацию о расположении, которое перенаправляет сеанс, и расположении, в которое оно было перенаправлено.

"Перенаправление" относится к расположению, вызвавшему операцию перенаправления. "Перенаправление" определяет новое назначение для сеанса.

Не все поставщики служб поддерживают использование этих сведений.

* * TAPI 2. x: * *[**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двредиректионидсизе**, **двредиректионидоффсет**, **двредиректиониднамесизе**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** и **dwRedirectingIDNameOffset** члены [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**иткаллинфо:: Get \_ каллинфостринг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)с именем **CI \_ редиректиониднаме**, **CIS \_ редиректиониднумбер**, **CIS \_ редиректингиднаме** или **CI \_ REDIRECTINGIDNUMBER** в [**\_ строке CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
