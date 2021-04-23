---
description: Сведения, относящиеся к приложению, позволяют приложениям передавать каждую другую информацию, касающуюся сеанса, через TAPI. Эти сведения не обрабатываются интерфейсом TAPI, и их использование полностью определяется приложениями.
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: Сведения, относящиеся к приложению
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674478"
---
# <a name="application-specific-information"></a><span data-ttu-id="a946f-104">Сведения, относящиеся к приложению</span><span class="sxs-lookup"><span data-stu-id="a946f-104">Application-specific Information</span></span>

<span data-ttu-id="a946f-105">Сведения, относящиеся к приложению, позволяют приложениям передавать каждую другую информацию, касающуюся сеанса, через TAPI.</span><span class="sxs-lookup"><span data-stu-id="a946f-105">Application-specific information allows applications to pass each other information concerning a session through TAPI.</span></span> <span data-ttu-id="a946f-106">Эти сведения не обрабатываются интерфейсом TAPI, и их использование полностью определяется приложениями.</span><span class="sxs-lookup"><span data-stu-id="a946f-106">This information is not interpreted by TAPI and usage is entirely defined by the applications.</span></span>

<span data-ttu-id="a946f-107">Когда информация, относящаяся к приложению, изменяется одним приложением, TAPI отправляет всем другим приложениям с правами монитора или владельца в сеансе событие, указывающее на то, что произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="a946f-107">When application-specific information is changed by one application, TAPI sends all other applications with monitor or owner privileges on the session an event indicating that a change has occurred.</span></span>

<span data-ttu-id="a946f-108">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="a946f-108">Not all service providers support use of this information.</span></span>

<span data-ttu-id="a946f-109">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (член *дваппспеЦифик* *лпкаллинфо*), [**линесетаппспеЦифик**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**строка \_ каллинфо**](./line-callinfo.md) сообщение (*dwParam1* задано в линекаллинфостате \_ ).</span><span class="sxs-lookup"><span data-stu-id="a946f-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*dwAppSpecific* member of *lpCallInfo*), [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific), [**LINE\_CALLINFO**](./line-callinfo.md) message (*dwParam1* set to LINECALLINFOSTATE\_APPSPECIFIC).</span></span>

<span data-ttu-id="a946f-110">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**иткаллинфо::p UT \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (элемент,**\_ определяемый CIL** в [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="a946f-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL\_APPSPECIFIC** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
