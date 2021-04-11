---
description: Удаление&\# 8194; Метод класса WMI удаляет существующую службу.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Метод Delete класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d06301c3620e144d72c2d4c4f3d8bc90e642374a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262657"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="3af56-103">Метод Delete класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3af56-103">Delete method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3af56-104">Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удаляет существующую службу.</span><span class="sxs-lookup"><span data-stu-id="3af56-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="3af56-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="3af56-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3af56-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3af56-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3af56-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3af56-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="3af56-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3af56-108">Parameters</span></span>

<span data-ttu-id="3af56-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3af56-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3af56-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3af56-110">Return value</span></span>

<span data-ttu-id="3af56-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="3af56-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="3af56-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3af56-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3af56-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3af56-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3af56-114">**0**</span><span class="sxs-lookup"><span data-stu-id="3af56-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-115">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="3af56-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-116">**1**</span><span class="sxs-lookup"><span data-stu-id="3af56-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3af56-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-118">**2**</span><span class="sxs-lookup"><span data-stu-id="3af56-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-119">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="3af56-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-120">**3**</span><span class="sxs-lookup"><span data-stu-id="3af56-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-121">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="3af56-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-122">**4**</span><span class="sxs-lookup"><span data-stu-id="3af56-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-123">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="3af56-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-124">**5**</span><span class="sxs-lookup"><span data-stu-id="3af56-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-125">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="3af56-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-126">**6**</span><span class="sxs-lookup"><span data-stu-id="3af56-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-127">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="3af56-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-128">**7**</span><span class="sxs-lookup"><span data-stu-id="3af56-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-129">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="3af56-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-130">**8**</span><span class="sxs-lookup"><span data-stu-id="3af56-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-131">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="3af56-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-132">**9**</span><span class="sxs-lookup"><span data-stu-id="3af56-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-133">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="3af56-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-134">**10**</span><span class="sxs-lookup"><span data-stu-id="3af56-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-135">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="3af56-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-136">**11**</span><span class="sxs-lookup"><span data-stu-id="3af56-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-137">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="3af56-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-138">**12**</span><span class="sxs-lookup"><span data-stu-id="3af56-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-139">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="3af56-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-140">**13**</span><span class="sxs-lookup"><span data-stu-id="3af56-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-141">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="3af56-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-142">**14**</span><span class="sxs-lookup"><span data-stu-id="3af56-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-143">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="3af56-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-144">**15**</span><span class="sxs-lookup"><span data-stu-id="3af56-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-145">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="3af56-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-146">**16**</span><span class="sxs-lookup"><span data-stu-id="3af56-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-147">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="3af56-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-148">**17**</span><span class="sxs-lookup"><span data-stu-id="3af56-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-149">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="3af56-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-150">**стр**</span><span class="sxs-lookup"><span data-stu-id="3af56-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-151">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="3af56-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-152">**стр**</span><span class="sxs-lookup"><span data-stu-id="3af56-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-153">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="3af56-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-154">**20**</span><span class="sxs-lookup"><span data-stu-id="3af56-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-155">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="3af56-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-156">**открыт**</span><span class="sxs-lookup"><span data-stu-id="3af56-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-157">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="3af56-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-158">**22**</span><span class="sxs-lookup"><span data-stu-id="3af56-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-159">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="3af56-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-160">**23**</span><span class="sxs-lookup"><span data-stu-id="3af56-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-161">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="3af56-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3af56-162">**24**</span><span class="sxs-lookup"><span data-stu-id="3af56-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3af56-163">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="3af56-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3af56-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3af56-164">Remarks</span></span>

<span data-ttu-id="3af56-165">По мере изменения организации может быть решено удалить определенные службы с определенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="3af56-165">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="3af56-166">Внутренние и сторонние службы можно удалить с помощью инструментария WMI, а службы операционной системы можно удалить с помощью Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="3af56-166">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="3af56-167">При подготовке к удалению служб учитывайте следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="3af56-167">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="3af56-168">Прежде чем удалять службы, их необходимо остановить.</span><span class="sxs-lookup"><span data-stu-id="3af56-168">Services must be stopped before you remove them.</span></span> <span data-ttu-id="3af56-169">Если служба выполняется при выполнении команды DELETE, она помечается для удаления, но будет продолжать выполняться до тех пор, пока она не будет остановлена и все открытые дескрипторы будут закрыты.</span><span class="sxs-lookup"><span data-stu-id="3af56-169">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="3af56-170">Если служба не остановлена, эта служба никогда не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="3af56-170">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="3af56-171">При удалении службы исполняемый файл службы не удаляется.</span><span class="sxs-lookup"><span data-stu-id="3af56-171">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="3af56-172">При удалении службы с помощью инструментария WMI удаляет связанные записи реестра в разделе HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services.</span><span class="sxs-lookup"><span data-stu-id="3af56-172">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="3af56-173">В результате служба больше не устанавливается и недоступна через оснастку "службы".</span><span class="sxs-lookup"><span data-stu-id="3af56-173">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="3af56-174">Однако Инструментарий WMI не удаляет исполняемый файл, что позволяет легко переустановить службу.</span><span class="sxs-lookup"><span data-stu-id="3af56-174">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="3af56-175">Чтобы удалить исполняемый файл, необходимо получить имя пути, а затем удалить файл.</span><span class="sxs-lookup"><span data-stu-id="3af56-175">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="3af56-176">Удаление базовой службы Windows 2000 (например, DHCP) с помощью инструментария WMI удаляет записи реестра для этой службы, но не удаляет ярлык из меню "Администрирование" или удаляет службу из мастера компонентов Windows.</span><span class="sxs-lookup"><span data-stu-id="3af56-176">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="3af56-177">Это может запутать всех, кто пытается определить, как настроен компьютер.</span><span class="sxs-lookup"><span data-stu-id="3af56-177">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="3af56-178">Например, если удалить службу DHCP с помощью скрипта WMI, служба DHCP больше не будет отображаться в оснастке "службы".</span><span class="sxs-lookup"><span data-stu-id="3af56-178">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="3af56-179">Однако нефункциональный ярлык консоли DHCP остается в меню "Администрирование", и при запуске мастера компонентов Windows это означает, что служба DHCP установлена.</span><span class="sxs-lookup"><span data-stu-id="3af56-179">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="3af56-180">Поэтому следует всегда использовать Sysocmgr.exe для программного удаления служб Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3af56-180">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="3af56-181">Примеры</span><span class="sxs-lookup"><span data-stu-id="3af56-181">Examples</span></span>

<span data-ttu-id="3af56-182">В следующем примере кода VBScript описывается удаление службы.</span><span class="sxs-lookup"><span data-stu-id="3af56-182">The following VBScript code sample describes how to delete a service.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



<span data-ttu-id="3af56-183">В следующем образце кода Perl описывается, как удалить службу.</span><span class="sxs-lookup"><span data-stu-id="3af56-183">The following Perl code sample describes how to delete a service.</span></span>


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="3af56-184">Требования</span><span class="sxs-lookup"><span data-stu-id="3af56-184">Requirements</span></span>



| <span data-ttu-id="3af56-185">Требование</span><span class="sxs-lookup"><span data-stu-id="3af56-185">Requirement</span></span> | <span data-ttu-id="3af56-186">Значение</span><span class="sxs-lookup"><span data-stu-id="3af56-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3af56-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3af56-187">Minimum supported client</span></span><br/> | <span data-ttu-id="3af56-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3af56-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3af56-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3af56-189">Minimum supported server</span></span><br/> | <span data-ttu-id="3af56-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3af56-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3af56-191">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3af56-191">Namespace</span></span><br/>                | <span data-ttu-id="3af56-192">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3af56-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3af56-193">MOF</span><span class="sxs-lookup"><span data-stu-id="3af56-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3af56-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3af56-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3af56-195">DLL</span><span class="sxs-lookup"><span data-stu-id="3af56-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3af56-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3af56-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3af56-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3af56-197">See also</span></span>

<dl> <dt>

<span data-ttu-id="3af56-198">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3af56-198">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3af56-199">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="3af56-199">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="3af56-200">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="3af56-200">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

