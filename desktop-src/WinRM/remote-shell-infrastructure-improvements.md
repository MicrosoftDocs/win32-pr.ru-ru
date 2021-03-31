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
# <a name="remote-shell-infrastructure-improvements"></a>Усовершенствования инфраструктуры удаленной оболочки

Служба удаленного управления Windows версии 2,0 (WinRM 2,0) предлагает несколько улучшений инфраструктуры удаленной оболочки. Эти улучшения подробно описаны в следующих разделах:

-   [Поддержка нескольких прыжков](multi-hop-support.md)
-   [Управление квотами для удаленных оболочек](quotas.md)

Одним из усовершенствований инфраструктуры удаленной оболочки WinRM является добавление более надежного диспетчера оболочки, в котором хранятся сведения о пользовательской оболочке. Пользователи WinRM могут создавать оболочки на удаленных компьютерах для выполнения команд или сценариев. Кроме того, пользователи могут создавать несколько оболочек на компьютере. Пользователям и администраторам требуется возможность управлять оболочками. Пользователи могут перечислять, получать и удалять созданные оболочки. Администраторы могут перечислять все активные оболочки и получать сведения о конкретных оболочках на локальном или удаленном узле. Администраторы также могут удалять любые активные оболочки на локальном или удаленном узле.

Когда пользователь или администратор перечисляет активные оболочки, служба WinRM может вернуть следующие сведения.

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>шеллид
</dt> <dd>

Задает уникальный идентификатор оболочки.

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Переменные среды
</dt> <dd>

Задает все переменные среды, заданные пользователем.

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory
</dt> <dd>

Указывает начальный каталог оболочки.

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI
</dt> <dd>

Указывает универсальный код ресурса (URI) для операции оболочки. URI ресурса можно использовать для получения конфигурации подключаемого модуля, относящейся к экземпляру оболочки.

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Указывает максимальную продолжительность (в миллисекундах), в течение которой оболочка будет оставаться открытой без запроса.

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>инпутстреамс
</dt> <dd>

Задает входные потоки для оболочки.

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>аутпутстреамс
</dt> <dd>

Указывает выходные потоки для оболочки.

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Время создания оболочки
</dt> <dd>

Указывает метку времени создания для оболочки.

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>идлетиме
</dt> <dd>

Указывает длительность бездействия оболочки в миллисекундах.

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId
</dt> <dd>

Указывает идентификатор пользователя.

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Имя узла или IP-адрес
</dt> <dd>

Указывает либо имя узла, либо IP-адрес компьютера, создавшего оболочку.

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Использование памяти оболочки
</dt> <dd>

Указывает объем памяти, используемый оболочкой.

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Число процессов
</dt> <dd>

Указывает количество процессов, созданных оболочкой.

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>Перечисление оболочки на локальном узле

Следующая команда демонстрирует использование служебной программы WinRM для перечисления оболочек в клиенте WinRM: **WinRM Enumerate Shell**.

В следующем примере на основе текста отображаются выходные данные для перечисления оболочки:

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

Дополнительные сведения см. в справке в Интернете, выполнив следующую команду: **WinRM Enumerate-?**.

## <a name="retrieving-information-about-a-specific-shell"></a>Получение сведений о конкретной оболочке

Администратор или пользователь может также использовать идентификатор Шеллид для получения сведений о оболочке. Следующая команда демонстрирует использование служебной программы WinRM для получения сведений о конкретной оболочке: **WinRM Get Shell? Шеллид = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.

В следующем примере на основе текста отображаются выходные данные для сведений о оболочке:

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

Дополнительные сведения см. в справке в Интернете, предоставляемой следующей командой: **WinRM Get-?**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поддержка нескольких прыжков](multi-hop-support.md)
</dt> <dt>

[Управление квотами для удаленных оболочек](quotas.md)
</dt> <dt>

[Управляемый Справочник по командам PowerShell WS-Management](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




