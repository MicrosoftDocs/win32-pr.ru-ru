---
description: Параметр Стрпривилеже метода Свбемпривилежесет. Аддасстринг и параметр Ипривилеже для Свбемпривилежесет. Add требуются строки прав доступа из Вбемпривилежеенум.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Константы прав доступа (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818048"
---
# <a name="privilege-constants"></a><span data-ttu-id="a33d3-103">Константы прав доступа</span><span class="sxs-lookup"><span data-stu-id="a33d3-103">Privilege Constants</span></span>

<span data-ttu-id="a33d3-104">Параметр *стрпривилеже* метода [**свбемпривилежесет. Аддасстринг**](swbemprivilegeset-addasstring.md) и параметр *ипривилеже* для [**свбемпривилежесет. Add**](swbemprivilegeset-add.md) требуются строки прав доступа из [вбемпривилежеенум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="a33d3-104">The *strPrivilege* parameter of the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method and the *iPrivilege* parameter for [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) require privilege strings from [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="a33d3-105">Дополнительные сведения об использовании констант прав доступа см. в разделе [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="a33d3-105">For more information about how to use privilege constants, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="a33d3-106">В [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)определены следующие константы.</span><span class="sxs-lookup"><span data-stu-id="a33d3-106">The following constants are defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="a33d3-107">В следующем списке приводятся эквивалентные константы для C++ и строки для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="a33d3-107">The following list includes the equivalent constants for C++ and strings for scripting.</span></span> <span data-ttu-id="a33d3-108">Для формирования краткого имени скрипта удалите слова "SE" и "Privilege" из имени константы C++.</span><span class="sxs-lookup"><span data-stu-id="a33d3-108">To form the scripting short name, remove the "Se" and "Privilege" from the C++ constant name.</span></span>

<span data-ttu-id="a33d3-109">В следующем примере кода VBScript показано, как включить привилегию Ремотешутдовн в скрипте.</span><span class="sxs-lookup"><span data-stu-id="a33d3-109">The following VBScript code example shows how to enable the RemoteShutdown privilege in a script.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



<span data-ttu-id="a33d3-110">Для многих методов WMI необходимо включить одно или несколько разрешений.</span><span class="sxs-lookup"><span data-stu-id="a33d3-110">Many WMI methods require that one or more permission be enabled.</span></span> <span data-ttu-id="a33d3-111">Если учетной записи не предоставлено право, ее нельзя включить для вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a33d3-111">If an account has not been granted a privilege, it cannot be enabled for the method call.</span></span>

<dl> <dt>

<span data-ttu-id="a33d3-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**вбемпривилежекреатетокен**</span><span class="sxs-lookup"><span data-stu-id="a33d3-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a33d3-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-114">Константа C++: **SE \_ Create \_ Token \_ Name** строка: **секреатетокенпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-114">C++ constant: **SE\_CREATE\_TOKEN\_NAME** string: **SeCreateTokenPrivilege**</span></span>

<span data-ttu-id="a33d3-115">Короткое имя сценария: **креатетокен**</span><span class="sxs-lookup"><span data-stu-id="a33d3-115">Scripting short name: **CreateToken**</span></span>

<span data-ttu-id="a33d3-116">Требуется для создания объекта первичного токена.</span><span class="sxs-lookup"><span data-stu-id="a33d3-116">Required to create a primary token object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**вбемпривилежепримаритокен**</span><span class="sxs-lookup"><span data-stu-id="a33d3-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-118">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="a33d3-118">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-119">Константа C++: строка **SeAssignPrimaryTokenPrivilege** : **SeAssignPrimaryTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-119">C++ constant: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**</span></span>

<span data-ttu-id="a33d3-120">Короткое имя сценария: **ассигнпримаритокен**</span><span class="sxs-lookup"><span data-stu-id="a33d3-120">Scripting short name: **AssignPrimaryToken**</span></span>

<span data-ttu-id="a33d3-121">Требуется для замены маркера уровня процесса.</span><span class="sxs-lookup"><span data-stu-id="a33d3-121">Required to replace a process-level token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**вбемпривилежелоккмемори**</span><span class="sxs-lookup"><span data-stu-id="a33d3-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-123">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="a33d3-123">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-124">Константа C++: **SE \_ Lock \_ Memory \_ Name** строка: **SeLockMemoryPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-124">C++ constant: **SE\_LOCK\_MEMORY\_NAME** string: **SeLockMemoryPrivilege**</span></span>

<span data-ttu-id="a33d3-125">Короткое имя сценария: **локкмемори**</span><span class="sxs-lookup"><span data-stu-id="a33d3-125">Scripting short name: **LockMemory**</span></span>

<span data-ttu-id="a33d3-126">Требуется для блокировки страниц в памяти.</span><span class="sxs-lookup"><span data-stu-id="a33d3-126">Required to lock pages in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**вбемпривилежеинкреасекуота**</span><span class="sxs-lookup"><span data-stu-id="a33d3-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="a33d3-128">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-129">Константа с + +: **SE \_ увеличить \_ \_ имя квоты** : **SeIncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-129">C++ constant: **SE\_INCREASE\_QUOTA\_NAME** string: **SeIncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="a33d3-130">Короткое имя сценария: **инкреасекуотапривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-130">Scripting short name: **IncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="a33d3-131">Требуется для настройки квот памяти для процесса.</span><span class="sxs-lookup"><span data-stu-id="a33d3-131">Required to adjust memory quotas for a process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**вбемпривилежемачинеаккаунт**</span><span class="sxs-lookup"><span data-stu-id="a33d3-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-133">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="a33d3-133">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-134">Константа C++: строка **\_ \_ \_ имени учетной записи SE машина** : **семачинеаккаунтпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-134">C++ constant: **SE\_MACINE\_ACCOUNT\_NAME** string: **SeMachineAccountPrivilege**</span></span>

<span data-ttu-id="a33d3-135">Короткое имя сценария: **мачинеаккаунт**</span><span class="sxs-lookup"><span data-stu-id="a33d3-135">Scripting short name: **MachineAccount**</span></span>

<span data-ttu-id="a33d3-136">Требуется для добавления рабочих станций в домен.</span><span class="sxs-lookup"><span data-stu-id="a33d3-136">Required to add workstations to a domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**вбемпривилежеткб**</span><span class="sxs-lookup"><span data-stu-id="a33d3-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-138">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="a33d3-138">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-139">Константа C++ **: \_ SE \_ имя TCB** строка: **SeTcbPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-139">C++ constant: **SE\_TCB\_NAME** string: **SeTcbPrivilege**</span></span>

<span data-ttu-id="a33d3-140">Короткое имя сценария: **TCB**</span><span class="sxs-lookup"><span data-stu-id="a33d3-140">Scripting short name: **Tcb**</span></span>

<span data-ttu-id="a33d3-141">Требуется для работы в составе операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a33d3-141">Required to act as part of the operating system.</span></span> <span data-ttu-id="a33d3-142">Владелец является частью базы доверенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a33d3-142">The holder is part of the trusted computer base.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**вбемпривилежесекурити**</span><span class="sxs-lookup"><span data-stu-id="a33d3-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-144">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="a33d3-144">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-145">Константа C++: строка **\_ \_ имени безопасности SE** : **SeSecurityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-145">C++ constant: **SE\_SECURITY\_NAME** string: **SeSecurityPrivilege**</span></span>

<span data-ttu-id="a33d3-146">Короткое имя сценария: **Безопасность**</span><span class="sxs-lookup"><span data-stu-id="a33d3-146">Scripting short name: **Security**</span></span>

<span data-ttu-id="a33d3-147">Требуется для управления аудитом и журналом безопасности NT.</span><span class="sxs-lookup"><span data-stu-id="a33d3-147">Required to manage auditing and the NT security log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**вбемпривилежетакеовнершип**</span><span class="sxs-lookup"><span data-stu-id="a33d3-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-149">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="a33d3-149">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-150">Константа C++ **: \_ SE \_ взять \_ имя владельца** строка: **сетакеовнершиппривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-150">C++ constant: **SE\_TAKE\_OWNERSHIP\_NAME** string: **SeTakeOwnershipPrivilege**</span></span>

<span data-ttu-id="a33d3-151">Короткое имя сценария: **такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="a33d3-151">Scripting short name: **TakeOwnership**</span></span>

<span data-ttu-id="a33d3-152">Требуется для того, чтобы стать владельцем файлов или других объектов без [*записи контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE) в *списке управления доступом на уровне пользователей* (DACL).</span><span class="sxs-lookup"><span data-stu-id="a33d3-152">Required to assume ownership of files or other objects without having an [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE) in the *discretionary access control list* (DACL).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**вбемпривилежелоаддривер**</span><span class="sxs-lookup"><span data-stu-id="a33d3-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-154">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="a33d3-154">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-155">Константа C++: **SE \_ Load \_ драйвер** строка: **селоаддриверпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-155">C++ constant: **SE\_LOAD\_DRIVER** string: **SeLoadDriverPrivilege**</span></span>

<span data-ttu-id="a33d3-156">Короткое имя сценария: **лоаддривер**</span><span class="sxs-lookup"><span data-stu-id="a33d3-156">Scripting short name: **LoadDriver**</span></span>

<span data-ttu-id="a33d3-157">Требуется для загрузки или выгрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="a33d3-157">Required to load or unload a device driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**вбемпривилежесистемпрофиле**</span><span class="sxs-lookup"><span data-stu-id="a33d3-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-159">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="a33d3-159">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-160">Константа C++: строка **\_ \_ \_ имени системного профиля SE** : **сесистемпрофилепривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-160">C++ constant: **SE\_SYSTEM\_PROFILE\_NAME** string: **SeSystemProfilePrivilege**</span></span>

<span data-ttu-id="a33d3-161">Короткое имя сценария: **SystemProfile**</span><span class="sxs-lookup"><span data-stu-id="a33d3-161">Scripting short name: **SystemProfile**</span></span>

<span data-ttu-id="a33d3-162">Требуется для сбора сведений о профиле производительности системы.</span><span class="sxs-lookup"><span data-stu-id="a33d3-162">Required to gather profile information about system performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**вбемпривилежесистемтиме**</span><span class="sxs-lookup"><span data-stu-id="a33d3-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-164">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="a33d3-164">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-165">Константа C++: **SE \_ SYSTEMTIME** \_ name string: **сесистемтимепривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-165">C++ constant: **SE\_SYSTEMTIME**\_NAME string: **SeSystemtimePrivilege**</span></span>

<span data-ttu-id="a33d3-166">Короткое имя сценария: **SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="a33d3-166">Scripting short name: **Systemtime**</span></span>

<span data-ttu-id="a33d3-167">Требуется для изменения системного времени.</span><span class="sxs-lookup"><span data-stu-id="a33d3-167">Required to change the system time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**вбемпривилежепрофилесинглепроцесс**</span><span class="sxs-lookup"><span data-stu-id="a33d3-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-169">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="a33d3-169">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-170">Константа C++: **SE \_ Prof \_ Single \_ Process \_ Name** строка: **сепрофилесинглепроцесспривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-170">C++ constant: **SE\_PROF\_SINGLE\_PROCESS\_NAME** string: **SeProfileSingleProcessPrivilege**</span></span>

<span data-ttu-id="a33d3-171">Короткое имя сценария: **профилесинглепроцесс**</span><span class="sxs-lookup"><span data-stu-id="a33d3-171">Scripting short name: **ProfileSingleProcess**</span></span>

<span data-ttu-id="a33d3-172">Требуется для сбора сведений о профиле для одного процесса.</span><span class="sxs-lookup"><span data-stu-id="a33d3-172">Required to gather profile information for a single process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**вбемпривилежеинкреасебасеприорити**</span><span class="sxs-lookup"><span data-stu-id="a33d3-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-174">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="a33d3-174">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-175">Константа C++: строка **\_ \_ \_ \_ имени базового приоритета для SE Inc** : **SeIncreaseBasePriorityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-175">C++ constant: **SE\_INC\_BASE\_PRIORITY\_NAME** string: **SeIncreaseBasePriorityPrivilege**</span></span>

<span data-ttu-id="a33d3-176">Короткое имя сценария: **инкреасебасеприорити**</span><span class="sxs-lookup"><span data-stu-id="a33d3-176">Scripting short name: **IncreaseBasePriority**</span></span>

<span data-ttu-id="a33d3-177">Требуется для увеличения приоритета планирования.</span><span class="sxs-lookup"><span data-stu-id="a33d3-177">Required to increase scheduling priority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**вбемпривилежекреатепажефиле**</span><span class="sxs-lookup"><span data-stu-id="a33d3-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-179">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="a33d3-179">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-180">Константа C++: **SE \_ Create \_ pagefile \_ Name** строка: **секреатепажефилепривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-180">C++ constant: **SE\_CREATE\_PAGEFILE\_NAME** string: **SeCreatePagefilePrivilege**</span></span>

<span data-ttu-id="a33d3-181">Короткое имя сценария: **креатепажефиле**</span><span class="sxs-lookup"><span data-stu-id="a33d3-181">Scripting short name: **CreatePagefile**</span></span>

<span data-ttu-id="a33d3-182">Требуется для создания файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="a33d3-182">Required to create a pagefile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**вбемпривилежекреатеперманент**</span><span class="sxs-lookup"><span data-stu-id="a33d3-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-184">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="a33d3-184">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-185">Константа C++: **SE \_ создать строку \_ постоянного \_ имени** : **секреатеперманентпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-185">C++ constant: **SE\_CREATE\_PERMANENT\_NAME** string: **SeCreatePermanentPrivilege**</span></span>

<span data-ttu-id="a33d3-186">Короткое имя сценария: **креатеперманент**</span><span class="sxs-lookup"><span data-stu-id="a33d3-186">Scripting short name: **CreatePermanent**</span></span>

<span data-ttu-id="a33d3-187">Требуется для создания постоянных общих объектов.</span><span class="sxs-lookup"><span data-stu-id="a33d3-187">Required to create permanent shared objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**вбемпривилежебаккуп**</span><span class="sxs-lookup"><span data-stu-id="a33d3-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-189">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="a33d3-189">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-190">Константа C++: **SE \_ BACKUP \_ Name** , строка: **себаккуппривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-190">C++ constant: **SE\_BACKUP\_NAME** string: **SeBackupPrivilege**</span></span>

<span data-ttu-id="a33d3-191">Короткое имя сценария: **резервное копирование**</span><span class="sxs-lookup"><span data-stu-id="a33d3-191">Scripting short name: **Backup**</span></span>

<span data-ttu-id="a33d3-192">Требуется для резервного копирования файлов и каталогов, независимо от списка ACL, указанного для файла.</span><span class="sxs-lookup"><span data-stu-id="a33d3-192">Required to backup files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**вбемпривилежересторе**</span><span class="sxs-lookup"><span data-stu-id="a33d3-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-194">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="a33d3-194">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-195">Константа C++: **SE \_ RESTORE \_ Name** String: **сересторепривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-195">C++ constant: **SE\_RESTORE\_NAME** string: **SeRestorePrivilege**</span></span>

<span data-ttu-id="a33d3-196">Короткое имя сценария: **RESTORE**</span><span class="sxs-lookup"><span data-stu-id="a33d3-196">Scripting short name: **Restore**</span></span>

<span data-ttu-id="a33d3-197">Требуется для восстановления файлов и каталогов независимо от списка ACL, указанного для файла.</span><span class="sxs-lookup"><span data-stu-id="a33d3-197">Required to restore files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**вбемпривилежешутдовн**</span><span class="sxs-lookup"><span data-stu-id="a33d3-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-199">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="a33d3-199">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-200">Константа C++: **SE \_ Shutdown \_ имя** строки: **сешутдовнпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-200">C++ constant: **SE\_SHUTDOWN\_NAME** string: **SeShutdownPrivilege**</span></span>

<span data-ttu-id="a33d3-201">Короткое имя сценария: **Завершение работы**</span><span class="sxs-lookup"><span data-stu-id="a33d3-201">Scripting short name: **Shutdown**</span></span>

<span data-ttu-id="a33d3-202">Требуется для завершения работы локальной системы.</span><span class="sxs-lookup"><span data-stu-id="a33d3-202">Required to shut down the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**вбемпривилежедебуг**</span><span class="sxs-lookup"><span data-stu-id="a33d3-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-204">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="a33d3-204">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-205">Константа C++: строка **\_ \_ имени отладки** : **SeDebugPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-205">C++ constant: **SE\_DEBUG\_NAME** string: **SeDebugPrivilege**</span></span>

<span data-ttu-id="a33d3-206">Короткое имя сценария: **Отладка**</span><span class="sxs-lookup"><span data-stu-id="a33d3-206">Scripting short name: **Debug**</span></span>

<span data-ttu-id="a33d3-207">Требуется для отладки и корректировки памяти процесса, принадлежащего другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a33d3-207">Required to debug and adjust the memory of a process owned by another account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**вбемпривилежеаудит**</span><span class="sxs-lookup"><span data-stu-id="a33d3-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-209">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="a33d3-209">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-210">Константа C++: **SE \_ Audit \_ Name** , строка: **SeAuditPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-210">C++ constant: **SE\_AUDIT\_NAME** string: **SeAuditPrivilege**</span></span>

<span data-ttu-id="a33d3-211">Короткое имя сценария: **Аудит**</span><span class="sxs-lookup"><span data-stu-id="a33d3-211">Scripting short name: **Audit**</span></span>

<span data-ttu-id="a33d3-212">Требуется для создания записей аудита в журнале безопасности NT.</span><span class="sxs-lookup"><span data-stu-id="a33d3-212">Required to generate audit entries in the NT Security log.</span></span> <span data-ttu-id="a33d3-213">Эта привилегия должна иметь только защищенные серверы.</span><span class="sxs-lookup"><span data-stu-id="a33d3-213">Only secure servers should have this privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**вбемпривилежесистеменвиронмент**</span><span class="sxs-lookup"><span data-stu-id="a33d3-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-215">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="a33d3-215">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-216">Константа C++: строка **\_ \_ \_ имени системной среды SE** : **сесистеменвиронментпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-216">C++ constant: **SE\_SYSTEM\_ENVIRONMENT\_NAME** string: **SeSystemEnvironmentPrivilege**</span></span>

<span data-ttu-id="a33d3-217">Короткое имя сценария: **системенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="a33d3-217">Scripting short name: **SystemEnvironment**</span></span>

<span data-ttu-id="a33d3-218">Требуется для изменения энергонезависимого ОЗУ систем, использующих этот тип памяти для хранения данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a33d3-218">Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**вбемпривилежечанженотифи**</span><span class="sxs-lookup"><span data-stu-id="a33d3-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-220">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="a33d3-220">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-221">Константа C++ **: \_ SE \_ изменить \_ имя уведомления** строка: **SeChangeNotifyPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-221">C++ constant: **SE\_CHANGE\_NOTIFY\_NAME** string: **SeChangeNotifyPrivilege**</span></span>

<span data-ttu-id="a33d3-222">Короткое имя сценария: **чанженотифи**</span><span class="sxs-lookup"><span data-stu-id="a33d3-222">Scripting short name: **ChangeNotify**</span></span>

<span data-ttu-id="a33d3-223">Требуется для получения уведомлений об изменениях в файлах или каталогах и обхода проверок доступа для обхода.</span><span class="sxs-lookup"><span data-stu-id="a33d3-223">Required to receive notifications of changes to files or directories and bypass traversal access checks.</span></span> <span data-ttu-id="a33d3-224">Эта привилегия включена по умолчанию для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="a33d3-224">This privilege is enabled by default for all users.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**вбемпривилежеремотешутдовн**</span><span class="sxs-lookup"><span data-stu-id="a33d3-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-226">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="a33d3-226">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-227">Константа C++: **SE \_ Remote \_ Shutdown \_ Name** строка: **серемотешутдовнпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-227">C++ constant: **SE\_REMOTE\_SHUTDOWN\_NAME** string: **SeRemoteShutdownPrivilege**</span></span>

<span data-ttu-id="a33d3-228">Короткое имя сценария: **ремотешутдовн**</span><span class="sxs-lookup"><span data-stu-id="a33d3-228">Scripting short name: **RemoteShutdown**</span></span>

<span data-ttu-id="a33d3-229">Требуется для завершения работы удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a33d3-229">Required to shut down a remote computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**вбемпривилежеундокк**</span><span class="sxs-lookup"><span data-stu-id="a33d3-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-231">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="a33d3-231">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-232">Константа C++: SE, строка **\_ \_ имени** : **сеундоккпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-232">C++ constant: **SE\_UNDOCK\_NAME** string: **SeUndockPrivilege**</span></span>

<span data-ttu-id="a33d3-233">Короткое имя сценария: отмена **закрепления**</span><span class="sxs-lookup"><span data-stu-id="a33d3-233">Scripting short name: **Undock**</span></span>

<span data-ttu-id="a33d3-234">Требуется для удаления ноутбука с стыковочного узла.</span><span class="sxs-lookup"><span data-stu-id="a33d3-234">Required to remove a laptop from a docking station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**вбемпривилежесинкажент**</span><span class="sxs-lookup"><span data-stu-id="a33d3-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-236">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="a33d3-236">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-237">Константа C++: **SE \_ Sync \_ Agent \_ Name** : **сесинкажентпривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-237">C++ constant: **SE\_SYNC\_AGENT\_NAME** string: **SeSyncAgentPrivilege**</span></span>

<span data-ttu-id="a33d3-238">Короткое имя сценария: **синкажент**</span><span class="sxs-lookup"><span data-stu-id="a33d3-238">Scripting short name: **SyncAgent**</span></span>

<span data-ttu-id="a33d3-239">Требуется для синхронизации данных службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="a33d3-239">Required to synchronize directory service data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**вбемпривилежеенабледелегатион**</span><span class="sxs-lookup"><span data-stu-id="a33d3-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-241">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="a33d3-241">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-242">Константа C++ **: \_ SE \_ включить \_ имя делегирования** : **SeEnableDelegationPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a33d3-242">C++ constant: **SE\_ENABLE\_DELEGATION\_NAME** string: **SeEnableDelegationPrivilege**</span></span>

<span data-ttu-id="a33d3-243">Короткое имя сценария: **енабледелегатион**</span><span class="sxs-lookup"><span data-stu-id="a33d3-243">Scripting short name: **EnableDelegation**</span></span>

<span data-ttu-id="a33d3-244">Требуется для включения доверия учетных записей компьютеров и пользователей для делегирования.</span><span class="sxs-lookup"><span data-stu-id="a33d3-244">Required to enable computer and user accounts to be trusted for delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a33d3-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**вбемпривилежеманажеволуме**</span><span class="sxs-lookup"><span data-stu-id="a33d3-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33d3-246">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="a33d3-246">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="a33d3-247">Константа C++ **: \_ SE \_ Управление \_ именем тома** : **семанажеволумепривилеже**</span><span class="sxs-lookup"><span data-stu-id="a33d3-247">C++ constant: **SE\_MANAGE\_VOLUME\_NAME** string: **SeManageVolumePrivilege**</span></span>

<span data-ttu-id="a33d3-248">Короткое имя сценария: **манажеволуме**</span><span class="sxs-lookup"><span data-stu-id="a33d3-248">Scripting short name: **ManageVolume**</span></span>

<span data-ttu-id="a33d3-249">Требуется для выполнения задач по обслуживанию томов.</span><span class="sxs-lookup"><span data-stu-id="a33d3-249">Required to perform volume maintenance tasks.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a33d3-250">Требования</span><span class="sxs-lookup"><span data-stu-id="a33d3-250">Requirements</span></span>



| <span data-ttu-id="a33d3-251">Требование</span><span class="sxs-lookup"><span data-stu-id="a33d3-251">Requirement</span></span> | <span data-ttu-id="a33d3-252">Значение</span><span class="sxs-lookup"><span data-stu-id="a33d3-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a33d3-253">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a33d3-253">Minimum supported client</span></span><br/> | <span data-ttu-id="a33d3-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a33d3-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a33d3-255">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a33d3-255">Minimum supported server</span></span><br/> | <span data-ttu-id="a33d3-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a33d3-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a33d3-257">Header</span><span class="sxs-lookup"><span data-stu-id="a33d3-257">Header</span></span><br/>                   | <dl> <span data-ttu-id="a33d3-258"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33d3-258"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a33d3-259">IDL</span><span class="sxs-lookup"><span data-stu-id="a33d3-259">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a33d3-260"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a33d3-260"><dt>Wbemdisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33d3-261">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a33d3-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33d3-262">Константы API скриптов</span><span class="sxs-lookup"><span data-stu-id="a33d3-262">Scripting API Constants</span></span>](scripting-api-constants.md)
</dt> <dt>

[<span data-ttu-id="a33d3-263">**свбемсекурити**</span><span class="sxs-lookup"><span data-stu-id="a33d3-263">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="a33d3-264">**вбемпривилежеенум**</span><span class="sxs-lookup"><span data-stu-id="a33d3-264">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="a33d3-265">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="a33d3-265">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="a33d3-266">Выполнение привилегированных операций с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="a33d3-266">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

