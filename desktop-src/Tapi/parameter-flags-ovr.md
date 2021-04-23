---
description: Флаги параметров предоставляют сведения о различных флагах состояния для сеанса связи, например, следует ли блокировать идентификацию звонящего. \_Список флагов, определенных TAPI, см. в разделе константы линекаллпарамфлагс.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Флаги параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3adcb8b430045dc41afea4e7f55e5fa4458530b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683411"
---
# <a name="parameter-flags"></a><span data-ttu-id="b0356-104">Флаги параметров</span><span class="sxs-lookup"><span data-stu-id="b0356-104">Parameter Flags</span></span>

<span data-ttu-id="b0356-105">Флаги параметров предоставляют сведения о различных флагах состояния для сеанса связи, например, следует ли блокировать идентификацию звонящего.</span><span class="sxs-lookup"><span data-stu-id="b0356-105">Parameter flags supply information on a variety of status flags concerning a communications session, such as whether caller identification should be blocked.</span></span> <span data-ttu-id="b0356-106">Список флагов, определенных TAPI, см. в разделе [ \_ константы линекаллпарамфлагс](./linecallparamflags--constants.md) .</span><span class="sxs-lookup"><span data-stu-id="b0356-106">See [LINECALLPARAMFLAGS\_ Constants](./linecallparamflags--constants.md) for a list of flags defined by TAPI.</span></span>

<span data-ttu-id="b0356-107">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="b0356-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="b0356-108">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**Двкаллпарамфлагс** Member of *лпкаллинфо*).</span><span class="sxs-lookup"><span data-stu-id="b0356-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallParamFlags** member of *lpCallInfo*).</span></span>

<span data-ttu-id="b0356-109">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (элемент **CIL \_ каллпарамсфлагс** [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="b0356-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLPARAMSFLAGS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
