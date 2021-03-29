---
title: Метод Delete класса Win32_Service (службы удаленных рабочих столов)
description: Удаление \ 8194; Метод класса WMI удаляет существующую службу.
ms.assetid: 0F012D6B-BD29-4AC3-AC7E-78EC02C1FF43
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Delete
- Службы удаленных рабочих столов метода Delete, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод Delete
topic_type:
- apiref
api_name:
- Win32_Service.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89e2c30ef39d7b36baf62a486477fcf4a7fa2842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535309"
---
# <a name="delete-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="bff40-106">Метод Delete класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="bff40-106">Delete method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="bff40-107">Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удаляет существующую службу.</span><span class="sxs-lookup"><span data-stu-id="bff40-107">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="bff40-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="bff40-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bff40-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bff40-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bff40-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bff40-110">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="bff40-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bff40-111">Parameters</span></span>

<span data-ttu-id="bff40-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bff40-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bff40-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bff40-113">Return value</span></span>

<span data-ttu-id="bff40-114">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="bff40-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="bff40-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bff40-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bff40-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="bff40-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bff40-117">**0**</span><span class="sxs-lookup"><span data-stu-id="bff40-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-118">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="bff40-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-119">**1**</span><span class="sxs-lookup"><span data-stu-id="bff40-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-120">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bff40-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-121">**2**</span><span class="sxs-lookup"><span data-stu-id="bff40-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="bff40-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-123">**3**</span><span class="sxs-lookup"><span data-stu-id="bff40-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-124">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="bff40-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-125">**4**</span><span class="sxs-lookup"><span data-stu-id="bff40-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="bff40-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-127">**5**</span><span class="sxs-lookup"><span data-stu-id="bff40-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-128">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="bff40-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-129">**6**</span><span class="sxs-lookup"><span data-stu-id="bff40-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-130">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="bff40-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-131">**7**</span><span class="sxs-lookup"><span data-stu-id="bff40-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-132">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="bff40-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-133">**8**</span><span class="sxs-lookup"><span data-stu-id="bff40-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="bff40-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-135">**9**</span><span class="sxs-lookup"><span data-stu-id="bff40-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="bff40-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-137">**10**</span><span class="sxs-lookup"><span data-stu-id="bff40-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="bff40-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-139">**11**</span><span class="sxs-lookup"><span data-stu-id="bff40-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="bff40-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-141">**12**</span><span class="sxs-lookup"><span data-stu-id="bff40-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="bff40-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-143">**13**</span><span class="sxs-lookup"><span data-stu-id="bff40-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="bff40-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-145">**14**</span><span class="sxs-lookup"><span data-stu-id="bff40-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="bff40-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-147">**15**</span><span class="sxs-lookup"><span data-stu-id="bff40-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="bff40-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-149">**16**</span><span class="sxs-lookup"><span data-stu-id="bff40-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="bff40-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-151">**17**</span><span class="sxs-lookup"><span data-stu-id="bff40-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="bff40-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="bff40-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="bff40-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="bff40-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="bff40-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-157">**20**</span><span class="sxs-lookup"><span data-stu-id="bff40-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="bff40-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-159">**открыт**</span><span class="sxs-lookup"><span data-stu-id="bff40-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-160">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="bff40-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-161">**22**</span><span class="sxs-lookup"><span data-stu-id="bff40-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-162">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="bff40-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-163">**23**</span><span class="sxs-lookup"><span data-stu-id="bff40-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-164">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="bff40-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="bff40-165">**24**</span><span class="sxs-lookup"><span data-stu-id="bff40-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="bff40-166">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="bff40-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bff40-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bff40-167">Remarks</span></span>

<span data-ttu-id="bff40-168">По мере изменения организации может быть решено удалить определенные службы с определенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="bff40-168">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="bff40-169">Внутренние и сторонние службы можно удалить с помощью инструментария WMI, а службы операционной системы можно удалить с помощью Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="bff40-169">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="bff40-170">При подготовке к удалению служб учитывайте следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="bff40-170">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="bff40-171">Прежде чем удалять службы, их необходимо остановить.</span><span class="sxs-lookup"><span data-stu-id="bff40-171">Services must be stopped before you remove them.</span></span> <span data-ttu-id="bff40-172">Если служба выполняется при выполнении команды DELETE, она помечается для удаления, но будет продолжать выполняться до тех пор, пока она не будет остановлена и все открытые дескрипторы будут закрыты.</span><span class="sxs-lookup"><span data-stu-id="bff40-172">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="bff40-173">Если служба не остановлена, эта служба никогда не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="bff40-173">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="bff40-174">При удалении службы исполняемый файл службы не удаляется.</span><span class="sxs-lookup"><span data-stu-id="bff40-174">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="bff40-175">При удалении службы с помощью инструментария WMI удаляет связанные записи реестра в разделе HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services.</span><span class="sxs-lookup"><span data-stu-id="bff40-175">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="bff40-176">В результате служба больше не устанавливается и недоступна через оснастку "службы".</span><span class="sxs-lookup"><span data-stu-id="bff40-176">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="bff40-177">Однако Инструментарий WMI не удаляет исполняемый файл, что позволяет легко переустановить службу.</span><span class="sxs-lookup"><span data-stu-id="bff40-177">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="bff40-178">Чтобы удалить исполняемый файл, необходимо получить имя пути, а затем удалить файл.</span><span class="sxs-lookup"><span data-stu-id="bff40-178">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="bff40-179">Удаление базовой службы Windows 2000 (например, DHCP) с помощью инструментария WMI удаляет записи реестра для этой службы, но не удаляет ярлык из меню "Администрирование" или удаляет службу из мастера компонентов Windows.</span><span class="sxs-lookup"><span data-stu-id="bff40-179">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="bff40-180">Это может запутать всех, кто пытается определить, как настроен компьютер.</span><span class="sxs-lookup"><span data-stu-id="bff40-180">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="bff40-181">Например, если удалить службу DHCP с помощью скрипта WMI, служба DHCP больше не будет отображаться в оснастке "службы".</span><span class="sxs-lookup"><span data-stu-id="bff40-181">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="bff40-182">Однако нефункциональный ярлык консоли DHCP остается в меню "Администрирование", и при запуске мастера компонентов Windows это означает, что служба DHCP установлена.</span><span class="sxs-lookup"><span data-stu-id="bff40-182">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="bff40-183">Поэтому следует всегда использовать Sysocmgr.exe для программного удаления служб Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="bff40-183">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="bff40-184">Примеры</span><span class="sxs-lookup"><span data-stu-id="bff40-184">Examples</span></span>

<span data-ttu-id="bff40-185">В следующем примере кода VBScript описывается удаление службы.</span><span class="sxs-lookup"><span data-stu-id="bff40-185">The following VBScript code sample describes how to delete a service.</span></span>


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



<span data-ttu-id="bff40-186">В следующем образце кода Perl описывается, как удалить службу.</span><span class="sxs-lookup"><span data-stu-id="bff40-186">The following Perl code sample describes how to delete a service.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bff40-187">Требования</span><span class="sxs-lookup"><span data-stu-id="bff40-187">Requirements</span></span>



| <span data-ttu-id="bff40-188">Требование</span><span class="sxs-lookup"><span data-stu-id="bff40-188">Requirement</span></span> | <span data-ttu-id="bff40-189">Значение</span><span class="sxs-lookup"><span data-stu-id="bff40-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bff40-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bff40-190">Minimum supported client</span></span><br/> | <span data-ttu-id="bff40-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bff40-191">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bff40-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bff40-192">Minimum supported server</span></span><br/> | <span data-ttu-id="bff40-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bff40-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bff40-194">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bff40-194">Namespace</span></span><br/>                | <span data-ttu-id="bff40-195">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="bff40-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bff40-196">MOF</span><span class="sxs-lookup"><span data-stu-id="bff40-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bff40-197"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bff40-197"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bff40-198">DLL</span><span class="sxs-lookup"><span data-stu-id="bff40-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bff40-199"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bff40-199"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff40-200">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bff40-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff40-201">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="bff40-201">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="bff40-202">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="bff40-202">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="bff40-203">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="bff40-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="bff40-204">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="bff40-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

