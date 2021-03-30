---
description: Win32Shutdown &\# 8194; Метод класса WMI предоставляет полный набор параметров завершения работы, поддерживаемых операционными системами Win32. К ним относятся выход, завершение работы, перезагрузка и принудительный выход, завершение работы или перезагрузка.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Метод Win32Shutdown класса Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896338"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="310a3-104">Метод Win32Shutdown \_ класса операционной системы Win32</span><span class="sxs-lookup"><span data-stu-id="310a3-104">Win32Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="310a3-105">Метод    [класса WMI](../wmisdk/retrieving-a-class.md) Win32Shutdown предоставляет полный набор параметров завершения работы, поддерживаемых операционными системами Win32.</span><span class="sxs-lookup"><span data-stu-id="310a3-105">The **Win32Shutdown**   [WMI class](../wmisdk/retrieving-a-class.md) method provides the full set of shutdown options supported by Win32 operating systems.</span></span> <span data-ttu-id="310a3-106">К ним относятся выход, завершение работы, перезагрузка и принудительный выход, завершение работы или перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="310a3-106">These include logoff, shutdown, reboot, and forcing a logoff, shutdown, or reboot.</span></span>

<span data-ttu-id="310a3-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="310a3-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="310a3-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](../wmisdk/calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="310a3-108">For more information about using this method, see [Calling a Method](../wmisdk/calling-a-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="310a3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="310a3-109">Syntax</span></span>


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a><span data-ttu-id="310a3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="310a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="310a3-111">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="310a3-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="310a3-112">Набор флагов битовой панели для выключения компьютера.</span><span class="sxs-lookup"><span data-stu-id="310a3-112">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="310a3-113">Чтобы принудительно выполнить команду, добавьте к значению команды флаг force (4).</span><span class="sxs-lookup"><span data-stu-id="310a3-113">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="310a3-114">Использование Force в сочетании с завершением работы или перезагрузкой на удаленном компьютере немедленно завершает все (включая WMI, COM и т. д.) или перезагружает удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="310a3-114">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="310a3-115">Это приводит к неопределенному возвращаемому значению.</span><span class="sxs-lookup"><span data-stu-id="310a3-115">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="310a3-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="310a3-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="310a3-117">Выход **из** системы — записывает пользователя на компьютер.</span><span class="sxs-lookup"><span data-stu-id="310a3-117">**Log Off** - Logs the user off the computer.</span></span> <span data-ttu-id="310a3-118">При выходе из системы останавливаются все процессы, связанные с контекстом безопасности процесса, который вызвал функцию Exit, записывает текущего пользователя в систему и отображает диалоговое окно входа.</span><span class="sxs-lookup"><span data-stu-id="310a3-118">Logging off stops all processes associated with the security context of the process that called the exit function, logs the current user off the system, and displays the logon dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="310a3-119">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="310a3-119">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="310a3-120">**Принудительный выход из системы (0 + 4)** . записывает пользователя на компьютер немедленно и не уведомляет приложения о завершении сеанса входа.</span><span class="sxs-lookup"><span data-stu-id="310a3-120">**Forced Log Off (0 + 4)** - Logs the user off the computer immediately and does not notify applications that the logon session is ending.</span></span> <span data-ttu-id="310a3-121">Это может привести к утрате данных.</span><span class="sxs-lookup"><span data-stu-id="310a3-121">This can result in a loss of data.</span></span>

</dd> <dt>

<span data-ttu-id="310a3-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="310a3-122">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="310a3-123">**Shutdown** — завершает работу компьютера до точки, в которой можно отключить питание.</span><span class="sxs-lookup"><span data-stu-id="310a3-123">**Shutdown** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="310a3-124">(Все буферы файлов записываются на диск, а все запущенные процессы останавливаются.) Пользователи видят сообщение, `It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="310a3-124">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message, `It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="310a3-125">Во время завершения работы система отправляет сообщение каждому работающему приложению.</span><span class="sxs-lookup"><span data-stu-id="310a3-125">During shutdown the system sends a message to each running application.</span></span> <span data-ttu-id="310a3-126">Приложения выполняют очистку при обработке сообщения и возвращают значение true, чтобы указать, что они могут быть завершены.</span><span class="sxs-lookup"><span data-stu-id="310a3-126">The applications perform any cleanup while processing the message and return True to indicate that they can be terminated.</span></span>

</dd> <dt>

<span data-ttu-id="310a3-127">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="310a3-127">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="310a3-128">**Принудительное завершение работы (1 + 4)** . завершает работу компьютера до точки, в которой можно отключить питание.</span><span class="sxs-lookup"><span data-stu-id="310a3-128">**Forced Shutdown (1 + 4)** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="310a3-129">(Все буферы файлов записываются на диск, а все запущенные процессы останавливаются.) Пользователи видят сообщение,` It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="310a3-129">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message,` It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="310a3-130">Когда используется подход принудительного завершения работы, все службы, включая WMI, немедленно завершают работу.</span><span class="sxs-lookup"><span data-stu-id="310a3-130">When the forced shutdown approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="310a3-131">По этой причине вы не сможете получить возвращаемое значение, если сценарий выполняется на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="310a3-131">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="310a3-132">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="310a3-132">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="310a3-133">**Перезагрузка** — завершает работу и перезагружает компьютер.</span><span class="sxs-lookup"><span data-stu-id="310a3-133">**Reboot** - Shuts down and then restarts the computer.</span></span>

</dd> <dt>

<span data-ttu-id="310a3-134">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="310a3-134">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="310a3-135">**Принудительная перезагрузка (2 + 4)** — завершает работу и перезагружает компьютер.</span><span class="sxs-lookup"><span data-stu-id="310a3-135">**Forced Reboot (2 + 4)** - Shuts down and then restarts the computer.</span></span>

<span data-ttu-id="310a3-136">При использовании принудительной перезагрузки все службы, включая WMI, немедленно завершают работу.</span><span class="sxs-lookup"><span data-stu-id="310a3-136">When the forced reboot approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="310a3-137">По этой причине вы не сможете получить возвращаемое значение, если сценарий выполняется на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="310a3-137">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="310a3-138">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="310a3-138">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="310a3-139">**Питание отключено** — завершает работу компьютера и выключает питание (если поддерживается компьютером).</span><span class="sxs-lookup"><span data-stu-id="310a3-139">**Power Off** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

</dd> <dt>

<span data-ttu-id="310a3-140">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="310a3-140">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="310a3-141">**Принудительное выключение (8 + 4)** — завершает работу компьютера и выключает питание (если это поддерживается компьютером).</span><span class="sxs-lookup"><span data-stu-id="310a3-141">**Forced Power Off (8 + 4)** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

<span data-ttu-id="310a3-142">При использовании подхода принудительного выключения питания все службы, включая WMI, немедленно завершают работу.</span><span class="sxs-lookup"><span data-stu-id="310a3-142">When the forced power off approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="310a3-143">По этой причине вы не сможете получить возвращаемое значение, если сценарий выполняется на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="310a3-143">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="310a3-144">*Зарезервировано* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="310a3-144">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="310a3-145">Средства для расширения **Win32Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="310a3-145">A means to extend **Win32Shutdown**.</span></span> <span data-ttu-id="310a3-146">В настоящее время *зарезервированный* параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="310a3-146">Currently, the *Reserved* parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="310a3-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="310a3-147">Return value</span></span>

<span data-ttu-id="310a3-148">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="310a3-148">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="310a3-149">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="310a3-149">Any other number indicates an error.</span></span> <span data-ttu-id="310a3-150">Коды ошибок см. в разделе [**константы WMI Error**](../wmisdk/wmi-error-constants.md) или [**вбемерроренум**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="310a3-150">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="310a3-151">Общие значения **HRESULT** см. в разделе [коды системных ошибок](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="310a3-151">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="310a3-152">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="310a3-152">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="310a3-153">**Другое** (1 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="310a3-153">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="310a3-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="310a3-154">Remarks</span></span>

<span data-ttu-id="310a3-155">Для более эффективного управления компьютерами в организации администраторам требуется возможность удаленного выключения или перезагрузки компьютера или удаленного выхода пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="310a3-155">For more efficient management of computers in an organization, administrators need the ability to remotely shut down or restart a computer, or to remotely log off a user.</span></span> <span data-ttu-id="310a3-156">Возможность выполнения этих задач позволяет администраторам устанавливать программное обеспечение, перенастраивать параметры компьютера, удалять компьютеры из сети и выполнять другие задачи без ручного выключения или перезапуска каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="310a3-156">The ability to carry out these tasks allows administrators to install software, reconfigure computer settings, remove computers from the network, and perform other tasks without having to manually shut down or restart each computer.</span></span>

<span data-ttu-id="310a3-157">Например, чтобы выполнить обновление сети, может потребоваться завершить работу всех компьютеров, работающих в определенном сегменте сети.</span><span class="sxs-lookup"><span data-stu-id="310a3-157">For example, to perform a network upgrade, you might need to shut down all the computers running on a particular network segment.</span></span> <span data-ttu-id="310a3-158">Чтобы принудительно обновить групповая политика, необходимо войти в систему пользователей с компьютеров.</span><span class="sxs-lookup"><span data-stu-id="310a3-158">To force a Group Policy upgrade, you need to log users off their computers.</span></span> <span data-ttu-id="310a3-159">Если компьютер находится в любом месте Организации, может потребоваться завершить работу максимально возможного количества компьютеров, прежде чем этот вирус сможет распространяться.</span><span class="sxs-lookup"><span data-stu-id="310a3-159">If a computer virus is present anywhere in your organization, you might want to shut down as many computers as possible, before the virus has an opportunity to spread.</span></span> <span data-ttu-id="310a3-160">Возможность выключения и перезагрузки компьютеров, а также программного выхода пользователей, а не вручную, может быть огромным временем.</span><span class="sxs-lookup"><span data-stu-id="310a3-160">The ability to shut down and restart computers and to log off users programmatically instead of manually can be an enormous time-saver.</span></span>

<span data-ttu-id="310a3-161">Вызывающий процесс должен иметь привилегию **SE \_ Shutdown \_ Name** .</span><span class="sxs-lookup"><span data-stu-id="310a3-161">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

<span data-ttu-id="310a3-162">Метод [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) предоставляет тот же набор параметров завершения работы, который поддерживает метод **Win32Shutdown** в [**Win32, \_**](win32-operatingsystem.md) но он также позволяет указывать комментарии, причину завершения работы или время ожидания.</span><span class="sxs-lookup"><span data-stu-id="310a3-162">The [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) method provides the same set of shutdown options supported by the **Win32Shutdown** method in [**Win32\_OperatingSystem**](win32-operatingsystem.md) but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

<span data-ttu-id="310a3-163">Метод Win32Shutdown не имеет параметра для блокировки рабочей станции, при этом пользователь вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="310a3-163">The Win32Shutdown method does not have a parameter for locking a workstation, leaving the user logged on.</span></span> <span data-ttu-id="310a3-164">Тем не менее рабочие станции можно заблокировать из командной строки с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="310a3-164">However, workstations can be locked from the command line by using the following command:</span></span>

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a><span data-ttu-id="310a3-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="310a3-165">Examples</span></span>

<span data-ttu-id="310a3-166">Пример " [выход, перезагрузка" или "завершение работы нескольких компьютеров](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) " в коллекции TechNet использует Win32Shutdown для выхода, выключения, перезагрузки или выключения питания (в зависимости от выбранных параметров) компьютеров, перечисленных в массиве серверов.</span><span class="sxs-lookup"><span data-stu-id="310a3-166">The [Log Out, Reboot, or Shut Down Multiple Computers](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript sample on TechNet Gallery uses Win32Shutdown to log off, shut down, reboot, or power off (depending on the selection) the computers listed in the Server array.</span></span>

<span data-ttu-id="310a3-167">Пример [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell в коллекции TechNet содержит метод, который вызывает Win32Shutdown на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="310a3-167">The [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sample on TechNet Gallery includes a method that calls Win32Shutdown on a remote computer.</span></span>

<span data-ttu-id="310a3-168">В следующем примере PowerShell используется метод Win32Shutdown для завершения работы указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="310a3-168">The following PowerShell example uses the Win32Shutdown method to shut down the specified computer.</span></span>


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



<span data-ttu-id="310a3-169">Следующий пример кода PowerShell использует Енаблеаллпривилежес из командлета Get-WmiObject для достижения нужных полномочий.</span><span class="sxs-lookup"><span data-stu-id="310a3-169">The following PowerShell code sample uses the EnableAllPrivileges from get-wmiobject cmdlet to achieve the proper priviliges.</span></span>


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



<span data-ttu-id="310a3-170">В следующем примере кода VB.NET используется метод Shutdown для перезагрузки или выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="310a3-170">The following VB.NET sample code uses the Shutdown method to reboot or log off a system.</span></span>


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a><span data-ttu-id="310a3-171">Требования</span><span class="sxs-lookup"><span data-stu-id="310a3-171">Requirements</span></span>



| <span data-ttu-id="310a3-172">Требование</span><span class="sxs-lookup"><span data-stu-id="310a3-172">Requirement</span></span> | <span data-ttu-id="310a3-173">Значение</span><span class="sxs-lookup"><span data-stu-id="310a3-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="310a3-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="310a3-174">Minimum supported client</span></span><br/> | <span data-ttu-id="310a3-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="310a3-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="310a3-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="310a3-176">Minimum supported server</span></span><br/> | <span data-ttu-id="310a3-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="310a3-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="310a3-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="310a3-178">Namespace</span></span><br/>                | <span data-ttu-id="310a3-179">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="310a3-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="310a3-180">MOF</span><span class="sxs-lookup"><span data-stu-id="310a3-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="310a3-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="310a3-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="310a3-182">DLL</span><span class="sxs-lookup"><span data-stu-id="310a3-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="310a3-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="310a3-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="310a3-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="310a3-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="310a3-185">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="310a3-185">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="310a3-186">**Win32, \_ Операционная система**</span><span class="sxs-lookup"><span data-stu-id="310a3-186">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="310a3-187">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="310a3-187">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="310a3-188">Задачи WMI: управление рабочим столом</span><span class="sxs-lookup"><span data-stu-id="310a3-188">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[<span data-ttu-id="310a3-189">Выполнение привилегированных операций с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="310a3-189">Executing Privileged Operations Using VBScript</span></span>](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
