---
description: Привилегия указывает, владеет ли приложение или отслеживает сеанс.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilege
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684049"
---
# <a name="privilege"></a><span data-ttu-id="6a9a7-103">Privilege</span><span class="sxs-lookup"><span data-stu-id="6a9a7-103">Privilege</span></span>

<span data-ttu-id="6a9a7-104">Привилегия указывает, владеет ли приложение или отслеживает сеанс.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-104">Privilege refers to whether an application owns or is monitoring the session.</span></span> <span data-ttu-id="6a9a7-105">Если приложение владеет сеансом, ему разрешается выполнять различные операции с сеансами.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-105">If the application owns the session, it is allowed to perform a variety of session operations.</span></span> <span data-ttu-id="6a9a7-106">Если приложение наблюдает только, оно получит сообщения о состоянии и сможет получить доступ к сведениям о сеансе, но любая попытка выполнить большинство операций приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-106">If the application is only monitoring, it will receive state messages and it can access session information, but any attempt to perform most operations will result in an error.</span></span>

<span data-ttu-id="6a9a7-107">Во время инициализации приложение сообщает TAPI, какой уровень привилегий требуется для этих адресов.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-107">During initialization, an application tells TAPI which privilege level it requires on which addresses.</span></span> <span data-ttu-id="6a9a7-108">TAPI предоставляет входящие сеансы только для приложений, зарегистрированных для владельца или владельца и прав монитора.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-108">TAPI offers incoming sessions only to applications that have registered for either owner or owner and monitor privilege.</span></span>

<span data-ttu-id="6a9a7-109">Права приложения в создаваемом сеансе всегда являются владельцами.</span><span class="sxs-lookup"><span data-stu-id="6a9a7-109">An application's privilege on a session it creates is always owner.</span></span>

<span data-ttu-id="6a9a7-110">**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллстатус**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **Двкаллпривилеже** , элемент [**линекаллстатус**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**линесеткаллпривилеже**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span><span class="sxs-lookup"><span data-stu-id="6a9a7-110">**TAPI 2.x:** See [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span></span>

<span data-ttu-id="6a9a7-111">**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ привилегия**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), который вызывается с помощью элемента **CIL \_ нумберофовнерс** или **CIL \_ нумберофмониторс** [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="6a9a7-111">**TAPI 3.x:** See [**ITCallInfo::get\_Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_NUMBEROFOWNERS** or **CIL\_NUMBEROFMONITORS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
