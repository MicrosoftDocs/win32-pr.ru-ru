---
description: Идентификатор вызова отличается от идентификатора сеанса двумя основными способами, которым поставщик услуг назначает его, и он одинаков для каждого приложения, которое обрабатывает сеанс.
ms.assetid: c9d0d43b-3053-4e3e-b442-57942f3448df
title: Идентификатор вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef571b55f653cb9c7bc1d61cdc8a3f71e91ba8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683474"
---
# <a name="call-id"></a><span data-ttu-id="9dffe-103">Идентификатор вызова</span><span class="sxs-lookup"><span data-stu-id="9dffe-103">Call ID</span></span>

<span data-ttu-id="9dffe-104">Идентификатор вызова отличается от [идентификатора сеанса](session-identifier-ovr.md) двумя основными способами: поставщик услуг назначает его, и он одинаков для каждого приложения, которое обрабатывает сеанс.</span><span class="sxs-lookup"><span data-stu-id="9dffe-104">The Call ID differs from the [Session Identifier](session-identifier-ovr.md) in two primary ways: the service provider assigns it, and it is the same for every application that handles the session.</span></span> <span data-ttu-id="9dffe-105">Его нельзя использовать для обычного взаимодействия с TAPI, касающихся операций сеанса, так как он не соответствует конкретному приложению.</span><span class="sxs-lookup"><span data-stu-id="9dffe-105">It cannot be used for ordinary communication with TAPI concerning session operations because it does not match to a particular application.</span></span>

<span data-ttu-id="9dffe-106">Идентификатор вызова используется в таких операциях, как определение того, действительно ли группа идентификаторов сеансов ссылается на один вызов, как в случае Конференции или для взаимодействия с другим приложением.</span><span class="sxs-lookup"><span data-stu-id="9dffe-106">The Call ID is used in operations such as determining whether a group of session IDs actually refer to one call, as is the case for a conference, or for communications with another application.</span></span>

<span data-ttu-id="9dffe-107">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="9dffe-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="9dffe-108">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**Двкаллид** Member of [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span><span class="sxs-lookup"><span data-stu-id="9dffe-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallID** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).</span></span>

<span data-ttu-id="9dffe-109">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (элемент **CIL \_ каллид** [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span><span class="sxs-lookup"><span data-stu-id="9dffe-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLID** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).</span></span>

 

 
