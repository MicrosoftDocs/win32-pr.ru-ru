---
title: Управление квотами для удаленных оболочек
description: Управление квотами позволяет пользователям более эффективно управлять системными ресурсами.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331760"
---
# <a name="quota-management-for-remote-shells"></a><span data-ttu-id="8d3e8-103">Управление квотами для удаленных оболочек</span><span class="sxs-lookup"><span data-stu-id="8d3e8-103">Quota Management for Remote Shells</span></span>

<span data-ttu-id="8d3e8-104">Управление квотами позволяет пользователям более эффективно управлять системными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-104">Quota management allows users to manage system resources more efficiently.</span></span> <span data-ttu-id="8d3e8-105">Служба удаленного управления Windows (WinRM) добавил Специальный набор квот, обеспечивающих более высокое качество обслуживания, помогает предотвратить проблемы отказа в обслуживании и выделить ресурсы сервера для параллельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-105">Windows Remote Management (WinRM) has added a specific set of quotas that provide a better quality of service, help prevent denial of service issues, and allocate server resources to concurrent users.</span></span> <span data-ttu-id="8d3e8-106">Набор квот WinRM основан на инфраструктуре квот, которая реализована для службы службы IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="8d3e8-106">The WinRM quota set is based on the quota infrastructure that is implemented for the Internet Information Services (IIS) service.</span></span>

<span data-ttu-id="8d3e8-107">Реализация квот поможет предотвратить проблемы снижения производительности и отказа в обслуживании, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-107">Implementing quotas will help to prevent performance degradation and denial of service issues by doing the following:</span></span>

-   <span data-ttu-id="8d3e8-108">Ограничение числа оболочек и процессов оболочки, которые может создать пользователь</span><span class="sxs-lookup"><span data-stu-id="8d3e8-108">Limiting the number of shells and shell processes that a user can create</span></span>
-   <span data-ttu-id="8d3e8-109">Ограничение максимального числа одновременных пользователей</span><span class="sxs-lookup"><span data-stu-id="8d3e8-109">Limiting the maximum number of concurrent users</span></span>
-   <span data-ttu-id="8d3e8-110">Управление объемом памяти, выделенной оболочке</span><span class="sxs-lookup"><span data-stu-id="8d3e8-110">Managing the amount of memory that is allocated to a shell</span></span>
-   <span data-ttu-id="8d3e8-111">Установка времени ожидания для оболочек, которые неактивны</span><span class="sxs-lookup"><span data-stu-id="8d3e8-111">Setting a time-out for shells that are inactive</span></span>

## <a name="quota-settings"></a><span data-ttu-id="8d3e8-112">Параметры квоты</span><span class="sxs-lookup"><span data-stu-id="8d3e8-112">Quota Settings</span></span>

<span data-ttu-id="8d3e8-113">Для управления удаленной оболочкой необходимо применять следующие квоты.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-113">The following quotas need to be enforced for remote shell management.</span></span> <span data-ttu-id="8d3e8-114">Эти квоты можно настроить с помощью служебной программы WinRM или с помощью параметров групповая политика.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-114">These quotas can be configured through the winrm utility or through Group Policy settings.</span></span> <span data-ttu-id="8d3e8-115">Параметры, настроенные групповая политика, заменяют квоты, заданные программой WinRM.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-115">Settings configured by a Group Policy supersede the quotas set by the winrm utility.</span></span> <span data-ttu-id="8d3e8-116">Дополнительные сведения о настройке групповых политик для WinRM см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="8d3e8-116">For more information about setting Group Policies for WinRM, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<dl> <dt>

<span data-ttu-id="8d3e8-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="8d3e8-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="8d3e8-118">Максимальное время в миллисекундах до удаления неактивной удаленной оболочки.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-118">The maximum time in milliseconds before an inactive remote shell is deleted.</span></span> <span data-ttu-id="8d3e8-119">Значение по умолчанию — 180000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-119">The default is 180000 milliseconds.</span></span> <span data-ttu-id="8d3e8-120">Минимальное время равно 1000 миллисекундам.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-120">The minimum time is 1000 milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="8d3e8-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>макспроцессеспершелл</span><span class="sxs-lookup"><span data-stu-id="8d3e8-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span></span>
</dt> <dd>

<span data-ttu-id="8d3e8-122">Максимальное количество процессов, разрешенных на оболочку, включая дочерние процессы оболочки.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-122">The maximum number of processes allowed per shell, including the shell's child processes.</span></span> <span data-ttu-id="8d3e8-123">Значение по умолчанию — 25.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-123">The default is 25.</span></span>

</dd> <dt>

<span data-ttu-id="8d3e8-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>максмеморипершеллмб</span><span class="sxs-lookup"><span data-stu-id="8d3e8-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span></span>
</dt> <dd>

<span data-ttu-id="8d3e8-125">Максимальный объем памяти, выделяемой на оболочку, включая дочерние процессы оболочки.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-125">The maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="8d3e8-126">Значение по умолчанию — 1024 МБ.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-126">The default is 1024 MB.</span></span>

> [!Note]  
> <span data-ttu-id="8d3e8-127">Поведение не поддерживается, если для Максмеморипершеллмб задано значение, которое меньше значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-127">The behavior is unsupported if the MaxMemoryPerShellMB is set to a value that is less than the default.</span></span>

 

</dd> <dt>

<span data-ttu-id="8d3e8-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>максшеллсперусер</span><span class="sxs-lookup"><span data-stu-id="8d3e8-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span></span>
</dt> <dd>

<span data-ttu-id="8d3e8-129">Максимальное количество оболочек на пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-129">The maximum number of shells per user.</span></span> <span data-ttu-id="8d3e8-130">Значение по умолчанию равно 30.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-130">The default is 30.</span></span>

</dd> <dt>

<span data-ttu-id="8d3e8-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>максконкуррентусерс</span><span class="sxs-lookup"><span data-stu-id="8d3e8-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span></span>
</dt> <dd>

<span data-ttu-id="8d3e8-132">Максимальное число одновременных пользователей, которые могут открывать оболочки.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-132">The maximum number of concurrent users who can open shells.</span></span> <span data-ttu-id="8d3e8-133">Значение по умолчанию равно 10.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-133">The default is 10.</span></span>

</dd> </dl>

## <a name="deprecated-quotas"></a><span data-ttu-id="8d3e8-134">Устаревшие квоты</span><span class="sxs-lookup"><span data-stu-id="8d3e8-134">Deprecated Quotas</span></span>

<span data-ttu-id="8d3e8-135">WinRM 2,0 устанавливает квоту Максшеллрунтиме на доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-135">WinRM 2.0 sets the MaxShellRunTime quota to read-only.</span></span> <span data-ttu-id="8d3e8-136">Изменение значения этой квоты не будет действовать на удаленных оболочках.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-136">Changing the value for this quota will have no effect on the remote shells.</span></span>

## <a name="retrieving-quota-configuration-information"></a><span data-ttu-id="8d3e8-137">Получение сведений о конфигурации квоты</span><span class="sxs-lookup"><span data-stu-id="8d3e8-137">Retrieving Quota Configuration Information</span></span>

<span data-ttu-id="8d3e8-138">Чтобы проверить параметры конфигурации квоты, введите **WinRM Get WinRM/config**.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-138">To check the quota configuration settings, type **winrm get winrm/config**.</span></span>

<span data-ttu-id="8d3e8-139">Следующий фрагмент кода представляет собой текстовый пример конфигурации WinRM с параметрами квоты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-139">The following snippet is a text-based example of a WinRM configuration with the default quota settings.</span></span>

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a><span data-ttu-id="8d3e8-140">Настройка квот оболочки</span><span class="sxs-lookup"><span data-stu-id="8d3e8-140">Configuring Shell Quotas</span></span>

<span data-ttu-id="8d3e8-141">Квоты можно задать с помощью параметра групповая политика или вручную.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-141">Quotas can be set through a Group Policy setting or manually.</span></span> <span data-ttu-id="8d3e8-142">Дополнительные сведения о конкретных параметрах конфигурации см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="8d3e8-142">For more information about specific configuration settings, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="8d3e8-143">**Установка квоты с групповая политика**</span><span class="sxs-lookup"><span data-stu-id="8d3e8-143">**To set a quota with Group Policy**</span></span>

1.  <span data-ttu-id="8d3e8-144">Откройте окно командной строки с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-144">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="8d3e8-145">В командной строке введите **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-145">At the Command Prompt, type **gpedit.msc**.</span></span> <span data-ttu-id="8d3e8-146">Откроется окно **Редактор объектов групповой политики** .</span><span class="sxs-lookup"><span data-stu-id="8d3e8-146">The **Group Policy Object Editor** window opens.</span></span>
3.  <span data-ttu-id="8d3e8-147">Найдите **Служба удаленного управления Windows** и **удаленная оболочка Windows** групповая политика объектов (GPO) в разделе **Конфигурация компьютера \\ Административные шаблоны \\ компоненты Windows**.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-147">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4.  <span data-ttu-id="8d3e8-148">На вкладке **Расширенная** выберите параметр, чтобы просмотреть описание.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-148">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="8d3e8-149">Дважды щелкните параметр, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-149">Double click a setting to edit it.</span></span>

<span data-ttu-id="8d3e8-150">**Задание квоты вручную**</span><span class="sxs-lookup"><span data-stu-id="8d3e8-150">**To set a quota manually**</span></span>

1.  <span data-ttu-id="8d3e8-151">Откройте окно командной строки с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-151">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="8d3e8-152">В командной строке введите **WinRM set winrm/config/WinRS ' @ { ***<Quota>*** = " ***<Value>*** "} "**</span><span class="sxs-lookup"><span data-stu-id="8d3e8-152">At the Command Prompt, type **winrm set winrm/config/winrs '@{***<Quota>***="***<Value>***"}'**</span></span>

<span data-ttu-id="8d3e8-153">Например, чтобы увеличить максимальное число оболочек на пользователя с 5 до 7, введите **WinRM set winrm/config/WinRS ' @ {максшеллсперусер = "7 '} '**.</span><span class="sxs-lookup"><span data-stu-id="8d3e8-153">For example, to increase the maximum number of shells per user from 5 to 7, type **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'**.</span></span>

 

 




