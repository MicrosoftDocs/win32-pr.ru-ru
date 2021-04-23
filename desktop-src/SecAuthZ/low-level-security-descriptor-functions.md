---
description: Функции для установки и получения дескриптора безопасности объектов.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Функции дескрипторов безопасности низкого уровня '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664658"
---
# <a name="low-level-security-descriptor-functions"></a><span data-ttu-id="e72fe-103">Функции дескрипторов безопасности низкого уровня </span><span class="sxs-lookup"><span data-stu-id="e72fe-103">Low-level Security Descriptor Functions</span></span>

<span data-ttu-id="e72fe-104">Существует несколько пар низкоуровневых функций для установки и извлечения [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly)объекта.</span><span class="sxs-lookup"><span data-stu-id="e72fe-104">There are several pairs of low-level functions for setting and retrieving an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="e72fe-105">Каждая из этих пар работает только с ограниченным набором объектов Windows.</span><span class="sxs-lookup"><span data-stu-id="e72fe-105">Each of these pairs works only with a limited set of Windows objects.</span></span> <span data-ttu-id="e72fe-106">Например, одна пара работает с объектами File, а другая работает с разделами реестра.</span><span class="sxs-lookup"><span data-stu-id="e72fe-106">For example, one pair works with file objects and another works with registry keys.</span></span> <span data-ttu-id="e72fe-107">В следующей таблице показаны низкоуровневые функции для использования с различными типами защищаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="e72fe-107">The following table shows the low-level functions to use with the different types of securable objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e72fe-108">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="e72fe-108">Object type</span></span></th>
<th><span data-ttu-id="e72fe-109">Низкоуровневые функции</span><span class="sxs-lookup"><span data-stu-id="e72fe-109">Low-level functions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e72fe-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Файлы</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Files</a></span></span></li>
<li><span data-ttu-id="e72fe-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Каталоги</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></span></span></li>
<li><span data-ttu-id="e72fe-112">маилслотс</span><span class="sxs-lookup"><span data-stu-id="e72fe-112">Mailslots</span></span></li>
<li><span data-ttu-id="e72fe-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Именованные каналы</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipes</a></span></span></li>
</ul></td>
<td><span data-ttu-id="e72fe-114">Используйте функции <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>жетфилесекурити</strong></a> и <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>сетфилесекурити</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e72fe-114">Use the <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> and <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> functions.</span></span> <span data-ttu-id="e72fe-115">Эти функции используют символьные строки для обнаружения защищаемого объекта вместо использования дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="e72fe-115">These functions use character strings to identify the securable object, instead of using handles.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="e72fe-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Процессы</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processes</a></span></span></li>
<li><span data-ttu-id="e72fe-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Потоки</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span></span></li>
<li><span data-ttu-id="e72fe-118"><a href="access-rights-for-access-token-objects.md">Маркеры доступа в Azure Active Directory</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-118"><a href="access-rights-for-access-token-objects.md">Access tokens</a></span></span></li>
<li><span data-ttu-id="e72fe-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Объекты сопоставления файлов</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File-mapping objects</a></span></span></li>
<li><span data-ttu-id="e72fe-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Семафоры</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphores</a></span></span></li>
<li><span data-ttu-id="e72fe-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">События</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Events</a></span></span></li>
<li><span data-ttu-id="e72fe-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Мьютексы</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></span></span></li>
<li><span data-ttu-id="e72fe-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Ожидающие таймеры</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Waitable timers</a></span></span></li>
</ul></td>
<td><span data-ttu-id="e72fe-124">Используйте функции <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>жеткернелобжектсекурити</strong></a> и <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>сеткернелобжектсекурити</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e72fe-124">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e72fe-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Оконные станции</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window stations</a></span></span></li>
<li><span data-ttu-id="e72fe-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Настольные системы</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span></span></li>
</ul></td>
<td><span data-ttu-id="e72fe-127">Используйте функции <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>жетусеробжектсекурити</strong></a> и <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>сетусеробжектсекурити</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e72fe-127">Use the <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="e72fe-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Разделы реестра</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry keys</a></span></span></li>
</ul></td>
<td><span data-ttu-id="e72fe-129">Используйте функции <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>регжеткэйсекурити</strong></a> и <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>регсеткэйсекурити</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e72fe-129">Use the <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> and <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e72fe-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Объекты службы Windows</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows service objects</a></span></span></li>
</ul></td>
<td><span data-ttu-id="e72fe-131">Используйте функции <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>куерисервицеобжектсекурити</strong></a> и <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>сетсервицеобжектсекурити</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e72fe-131">Use the <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="e72fe-132">Объекты принтера</span><span class="sxs-lookup"><span data-stu-id="e72fe-132">Printer objects</span></span></li>
</ul></td>
<td><span data-ttu-id="e72fe-133">Используйте структуру <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> с функциями <a href="/windows/desktop/printdocs/getprinter"><strong>PrintOut</strong></a> и <a href="/windows/desktop/printdocs/setprinter"><strong>сетпринтер</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e72fe-133">Use the <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> structure with the <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> and <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e72fe-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Общие сетевые папки</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Network shares</a></span></span></li>
</ul></td>
<td><span data-ttu-id="e72fe-135">Используйте уровень 502 с функциями <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>нетшарежетинфо</strong></a> и <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>нетшаресетинфо</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e72fe-135">Use level 502 with the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="e72fe-136"><a href="acl-based-access-control.md">Закрытые объекты (объекты являются частными для создания приложения)</a></span><span class="sxs-lookup"><span data-stu-id="e72fe-136"><a href="acl-based-access-control.md">Private objects (objects private to the creating application)</a></span></span></li>
</ul></td>
<td><span data-ttu-id="e72fe-137">Используйте функции <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>креатеприватеобжектсекурити</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>дестройприватеобжектсекурити</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>жетприватеобжектсекурити</strong></a> и <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e72fe-137">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> functions.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
