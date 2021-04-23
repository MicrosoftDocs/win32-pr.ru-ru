---
description: Скорость или пропускная способность вызова указывает скорость передачи данных. Три точки данных определяют скорость текущего значения максимальной скорости для указанного режима носителя и минимальное значение скорости для режима носителя.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Тариф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40747c26a98d8eb69e8161fb04302c5187121dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674143"
---
# <a name="rate"></a><span data-ttu-id="52cd9-104">Тариф</span><span class="sxs-lookup"><span data-stu-id="52cd9-104">Rate</span></span>

<span data-ttu-id="52cd9-105">Скорость (или пропускная способность) вызова указывает скорость передачи данных.</span><span class="sxs-lookup"><span data-stu-id="52cd9-105">The rate (or bandwidth) of a call specifies the speed of data transmission.</span></span> <span data-ttu-id="52cd9-106">Три точки данных определяют скорость: Текущая скорость, максимальная скорость для указанного режима носителя и минимальная скорость для режима носителя.</span><span class="sxs-lookup"><span data-stu-id="52cd9-106">Three data points identify rate: the current rate, the maximum rate for a specified bearer mode, and the minimum rate for the bearer mode.</span></span>

<span data-ttu-id="52cd9-107">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="52cd9-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="52cd9-108">\* \* TAPI 2. x: \* \*[**линесеткаллпарамс**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двминрате** или **двмаксрате** член [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="52cd9-108">\*\*TAPI 2.x:  \*\*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwMinRate** or **dwMaxRate** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="52cd9-109">\* \* TAPI 3. x: \* \*[**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**иткаллинфо::p UT \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ максрате**, **CIL \_ минрате** или **CIL в \_** [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span><span class="sxs-lookup"><span data-stu-id="52cd9-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_MAXRATE**, **CIL\_MINRATE**, or **CIL\_RATE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

<span data-ttu-id="52cd9-110">\* \* ТСПИ: \* \*[**строка \_ каллинфо**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) сообщение, а для *DWPARAM1* задано \_ значение линекаллинфостате</span><span class="sxs-lookup"><span data-stu-id="52cd9-110">\*\*TSPI:  \*\*[**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_RATE</span></span>

 

 
