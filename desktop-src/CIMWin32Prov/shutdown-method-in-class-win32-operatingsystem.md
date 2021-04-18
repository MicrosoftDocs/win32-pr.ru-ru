---
description: Завершение работы&\# 8194; Метод класса WMI выгружает программы и библиотеки DLL до отключения компьютера.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Метод Shutdown класса Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496728"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="1a074-103">Метод Shutdown \_ класса операционной системы Win32</span><span class="sxs-lookup"><span data-stu-id="1a074-103">Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="1a074-104">Метод класса **Shutdown** [инструментария WMI](/windows/desktop/WmiSdk/retrieving-a-class) выгружает программы и библиотеки DLL, пока не будет отключено отключение компьютера.</span><span class="sxs-lookup"><span data-stu-id="1a074-104">The **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method unloads programs and DLLs until it is safe to turn off the computer.</span></span>

<span data-ttu-id="1a074-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="1a074-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1a074-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1a074-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a074-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a074-107">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="1a074-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a074-108">Parameters</span></span>

<span data-ttu-id="1a074-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1a074-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a074-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a074-110">Return value</span></span>

<span data-ttu-id="1a074-111">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="1a074-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="1a074-112">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="1a074-112">Any other number indicates an error.</span></span> <span data-ttu-id="1a074-113">Коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1a074-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1a074-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1a074-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1a074-115">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="1a074-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1a074-116">**Другие** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="1a074-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1a074-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a074-117">Remarks</span></span>

<span data-ttu-id="1a074-118">Иногда требуется удалить компьютеры из сети, например для запланированного обслуживания, так как компьютер работает неправильно или не может завершить процесс настройки.</span><span class="sxs-lookup"><span data-stu-id="1a074-118">Computers occasionally need to be removed from the network, perhaps for scheduled maintenance, because the computer is not functioning correctly, or to complete a configuration process.</span></span> <span data-ttu-id="1a074-119">Например, если сервер DHCP передает ошибочные IP-адреса, может потребоваться завершить работу компьютера до тех пор, пока не будет подготовлен специалист по обслуживанию для решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="1a074-119">For example, if a DHCP server is handing out erroneous IP addresses, you might want to shut the computer down until a service technician can be dispatched to fix the problem.</span></span> <span data-ttu-id="1a074-120">Если вы подозреваете, что произошло нарушение безопасности, может потребоваться завершить работу некоторых серверов, чтобы убедиться в отсутствии доступа к ним, пока проблема безопасности не будет устранена.</span><span class="sxs-lookup"><span data-stu-id="1a074-120">If you suspect that a security breach has occurred, you might need to shut down certain servers to ensure that they cannot be accessed until the security issue has been resolved.</span></span> <span data-ttu-id="1a074-121">Некоторые операции настройки (например, изменение имени компьютера) потребовали перезагрузки компьютера, прежде чем изменение вступит в силу.</span><span class="sxs-lookup"><span data-stu-id="1a074-121">Some configuration operations (such as changing a computer name) require you to restart the computer before the change takes effect.</span></span>

<span data-ttu-id="1a074-122">Этот метод немедленно завершает работу компьютера, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="1a074-122">This method immediately shuts the computer down, if possible.</span></span> <span data-ttu-id="1a074-123">Система останавливает все запущенные процессы, сбрасывает все буферы файлов на диск, а затем выключает систему.</span><span class="sxs-lookup"><span data-stu-id="1a074-123">The system stops all running processes, flushes all file buffers to the disk, and then powers down the system.</span></span> <span data-ttu-id="1a074-124">Вызывающий процесс должен иметь привилегию **SE \_ Shutdown \_ Name** , как описано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1a074-124">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege, as described in the following example.</span></span>


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



<span data-ttu-id="1a074-125">Дополнительные сведения об установке привилегий см. в статьях [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations) и [выполнение привилегированных операций с помощью VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="1a074-125">For more information on setting a privilege, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations) and [Executing Privileged Operations Using VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span></span> <span data-ttu-id="1a074-126">Дополнительные параметры завершения работы, такие как выход из системы или принудительное завершение работы, см. в описании метода [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="1a074-126">For additional shutdown options, such as a logoff or a forced shutdown, see the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="1a074-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="1a074-127">Examples</span></span>

<span data-ttu-id="1a074-128">Следующий код VBScript закрывает локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="1a074-128">The following VBScript code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="1a074-129">Для успешного вызова метода Shutdown необходимо иметь права на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="1a074-129">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



<span data-ttu-id="1a074-130">Следующий код Perl закрывает локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="1a074-130">The following Perl code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="1a074-131">Для успешного вызова метода Shutdown необходимо иметь права на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="1a074-131">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
  if (!defined $RetVal || $RetVal != 0)
  { 
   print Win32::OLE->LastError, "\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="1a074-132">Следующий код VBScript закрывает указанный удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="1a074-132">The following VBScript code shuts the specified remote computer down.</span></span> <span data-ttu-id="1a074-133">В поле *\_ \_ имя удаленной системы* введите имя удаленной системы для завершения работы.</span><span class="sxs-lookup"><span data-stu-id="1a074-133">Fill in *REMOTE\_SYSTEM\_NAME* with the name of the remote system to shutdown.</span></span>

> [!Note]  
> <span data-ttu-id="1a074-134">Для успешного вызова метода **Shutdown** необходимо иметь привилегию ремотешутдовн.</span><span class="sxs-lookup"><span data-stu-id="1a074-134">You must have the RemoteShutdown privilege to successfully invoke the **Shutdown** method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a><span data-ttu-id="1a074-135">Требования</span><span class="sxs-lookup"><span data-stu-id="1a074-135">Requirements</span></span>



| <span data-ttu-id="1a074-136">Требование</span><span class="sxs-lookup"><span data-stu-id="1a074-136">Requirement</span></span> | <span data-ttu-id="1a074-137">Значение</span><span class="sxs-lookup"><span data-stu-id="1a074-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a074-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a074-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1a074-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a074-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a074-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a074-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1a074-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a074-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a074-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1a074-142">Namespace</span></span><br/>                | <span data-ttu-id="1a074-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1a074-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a074-144">MOF</span><span class="sxs-lookup"><span data-stu-id="1a074-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a074-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a074-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a074-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1a074-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a074-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a074-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a074-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a074-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a074-149">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a074-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1a074-150">**Win32, \_ Операционная система**</span><span class="sxs-lookup"><span data-stu-id="1a074-150">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="1a074-151">Задачи WMI: управление рабочим столом</span><span class="sxs-lookup"><span data-stu-id="1a074-151">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[<span data-ttu-id="1a074-152">Выполнение привилегированных операций с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="1a074-152">Executing Privileged Operations Using VBScript</span></span>](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

