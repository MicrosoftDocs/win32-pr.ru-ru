---
description: Пытается перевести указанную службу в состояние запуска.
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Метод StartService класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb530766781de4e23cc86778c1597a5c5c2a1014
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990569"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="6a813-103">Метод StartService класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="6a813-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6a813-104">Метод **StartService** пытается поместить указанную службу в свое состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="6a813-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="6a813-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a813-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6a813-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6a813-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a813-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a813-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="6a813-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a813-108">Parameters</span></span>

<span data-ttu-id="6a813-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6a813-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a813-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a813-110">Return value</span></span>

<span data-ttu-id="6a813-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="6a813-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="6a813-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6a813-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6a813-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6a813-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6a813-114">**0**</span><span class="sxs-lookup"><span data-stu-id="6a813-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-115">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="6a813-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-116">**1**</span><span class="sxs-lookup"><span data-stu-id="6a813-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6a813-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-118">**2**</span><span class="sxs-lookup"><span data-stu-id="6a813-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-119">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="6a813-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-120">**3**</span><span class="sxs-lookup"><span data-stu-id="6a813-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-121">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="6a813-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-122">**4**</span><span class="sxs-lookup"><span data-stu-id="6a813-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-123">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="6a813-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-124">**5**</span><span class="sxs-lookup"><span data-stu-id="6a813-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-125">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="6a813-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-126">**6**</span><span class="sxs-lookup"><span data-stu-id="6a813-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-127">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="6a813-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-128">**7**</span><span class="sxs-lookup"><span data-stu-id="6a813-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-129">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="6a813-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-130">**8**</span><span class="sxs-lookup"><span data-stu-id="6a813-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-131">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="6a813-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-132">**9**</span><span class="sxs-lookup"><span data-stu-id="6a813-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-133">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="6a813-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-134">**10**</span><span class="sxs-lookup"><span data-stu-id="6a813-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-135">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="6a813-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-136">**11**</span><span class="sxs-lookup"><span data-stu-id="6a813-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-137">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="6a813-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-138">**12**</span><span class="sxs-lookup"><span data-stu-id="6a813-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-139">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="6a813-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-140">**13**</span><span class="sxs-lookup"><span data-stu-id="6a813-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-141">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="6a813-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-142">**14**</span><span class="sxs-lookup"><span data-stu-id="6a813-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-143">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="6a813-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-144">**15**</span><span class="sxs-lookup"><span data-stu-id="6a813-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-145">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="6a813-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-146">**16**</span><span class="sxs-lookup"><span data-stu-id="6a813-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-147">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="6a813-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-148">**17**</span><span class="sxs-lookup"><span data-stu-id="6a813-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-149">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="6a813-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-150">**стр**</span><span class="sxs-lookup"><span data-stu-id="6a813-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-151">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="6a813-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-152">**стр**</span><span class="sxs-lookup"><span data-stu-id="6a813-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-153">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="6a813-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-154">**20**</span><span class="sxs-lookup"><span data-stu-id="6a813-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-155">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="6a813-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-156">**открыт**</span><span class="sxs-lookup"><span data-stu-id="6a813-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-157">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="6a813-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-158">**22**</span><span class="sxs-lookup"><span data-stu-id="6a813-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-159">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="6a813-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-160">**23**</span><span class="sxs-lookup"><span data-stu-id="6a813-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-161">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="6a813-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6a813-162">**24**</span><span class="sxs-lookup"><span data-stu-id="6a813-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="6a813-163">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="6a813-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a813-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a813-164">Remarks</span></span>

<span data-ttu-id="6a813-165">Хотя может показаться, что непрактичное различие между остановленной службой и приостановленной службой, два состояния по-разному отображаются в SCM.</span><span class="sxs-lookup"><span data-stu-id="6a813-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="6a813-166">Остановленная служба — это служба, которая не запущена и должна проходить всю процедуру запуска службы.</span><span class="sxs-lookup"><span data-stu-id="6a813-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="6a813-167">Однако Приостановленная служба все еще работает, но ее работа приостановлена.</span><span class="sxs-lookup"><span data-stu-id="6a813-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="6a813-168">По этой причине Приостановленная служба не обязана проходить всю процедуру запуска службы, но для ее возобновления требуется другая процедура.</span><span class="sxs-lookup"><span data-stu-id="6a813-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="6a813-169">Необходимо использовать правильный метод для запуска остановленной службы или возобновления работы приостановленной службы.</span><span class="sxs-lookup"><span data-stu-id="6a813-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="6a813-170">Методы [**\_ службы Win32**](win32-service.md) **StartService** и [**ResumeService**](resumeservice-method-in-class-win32-service.md) следует использовать в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="6a813-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="6a813-171">Если служба в данный момент остановлена, для ее перезапуска необходимо использовать метод **StartService** . [**ResumeService**](resumeservice-method-in-class-win32-service.md) не может запустить службу, которая в данный момент остановлена.</span><span class="sxs-lookup"><span data-stu-id="6a813-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="6a813-172">Если служба приостановлена, необходимо использовать [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="6a813-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="6a813-173">При использовании метода **StartService** в приостановленной службе появляется сообщение "служба уже запущена".</span><span class="sxs-lookup"><span data-stu-id="6a813-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="6a813-174">Однако служба остается приостановленной до тех пор, пока в нее не будет отправлен код управления службой возобновления.</span><span class="sxs-lookup"><span data-stu-id="6a813-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="6a813-175">При запуске остановленной службы, которая зависит от другой службы, запускаются обе службы.</span><span class="sxs-lookup"><span data-stu-id="6a813-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="6a813-176">При запуске службы с помощью этого метода все зависимые службы не запускаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="6a813-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="6a813-177">Для поиска зависимых объектов и их запуска по отдельности необходимо использовать класс ассоциации [**Win32 \_ Депендентсервице**](win32-dependentservice.md) и [соединители](/windows/desktop/WmiSdk/associators-of-statement) запроса.</span><span class="sxs-lookup"><span data-stu-id="6a813-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="6a813-178">Примеры</span><span class="sxs-lookup"><span data-stu-id="6a813-178">Examples</span></span>

<span data-ttu-id="6a813-179">Удаленный [Включение примера RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell удаленно включает службу Удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="6a813-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="6a813-180">Пример [остановки, запуска, включения или отключения службы](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell запускает, останавливает, включает или отключает службу.</span><span class="sxs-lookup"><span data-stu-id="6a813-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="6a813-181">В следующем образце кода Вбсскрипт показано, как запустить определенную службу из экземпляров [**\_ службы Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="6a813-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="6a813-182">В следующем образце кода Perl показано, как запустить определенную службу из экземпляров [**\_ службы Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="6a813-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="6a813-183">Следующий пример кода VBScript, NetDDE, зависит от службы Нетддедсдм.</span><span class="sxs-lookup"><span data-stu-id="6a813-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="6a813-184">Скрипт находит класс, от которого зависит NetDDE, и запускает его, который автоматически не запускает NetDDE.</span><span class="sxs-lookup"><span data-stu-id="6a813-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
```



## <a name="requirements"></a><span data-ttu-id="6a813-185">Требования</span><span class="sxs-lookup"><span data-stu-id="6a813-185">Requirements</span></span>



| <span data-ttu-id="6a813-186">Требование</span><span class="sxs-lookup"><span data-stu-id="6a813-186">Requirement</span></span> | <span data-ttu-id="6a813-187">Значение</span><span class="sxs-lookup"><span data-stu-id="6a813-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a813-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a813-188">Minimum supported client</span></span><br/> | <span data-ttu-id="6a813-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a813-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a813-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a813-190">Minimum supported server</span></span><br/> | <span data-ttu-id="6a813-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a813-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a813-192">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6a813-192">Namespace</span></span><br/>                | <span data-ttu-id="6a813-193">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6a813-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a813-194">MOF</span><span class="sxs-lookup"><span data-stu-id="6a813-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a813-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a813-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a813-196">DLL</span><span class="sxs-lookup"><span data-stu-id="6a813-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a813-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a813-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a813-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a813-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a813-199">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a813-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a813-200">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="6a813-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="6a813-201">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="6a813-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

