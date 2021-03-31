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
# <a name="creating-processes-remotely-using-wmi"></a><span data-ttu-id="c4fae-105">Удаленное создание процессов с помощью WMI</span><span class="sxs-lookup"><span data-stu-id="c4fae-105">Creating Processes Remotely using WMI</span></span>

<span data-ttu-id="c4fae-106">Для выполнения сценария или приложения на удаленном компьютере можно использовать [**\_ процесс Win32. Create.**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)</span><span class="sxs-lookup"><span data-stu-id="c4fae-106">You can use [**Win32\_Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) to execute a script or application on a remote computer.</span></span> <span data-ttu-id="c4fae-107">Однако в целях безопасности процесс не может быть интерактивным.</span><span class="sxs-lookup"><span data-stu-id="c4fae-107">However, for security reasons, the process cannot be interactive.</span></span> <span data-ttu-id="c4fae-108">Когда на локальном компьютере вызывается **Win32 \_ Process. Create** , процесс может быть интерактивным.</span><span class="sxs-lookup"><span data-stu-id="c4fae-108">When **Win32\_Process.Create** is called on the local computer, the process can be interactive.</span></span>

> [!WARNING]
> <span data-ttu-id="c4fae-109">В этом разделе описывается общая процедура создания удаленного процесса с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="c4fae-109">This topic describes the general procedure for creating a remote process with WMI.</span></span> <span data-ttu-id="c4fae-110">Если вы просто ищете запуск сценария в удаленной системе, см. раздел [Подключение к инструментарию WMI удаленно с помощью Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)или [Подключение к инструментарию WMI на удаленном компьютере с использованием Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c4fae-110">If you are simply looking to run a script on a remote system, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md), or [Connecting to WMI on a Remote Computer by Using Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span> <span data-ttu-id="c4fae-111">Дополнительные общие сведения об удаленном взаимодействии с помощью PowerShell см. в разделе [выполнение удаленных команд](https://technet.microsoft.com/library/dd819505.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4fae-111">For more general information on remoting with PowerShell, see [Running Remote Commands](https://technet.microsoft.com/library/dd819505.aspx).</span></span>

 

<span data-ttu-id="c4fae-112">Удаленный процесс не имеет пользовательского интерфейса, но он указан в **диспетчере задач**.</span><span class="sxs-lookup"><span data-stu-id="c4fae-112">The remote process has no user interface but it is listed in the **Task Manager**.</span></span> <span data-ttu-id="c4fae-113">Процесс, созданный локально, может выполняться под любой учетной записью, если у учетной записи есть разрешение на **выполнение метода Execute** для корневого \\ пространства имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="c4fae-113">A process created locally can run under any account if the account has the **Execute Method** permission for the root\\cimv2 namespace.</span></span> <span data-ttu-id="c4fae-114">Процесс, созданный удаленно, может выполняться под любой учетной записью, если у учетной записи есть **метод Execute** и разрешения **Remote Enable** для root \\ CIMV2.</span><span class="sxs-lookup"><span data-stu-id="c4fae-114">A process created remotely can run under any account if the account has the **Execute Method** and **Remote Enable** permissions for root\\cimv2.</span></span> <span data-ttu-id="c4fae-115">Разрешения **EXECUTE** и **Remote Enable** устанавливаются в элементе управления WMI на панели управления.</span><span class="sxs-lookup"><span data-stu-id="c4fae-115">The **Execute Method** and **Remote Enable** permissions are set in WMI Control in the Control Panel.</span></span> <span data-ttu-id="c4fae-116">Дополнительные сведения см. [в разделе Настройка безопасности пространства имен с помощью элемента управления WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="c4fae-116">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

<span data-ttu-id="c4fae-117">Для удаленного создания интерактивного процесса можно использовать [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) .</span><span class="sxs-lookup"><span data-stu-id="c4fae-117">You can use [**Win32\_ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) to create an interactive process remotely.</span></span> <span data-ttu-id="c4fae-118">Но процессы, запущенные с помощью **Win32 \_ ScheduledJob. Create** , выполняются под учетной записью LocalSystem, которая может послужить слишком большим уровнем привилегий.</span><span class="sxs-lookup"><span data-stu-id="c4fae-118">But processes started by **Win32\_ScheduledJob.Create** run under the LocalSystem account that can confer too much privilege.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4fae-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c4fae-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4fae-120">Защита удаленного WMI-подключения</span><span class="sxs-lookup"><span data-stu-id="c4fae-120">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="c4fae-121">Подключение к третьим компьютерам — делегирование</span><span class="sxs-lookup"><span data-stu-id="c4fae-121">Connecting to a 3rd Computer-Delegation</span></span>](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
