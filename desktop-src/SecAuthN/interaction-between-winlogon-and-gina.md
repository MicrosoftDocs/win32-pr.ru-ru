---
description: Winlogon и GINA должны передавать сведения об инициализации, управлять мониторингом последовательности защиты (SAS) и уведомлениями, а также выполнять действия по выходу и завершению работы.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Взаимодействие между Winlogon и GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081395"
---
# <a name="interaction-between-winlogon-and-gina"></a><span data-ttu-id="728ea-103">Взаимодействие между Winlogon и GINA </span><span class="sxs-lookup"><span data-stu-id="728ea-103">Interaction Between Winlogon and GINA</span></span>

<span data-ttu-id="728ea-104">[*Winlogon*](../secgloss/w-gly.md) и [*GINA*](../secgloss/g-gly.md) должны передавать сведения об инициализации, управлять мониторингом [*последовательности защиты*](../secgloss/s-gly.md) (SAS) и уведомлениями, а также выполнять действия по выходу и завершению работы.</span><span class="sxs-lookup"><span data-stu-id="728ea-104">[*Winlogon*](../secgloss/w-gly.md) and the [*GINA*](../secgloss/g-gly.md) must communicate initialization information, handle [*secure attention sequence*](../secgloss/s-gly.md) (SAS) monitoring and notification, and permit logoff and shutdown activities.</span></span> <span data-ttu-id="728ea-105">Состояние Winlogon определяет, какая функция GINA вызывается для обработки любого заданного события SAS.</span><span class="sxs-lookup"><span data-stu-id="728ea-105">The state of Winlogon determines which GINA function is called to process any given SAS event.</span></span> <span data-ttu-id="728ea-106">Связь происходит в порядке, показанном здесь.</span><span class="sxs-lookup"><span data-stu-id="728ea-106">Communications occur in the order shown here.</span></span>

> [!Note]  
> <span data-ttu-id="728ea-107">Библиотеки DLL GINA не учитываются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="728ea-107">GINA DLLs are ignored in Windows Vista.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="728ea-108">Событие</span><span class="sxs-lookup"><span data-stu-id="728ea-108">Event</span></span></th>
<th><span data-ttu-id="728ea-109">Описание</span><span class="sxs-lookup"><span data-stu-id="728ea-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="728ea-110">Загрузка рабочей станции</span><span class="sxs-lookup"><span data-stu-id="728ea-110">Workstation boot</span></span></td>
<td><ol>
<li><span data-ttu-id="728ea-111">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>ВЛКСНЕГОТИАТЕ</strong></a> GINA, чтобы уведомить GINA о используемой версии Winlogon.</span><span class="sxs-lookup"><span data-stu-id="728ea-111">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> function to notify the GINA about the version of Winlogon in use.</span></span></li>
<li><span data-ttu-id="728ea-112">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>ВЛКСИНИТИАЛИЗЕ</strong></a> GINA, чтобы передать модели GINA адреса функций поддержки, обработчику Winlogon и получить сведения о <a href="/windows/desktop/SecGloss/c-gly"><em>контексте</em></a> для модели GINA (для использования во всех будущих вызовах модели GINA).</span><span class="sxs-lookup"><span data-stu-id="728ea-112">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> function to give the GINA the addresses of the support functions, a handle to Winlogon, and to obtain the <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> information for the GINA (to be used in all future calls to the GINA).</span></span><br/> <span data-ttu-id="728ea-113">Winlogon находится в состоянии "выход".</span><span class="sxs-lookup"><span data-stu-id="728ea-113">Winlogon is in the logged-out state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="728ea-114">Никто не вошел в систему</span><span class="sxs-lookup"><span data-stu-id="728ea-114">No one is logged on</span></span></td>
<td><span data-ttu-id="728ea-115">(GINA отслеживает устройства для событий SAS).</span><span class="sxs-lookup"><span data-stu-id="728ea-115">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="728ea-116">GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>Влкссаснотифи</strong></a> Winlogon при получении события SAS.</span><span class="sxs-lookup"><span data-stu-id="728ea-116">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="728ea-117">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>ВЛКСЛОГЖЕДАУТСАС</strong></a> GINA, позволяя GINA обрабатывать данные идентификации пользователя и проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="728ea-117">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> function, allowing the GINA to process a user's identification and authentication information.</span></span><br/> <span data-ttu-id="728ea-118">После успешного входа в систему Winlogon находится в состоянии "в системе".</span><span class="sxs-lookup"><span data-stu-id="728ea-118">When logon is successful, Winlogon is in the logged-on state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="728ea-119">Пользователь вошел в систему</span><span class="sxs-lookup"><span data-stu-id="728ea-119">The user is logged on</span></span></td>
<td><span data-ttu-id="728ea-120">(GINA отслеживает устройства для событий SAS).</span><span class="sxs-lookup"><span data-stu-id="728ea-120">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="728ea-121">GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>Влкссаснотифи</strong></a> Winlogon при получении события SAS.</span><span class="sxs-lookup"><span data-stu-id="728ea-121">The GINA calls Winlogon's <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function when a SAS event has been received.</span></span></li>
<li><span data-ttu-id="728ea-122">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>ВЛКСЛОГЖЕДОНСАС</strong></a> GINA, позволяя модели GINA предоставлять параметры пользователю, который в данный момент вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="728ea-122">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function, allowing the GINA to present options to the user who is currently logged on.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="728ea-123">Пользователь вошел в систему и хочет заблокировать компьютер</span><span class="sxs-lookup"><span data-stu-id="728ea-123">The user is logged on and wants to lock computer</span></span></td>
<td><span data-ttu-id="728ea-124">(GINA отслеживает устройства для событий SAS).</span><span class="sxs-lookup"><span data-stu-id="728ea-124">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="728ea-125">GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>влкссаснотифи</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="728ea-125">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-126">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>ВЛКСЛОГЖЕДОНСАС</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-126">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-127">GINA возвращает WLX_SAS_ACTION_LOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="728ea-127">The GINA returns WLX_SAS_ACTION_LOCK_WKSTA.</span></span><br/> <span data-ttu-id="728ea-128">Winlogon находится в состоянии блокировки рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="728ea-128">Winlogon is in the workstation-locked state.</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="728ea-129">Пользователь вошел в систему, Рабочая станция заблокирована, и пользователь хочет разблокировать компьютер</span><span class="sxs-lookup"><span data-stu-id="728ea-129">The user is logged on, the workstation is locked, and the user wants to unlock computer</span></span></td>
<td><span data-ttu-id="728ea-130">(GINA отслеживает устройства для событий SAS).</span><span class="sxs-lookup"><span data-stu-id="728ea-130">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="728ea-131">GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>влкссаснотифи</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="728ea-131">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-132">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>ВЛКСВКСТАЛОККЕДСАС</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-132">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-133">GINA возвращает WLX_SAS_ACTION_UNLOCK_WKSTA.</span><span class="sxs-lookup"><span data-stu-id="728ea-133">The GINA returns WLX_SAS_ACTION_UNLOCK_WKSTA.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="728ea-134">Пользователь вошел в систему, и программа вызывает функцию <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="728ea-134">The user is logged on, and the program calls the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> function</span></span></td>
<td><span data-ttu-id="728ea-135">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>ВЛКСЛОГОФФ</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-135">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="728ea-136">Пользователь вошел в систему и хочет выйти из системы с помощью SAS.</span><span class="sxs-lookup"><span data-stu-id="728ea-136">The user is logged on and wants to log off by using SAS</span></span></td>
<td><span data-ttu-id="728ea-137">(GINA отслеживает устройства для событий SAS).</span><span class="sxs-lookup"><span data-stu-id="728ea-137">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="728ea-138">GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>влкссаснотифи</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="728ea-138">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-139">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>ВЛКСЛОГЖЕДОНСАС</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-139">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-140">GINA возвращает WLX_SAS_ACTION_LOGOFF.</span><span class="sxs-lookup"><span data-stu-id="728ea-140">The GINA returns WLX_SAS_ACTION_LOGOFF.</span></span></li>
<li><span data-ttu-id="728ea-141">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>ВЛКСЛОГОФФ</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-141">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="728ea-142">Пользователь вошел в систему и хочет выйти из системы и завершить работу с помощью функции <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong> .</a></span><span class="sxs-lookup"><span data-stu-id="728ea-142">The user is logged on and wants to log off and shut down by using <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="728ea-143">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>ВЛКСЛОГОФФ</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-143">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-144">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>ВЛКСШУТДОВН</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-144">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="728ea-145">Пользователь вошел в систему и хочет выйти из системы и завершить работу с помощью SAS.</span><span class="sxs-lookup"><span data-stu-id="728ea-145">The user is logged on and wants to log off and shut down by using SAS</span></span></td>
<td><span data-ttu-id="728ea-146">(GINA отслеживает устройства для событий SAS).</span><span class="sxs-lookup"><span data-stu-id="728ea-146">(The GINA monitors devices for SAS events).</span></span>
<ol>
<li><span data-ttu-id="728ea-147">GINA вызывает функцию <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>влкссаснотифи</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="728ea-147">The GINA calls the <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-148">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>ВЛКСЛОГЖЕДОНСАС</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-148">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-149">GINA возвращает WLX_SAS_ACTION_SHUTDOWN.</span><span class="sxs-lookup"><span data-stu-id="728ea-149">The GINA returns WLX_SAS_ACTION_SHUTDOWN.</span></span></li>
<li><span data-ttu-id="728ea-150">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>ВЛКСЛОГОФФ</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-150">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> function.</span></span></li>
<li><span data-ttu-id="728ea-151">Winlogon вызывает функцию <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>ВЛКСШУТДОВН</strong></a> GINA.</span><span class="sxs-lookup"><span data-stu-id="728ea-151">Winlogon calls the GINA's <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> function.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
