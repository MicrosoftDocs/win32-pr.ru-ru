---
description: '\_Для выполнения сценария или приложения на удаленном компьютере можно использовать процесс Win32. Create. Однако в целях безопасности процесс не может быть интерактивным. Когда \_ на локальном компьютере вызывается Win32 Process. Create, процесс может быть интерактивным.'
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Удаленное создание процессов с помощью WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816688"
---
# <a name="creating-processes-remotely-using-wmi"></a>Удаленное создание процессов с помощью WMI

Для выполнения сценария или приложения на удаленном компьютере можно использовать [**\_ процесс Win32. Create.**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) Однако в целях безопасности процесс не может быть интерактивным. Когда на локальном компьютере вызывается **Win32 \_ Process. Create** , процесс может быть интерактивным.

> [!WARNING]
> В этом разделе описывается общая процедура создания удаленного процесса с помощью инструментария WMI. Если вы просто ищете запуск сценария в удаленной системе, см. раздел [Подключение к инструментарию WMI удаленно с помощью Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)или [Подключение к инструментарию WMI на удаленном компьютере с использованием Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Дополнительные общие сведения об удаленном взаимодействии с помощью PowerShell см. в разделе [выполнение удаленных команд](https://technet.microsoft.com/library/dd819505.aspx).

 

Удаленный процесс не имеет пользовательского интерфейса, но он указан в **диспетчере задач**. Процесс, созданный локально, может выполняться под любой учетной записью, если у учетной записи есть разрешение на **выполнение метода Execute** для корневого \\ пространства имен CIMV2. Процесс, созданный удаленно, может выполняться под любой учетной записью, если у учетной записи есть **метод Execute** и разрешения **Remote Enable** для root \\ CIMV2. Разрешения **EXECUTE** и **Remote Enable** устанавливаются в элементе управления WMI на панели управления. Дополнительные сведения см. [в разделе Настройка безопасности пространства имен с помощью элемента управления WMI](setting-namespace-security-with-the-wmi-control.md).

Для удаленного создания интерактивного процесса можно использовать [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) . Но процессы, запущенные с помощью **Win32 \_ ScheduledJob. Create** , выполняются под учетной записью LocalSystem, которая может послужить слишком большим уровнем привилегий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Подключение к третьим компьютерам — делегирование](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
