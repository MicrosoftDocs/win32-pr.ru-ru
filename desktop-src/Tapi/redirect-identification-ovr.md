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
# <a name="redirect-identification"></a>Идентификация перенаправления

Когда приложение [перенаправляет](redirect-ovr.md) сеанс, TAPI оставляет идентификационную информацию о расположении, которое перенаправляет сеанс, и расположении, в которое оно было перенаправлено.

"Перенаправление" относится к расположению, вызвавшему операцию перенаправления. "Перенаправление" определяет новое назначение для сеанса.

Не все поставщики служб поддерживают использование этих сведений.

* * TAPI 2. x: * *[**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двредиректионидсизе**, **двредиректионидоффсет**, **двредиректиониднамесизе**, **dwRedirectionIDNameOffset**, **dwRedirectingIDSize**, **dwRedirectingIDOffset**, **dwRedirectingIDNameSize** и **dwRedirectingIDNameOffset** члены [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**иткаллинфо:: Get \_ каллинфостринг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring)с именем **CI \_ редиректиониднаме**, **CIS \_ редиректиониднумбер**, **CIS \_ редиректингиднаме** или **CI \_ REDIRECTINGIDNUMBER** в [**\_ строке CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)

 

 
