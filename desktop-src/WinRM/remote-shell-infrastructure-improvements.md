---
title: Усовершенствования инфраструктуры удаленной оболочки
description: Служба удаленного управления Windows версии 2,0 (WinRM 2,0) предлагает несколько улучшений инфраструктуры удаленной оболочки.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c67752222f1ca969ea254164a25144168d1eb3
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "104069485"
---
# <a name="remote-shell-infrastructure-improvements"></a><span data-ttu-id="7682a-103">Усовершенствования инфраструктуры удаленной оболочки</span><span class="sxs-lookup"><span data-stu-id="7682a-103">Remote Shell Infrastructure Improvements</span></span>

<span data-ttu-id="7682a-104">Служба удаленного управления Windows версии 2,0 (WinRM 2,0) предлагает несколько улучшений инфраструктуры удаленной оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-104">Windows Remote Management version 2.0 (WinRM 2.0) offers many remote shell infrastructure improvements.</span></span> <span data-ttu-id="7682a-105">Эти улучшения подробно описаны в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7682a-105">The following topics describe these improvements in detail:</span></span>

-   [<span data-ttu-id="7682a-106">Поддержка нескольких прыжков</span><span class="sxs-lookup"><span data-stu-id="7682a-106">Multi-Hop Support</span></span>](multi-hop-support.md)
-   [<span data-ttu-id="7682a-107">Управление квотами для удаленных оболочек</span><span class="sxs-lookup"><span data-stu-id="7682a-107">Quota Management for Remote Shells</span></span>](quotas.md)

<span data-ttu-id="7682a-108">Одним из усовершенствований инфраструктуры удаленной оболочки WinRM является добавление более надежного диспетчера оболочки, в котором хранятся сведения о пользовательской оболочке.</span><span class="sxs-lookup"><span data-stu-id="7682a-108">One of the improvements to the WinRM remote shell infrastructure is the addition of a more robust shell manager that maintains user-specific shell information.</span></span> <span data-ttu-id="7682a-109">Пользователи WinRM могут создавать оболочки на удаленных компьютерах для выполнения команд или сценариев.</span><span class="sxs-lookup"><span data-stu-id="7682a-109">WinRM users can create shells on remote computers to run commands or scripts.</span></span> <span data-ttu-id="7682a-110">Кроме того, пользователи могут создавать несколько оболочек на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7682a-110">In addition, users can create multiple shells on a computer.</span></span> <span data-ttu-id="7682a-111">Пользователям и администраторам требуется возможность управлять оболочками.</span><span class="sxs-lookup"><span data-stu-id="7682a-111">Users and administrators both need the ability to manage shells.</span></span> <span data-ttu-id="7682a-112">Пользователи могут перечислять, получать и удалять созданные оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-112">Users can enumerate, get, and delete the shells that they have created.</span></span> <span data-ttu-id="7682a-113">Администраторы могут перечислять все активные оболочки и получать сведения о конкретных оболочках на локальном или удаленном узле.</span><span class="sxs-lookup"><span data-stu-id="7682a-113">Administrators can enumerate over all active shells and retrieve details about specific shells on a local or remote host.</span></span> <span data-ttu-id="7682a-114">Администраторы также могут удалять любые активные оболочки на локальном или удаленном узле.</span><span class="sxs-lookup"><span data-stu-id="7682a-114">Administrators can also delete any active shells on a local or remote host.</span></span>

<span data-ttu-id="7682a-115">Когда пользователь или администратор перечисляет активные оболочки, служба WinRM может вернуть следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="7682a-115">When a user or administrator enumerates the active shells, the following information can be returned by the WinRM service.</span></span>

<dl> <dt>

<span data-ttu-id="7682a-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>шеллид</span><span class="sxs-lookup"><span data-stu-id="7682a-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span></span>
</dt> <dd>

<span data-ttu-id="7682a-117">Задает уникальный идентификатор оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-117">Specifies the unique identifier for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Переменные среды</span><span class="sxs-lookup"><span data-stu-id="7682a-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Environment variables</span></span>
</dt> <dd>

<span data-ttu-id="7682a-119">Задает все переменные среды, заданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="7682a-119">Specifies any environment variables set by the user.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="7682a-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span></span>
</dt> <dd>

<span data-ttu-id="7682a-121">Указывает начальный каталог оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-121">Specifies the starting directory for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span><span class="sxs-lookup"><span data-stu-id="7682a-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span></span>
</dt> <dd>

<span data-ttu-id="7682a-123">Указывает универсальный код ресурса (URI) для операции оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-123">Specifies the resource URI for the shell operation.</span></span> <span data-ttu-id="7682a-124">URI ресурса можно использовать для получения конфигурации подключаемого модуля, относящейся к экземпляру оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-124">The resource URI can be used to retrieve plug-in configuration that is specific to the shell instance.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="7682a-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="7682a-126">Указывает максимальную продолжительность (в миллисекундах), в течение которой оболочка будет оставаться открытой без запроса.</span><span class="sxs-lookup"><span data-stu-id="7682a-126">Specifies the maximum duration, in milliseconds, that the shell will stay open without any request.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>инпутстреамс</span><span class="sxs-lookup"><span data-stu-id="7682a-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span></span>
</dt> <dd>

<span data-ttu-id="7682a-128">Задает входные потоки для оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-128">Specifies the input streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>аутпутстреамс</span><span class="sxs-lookup"><span data-stu-id="7682a-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span></span>
</dt> <dd>

<span data-ttu-id="7682a-130">Указывает выходные потоки для оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-130">Specifies the output streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Время создания оболочки</span><span class="sxs-lookup"><span data-stu-id="7682a-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell creation time</span></span>
</dt> <dd>

<span data-ttu-id="7682a-132">Указывает метку времени создания для оболочки.</span><span class="sxs-lookup"><span data-stu-id="7682a-132">Specifies the creation timestamp for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>идлетиме</span><span class="sxs-lookup"><span data-stu-id="7682a-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span></span>
</dt> <dd>

<span data-ttu-id="7682a-134">Указывает длительность бездействия оболочки в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="7682a-134">Specifies the duration, in milliseconds, that the shell has been idle.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span><span class="sxs-lookup"><span data-stu-id="7682a-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span></span>
</dt> <dd>

<span data-ttu-id="7682a-136">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="7682a-136">Specifies the user ID.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Имя узла или IP-адрес</span><span class="sxs-lookup"><span data-stu-id="7682a-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname or IP address</span></span>
</dt> <dd>

<span data-ttu-id="7682a-138">Указывает либо имя узла, либо IP-адрес компьютера, создавшего оболочку.</span><span class="sxs-lookup"><span data-stu-id="7682a-138">Specifies either the host name or IP address of the computer that created the shell.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Использование памяти оболочки</span><span class="sxs-lookup"><span data-stu-id="7682a-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell memory usage</span></span>
</dt> <dd>

<span data-ttu-id="7682a-140">Указывает объем памяти, используемый оболочкой.</span><span class="sxs-lookup"><span data-stu-id="7682a-140">Specifies the amount of memory that has been used by the shell.</span></span>

</dd> <dt>

<span data-ttu-id="7682a-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Число процессов</span><span class="sxs-lookup"><span data-stu-id="7682a-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Number of processes</span></span>
</dt> <dd>

<span data-ttu-id="7682a-142">Указывает количество процессов, созданных оболочкой.</span><span class="sxs-lookup"><span data-stu-id="7682a-142">Specifies the number of processes that have been created by the shell.</span></span>

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a><span data-ttu-id="7682a-143">Перечисление оболочки на локальном узле</span><span class="sxs-lookup"><span data-stu-id="7682a-143">Enumerating a Shell on a Local Host</span></span>

<span data-ttu-id="7682a-144">Следующая команда демонстрирует использование служебной программы WinRM для перечисления оболочек в клиенте WinRM: **WinRM Enumerate Shell**.</span><span class="sxs-lookup"><span data-stu-id="7682a-144">The following command demonstrates how to use the winrm utility to enumerate shells on a WinRM client: **winrm enumerate shell**.</span></span>

<span data-ttu-id="7682a-145">В следующем примере на основе текста отображаются выходные данные для перечисления оболочки:</span><span class="sxs-lookup"><span data-stu-id="7682a-145">The following text-based example displays the output for shell enumeration:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

<span data-ttu-id="7682a-146">Дополнительные сведения см. в справке в Интернете, выполнив следующую команду: **WinRM Enumerate-?**.</span><span class="sxs-lookup"><span data-stu-id="7682a-146">For more information, see the online help provided by running the following command: **winrm enumerate -?**.</span></span>

## <a name="retrieving-information-about-a-specific-shell"></a><span data-ttu-id="7682a-147">Получение сведений о конкретной оболочке</span><span class="sxs-lookup"><span data-stu-id="7682a-147">Retrieving Information About a Specific Shell</span></span>

<span data-ttu-id="7682a-148">Администратор или пользователь может также использовать идентификатор Шеллид для получения сведений о оболочке.</span><span class="sxs-lookup"><span data-stu-id="7682a-148">An administrator or user can also use the ShellId identifier to retrieve information about the shell.</span></span> <span data-ttu-id="7682a-149">Следующая команда демонстрирует использование служебной программы WinRM для получения сведений о конкретной оболочке: **WinRM Get Shell? Шеллид = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span><span class="sxs-lookup"><span data-stu-id="7682a-149">The following command demonstrates how to use the winrm utility to get information about a specific shell: **winrm get shell?ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span></span>

<span data-ttu-id="7682a-150">В следующем примере на основе текста отображаются выходные данные для сведений о оболочке:</span><span class="sxs-lookup"><span data-stu-id="7682a-150">The following text-based example displays the output for shell information:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

<span data-ttu-id="7682a-151">Дополнительные сведения см. в справке в Интернете, предоставляемой следующей командой: **WinRM Get-?**.</span><span class="sxs-lookup"><span data-stu-id="7682a-151">For more information, see the online help provided by the following command: **winrm get -?**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7682a-152">См. также</span><span class="sxs-lookup"><span data-stu-id="7682a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7682a-153">Поддержка нескольких прыжков</span><span class="sxs-lookup"><span data-stu-id="7682a-153">Multi-Hop Support</span></span>](multi-hop-support.md)
</dt> <dt>

[<span data-ttu-id="7682a-154">Управление квотами для удаленных оболочек</span><span class="sxs-lookup"><span data-stu-id="7682a-154">Quota Management for Remote Shells</span></span>](quotas.md)
</dt> <dt>

[<span data-ttu-id="7682a-155">Управляемый Справочник по командам PowerShell WS-Management</span><span class="sxs-lookup"><span data-stu-id="7682a-155">Managed Reference for WS-Management PowerShell Commands</span></span>](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




