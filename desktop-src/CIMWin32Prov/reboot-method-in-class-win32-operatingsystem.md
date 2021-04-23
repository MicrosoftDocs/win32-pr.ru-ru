---
description: Перезагрузка&\# 8194; Метод класса WMI завершает работу системы компьютера, а затем перезапускает ее.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Метод reboot класса Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990714"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="2bb9c-103">Метод reboot \_ класса Win32 операционной системы</span><span class="sxs-lookup"><span data-stu-id="2bb9c-103">Reboot method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="2bb9c-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) reboot закрывает компьютерную систему, а затем перезапускает его.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-104">The **Reboot** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method shuts down the computer system, then restarts it.</span></span>

<span data-ttu-id="2bb9c-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="2bb9c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2bb9c-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2bb9c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb9c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bb9c-107">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="2bb9c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bb9c-108">Parameters</span></span>

<span data-ttu-id="2bb9c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bb9c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bb9c-110">Return value</span></span>

<span data-ttu-id="2bb9c-111">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="2bb9c-112">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-112">Any other number indicates an error.</span></span> <span data-ttu-id="2bb9c-113">Коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2bb9c-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2bb9c-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2bb9c-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2bb9c-115">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="2bb9c-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2bb9c-116">**Другие** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="2bb9c-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2bb9c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bb9c-117">Remarks</span></span>

<span data-ttu-id="2bb9c-118">Возможность программной перезагрузки компьютера позволяет администраторам удаленно выполнять многие задачи управления компьютером.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-118">The ability to programmatically restart a computer allows administrators to perform many computer management tasks remotely.</span></span>

<span data-ttu-id="2bb9c-119">Например, при создании сценария для установки программного обеспечения или при изменении конфигурации, требующей перезагрузки компьютера, можно включить в сценарий команду перезапуска и выполнить всю операцию удаленно.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-119">For example, if you create a script to install software or make a configuration change that requires restarting a computer, you can include the restart command in the script and perform the entire operation remotely.</span></span> <span data-ttu-id="2bb9c-120">Метод **reboot** можно использовать для перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-120">The **Reboot** method can be used to restart a computer.</span></span> <span data-ttu-id="2bb9c-121">Как и метод [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , методу **reboot** требуется пользователь, чьи учетные данные безопасности используются сценарием для предоставления прав на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-121">Like the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method, the **Reboot** method requires the user whose security credentials are being used by the script to possess the Shutdown privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="2bb9c-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="2bb9c-122">Examples</span></span>

<span data-ttu-id="2bb9c-123">В следующем примере кода VBScript вызывается метод reboot класса операционной системы [**Win32 \_**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="2bb9c-123">The following VBScript code sample invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="2bb9c-124">Для успешного вызова метода Shutdown необходимо иметь права на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-124">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="2bb9c-125">Следующий код Perl вызывает метод reboot класса [**Win32 \_ операционной**](win32-operatingsystem.md) системы.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-125">The following Perl code invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="2bb9c-126">Для успешного вызова метода Shutdown необходимо иметь права на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-126">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
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



<span data-ttu-id="2bb9c-127">Следующий сценарий VBScript вызывает метод reboot класса [**Win32 \_ операционной**](win32-operatingsystem.md) системы в удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-127">The following VBScript invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="2bb9c-128">В поле \_ имя удаленной системы введите \_ имя удаленной системы для перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-128">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="2bb9c-129">Для успешного вызова метода reboot необходимо иметь привилегию Ремотешутдовн</span><span class="sxs-lookup"><span data-stu-id="2bb9c-129">You must have the RemoteShutdown privilege to successfully invoke the Reboot method</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="2bb9c-130">Следующий вызов Perl вызывает метод перезагрузки класса операционной системы [**Win32 \_**](win32-operatingsystem.md) в удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-130">he following Perl invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="2bb9c-131">В поле \_ имя удаленной системы введите \_ имя удаленной системы для перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-131">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="2bb9c-132">Для успешного вызова метода reboot необходимо иметь привилегию Ремотешутдовн.</span><span class="sxs-lookup"><span data-stu-id="2bb9c-132">You must have the RemoteShutdown privilege to successfully invoke the Reboot method.</span></span>

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a><span data-ttu-id="2bb9c-133">Требования</span><span class="sxs-lookup"><span data-stu-id="2bb9c-133">Requirements</span></span>



| <span data-ttu-id="2bb9c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="2bb9c-134">Requirement</span></span> | <span data-ttu-id="2bb9c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="2bb9c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb9c-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bb9c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb9c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bb9c-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2bb9c-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bb9c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb9c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bb9c-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2bb9c-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2bb9c-140">Namespace</span></span><br/>                | <span data-ttu-id="2bb9c-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2bb9c-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2bb9c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2bb9c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bb9c-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bb9c-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bb9c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2bb9c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bb9c-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bb9c-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bb9c-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bb9c-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="2bb9c-147">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bb9c-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2bb9c-148">**Win32, \_ Операционная система**</span><span class="sxs-lookup"><span data-stu-id="2bb9c-148">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="2bb9c-149">**\_Метод операционной системы для CIM. Shutdown**</span><span class="sxs-lookup"><span data-stu-id="2bb9c-149">**CIM\_OperatingSystem.Shutdown method**</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="2bb9c-150">Задачи WMI: управление рабочим столом</span><span class="sxs-lookup"><span data-stu-id="2bb9c-150">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

