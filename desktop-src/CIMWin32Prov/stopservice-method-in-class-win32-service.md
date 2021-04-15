---
description: Помещает службу, представленную \_ объектом службы Win32, в остановленное состояние.
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: Метод «начало» класса Win32_Service (Сдоиас. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90d979754a3d6f034c353229dbaa1b1dbaedea79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655878"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a><span data-ttu-id="c0c55-103">Метод «начало» класса Win32_Service (Сдоиас. h)</span><span class="sxs-lookup"><span data-stu-id="c0c55-103">StopService method of the Win32_Service class (Sdoias.h)</span></span>

<span data-ttu-id="c0c55-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) "неработающий" помещает службу, представленную объектом [**\_ службы Win32**](win32-service.md) , в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c0c55-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_Service**](win32-service.md) object, in the stopped state.</span></span>

<span data-ttu-id="c0c55-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="c0c55-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c0c55-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c0c55-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c55-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0c55-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="c0c55-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0c55-108">Parameters</span></span>

<span data-ttu-id="c0c55-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c0c55-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0c55-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0c55-110">Return value</span></span>

<span data-ttu-id="c0c55-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c0c55-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c0c55-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c0c55-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c0c55-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c0c55-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c0c55-114">**0**</span><span class="sxs-lookup"><span data-stu-id="c0c55-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-115">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="c0c55-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-116">**1**</span><span class="sxs-lookup"><span data-stu-id="c0c55-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c0c55-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-118">**2**</span><span class="sxs-lookup"><span data-stu-id="c0c55-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-119">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c0c55-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-120">**3**</span><span class="sxs-lookup"><span data-stu-id="c0c55-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-121">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-122">**4**</span><span class="sxs-lookup"><span data-stu-id="c0c55-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-123">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-124">**5**</span><span class="sxs-lookup"><span data-stu-id="c0c55-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-125">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="c0c55-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-126">**6**</span><span class="sxs-lookup"><span data-stu-id="c0c55-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-127">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="c0c55-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-128">**7**</span><span class="sxs-lookup"><span data-stu-id="c0c55-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-129">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="c0c55-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-130">**8**</span><span class="sxs-lookup"><span data-stu-id="c0c55-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-131">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-132">**9**</span><span class="sxs-lookup"><span data-stu-id="c0c55-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-133">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-134">**10**</span><span class="sxs-lookup"><span data-stu-id="c0c55-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-135">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="c0c55-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-136">**11**</span><span class="sxs-lookup"><span data-stu-id="c0c55-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-137">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="c0c55-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-138">**12**</span><span class="sxs-lookup"><span data-stu-id="c0c55-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-139">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-140">**13**</span><span class="sxs-lookup"><span data-stu-id="c0c55-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-141">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="c0c55-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-142">**14**</span><span class="sxs-lookup"><span data-stu-id="c0c55-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-143">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="c0c55-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-144">**15**</span><span class="sxs-lookup"><span data-stu-id="c0c55-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-145">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="c0c55-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-146">**16**</span><span class="sxs-lookup"><span data-stu-id="c0c55-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-147">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-148">**17**</span><span class="sxs-lookup"><span data-stu-id="c0c55-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-149">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="c0c55-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-150">**стр**</span><span class="sxs-lookup"><span data-stu-id="c0c55-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-151">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="c0c55-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-152">**стр**</span><span class="sxs-lookup"><span data-stu-id="c0c55-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-153">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="c0c55-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-154">**20**</span><span class="sxs-lookup"><span data-stu-id="c0c55-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-155">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-156">**открыт**</span><span class="sxs-lookup"><span data-stu-id="c0c55-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-157">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="c0c55-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-158">**22**</span><span class="sxs-lookup"><span data-stu-id="c0c55-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-159">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-160">**23**</span><span class="sxs-lookup"><span data-stu-id="c0c55-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-161">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="c0c55-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0c55-162">**24**</span><span class="sxs-lookup"><span data-stu-id="c0c55-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c0c55-163">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="c0c55-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0c55-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0c55-164">Remarks</span></span>

<span data-ttu-id="c0c55-165">Определив, какие службы могут быть остановлены или приостановлены, можно использовать **методы "** [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) " и "приостановить" для остановки и приостановки служб.</span><span class="sxs-lookup"><span data-stu-id="c0c55-165">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="c0c55-166">Решение о прекращении работы службы, а не приостановке или наоборот, зависит от нескольких факторов, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="c0c55-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="c0c55-167">Может ли служба быть приостановлена?</span><span class="sxs-lookup"><span data-stu-id="c0c55-167">Is the service capable of being paused?</span></span> <span data-ttu-id="c0c55-168">В противном случае единственным вариантом будет «останавливает службу».</span><span class="sxs-lookup"><span data-stu-id="c0c55-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="c0c55-169">Нужно ли продолжать обработку запросов клиентов для всех, кто уже подключен к службе?</span><span class="sxs-lookup"><span data-stu-id="c0c55-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="c0c55-170">Если да, то приостановка службы обычно позволяет ей управлять существующими клиентами при запрете доступа к новым клиентам.</span><span class="sxs-lookup"><span data-stu-id="c0c55-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="c0c55-171">Напротив, при прекращении службы все клиенты сразу же отключаются.</span><span class="sxs-lookup"><span data-stu-id="c0c55-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="c0c55-172">Нужно ли перенастроить службу, чтобы изменения вступили в силу немедленно?</span><span class="sxs-lookup"><span data-stu-id="c0c55-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="c0c55-173">Несмотря на то, что свойства службы могут быть изменены, пока служба приостановлена, большинство из них не вступают в силу, пока служба не будет остановлена и перезапущена.</span><span class="sxs-lookup"><span data-stu-id="c0c55-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="c0c55-174">Код скрипта, необходимый для остановки службы, почти идентичен коду, требуемому для приостановки службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="c0c55-175">При попытке отключить службу, для которой выполняются зависимые службы **, метод «не работает» возвращает** значение 3.</span><span class="sxs-lookup"><span data-stu-id="c0c55-175">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="c0c55-176">Сначала необходимо остановить зависимые службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-176">The dependent services must be stopped first.</span></span>

<span data-ttu-id="c0c55-177">Если служба останавливается, сразу же проверьте [**\_ службу Win32**](win32-service.md).**State** , так как значение по-прежнему может отображать службу как выполняющуюся.</span><span class="sxs-lookup"><span data-stu-id="c0c55-177">If you stop a service, then immediately check the [**Win32\_Service**](win32-service.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="c0c55-178">Примеры</span><span class="sxs-lookup"><span data-stu-id="c0c55-178">Examples</span></span>

<span data-ttu-id="c0c55-179">[Set-ремотесервице](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) Образец PowerShell задает состояние службы для удаленных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="c0c55-179">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="c0c55-180">При [остановке службы и ее зависимых](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) примеров VBScript останавливается служба и все зависимые службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-180">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

<span data-ttu-id="c0c55-181">В следующем примере кода VBScript показано, как завершить работу службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-181">The following VBScript code sample demonstrates how to shut down a service.</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



<span data-ttu-id="c0c55-182">В следующем образце кода Perl показано, как завершить работу службы.</span><span class="sxs-lookup"><span data-stu-id="c0c55-182">The following Perl code sample demonstrates how to shut down a service.</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="c0c55-183">В следующем примере кода VBScript показано, что нельзя остановить службу NetDDE до тех пор, пока зависимые службы не будут остановлены.</span><span class="sxs-lookup"><span data-stu-id="c0c55-183">The following VBScript code example shows that you cannot stop the NetDDE service until the dependent services have been stopped.</span></span> <span data-ttu-id="c0c55-184">Чтобы запустить сценарий, убедитесь, что служба NetDDE и ее зависимые службы запущены с помощью оснастки MMC Services. msc или команды **net start** .</span><span class="sxs-lookup"><span data-stu-id="c0c55-184">To run the script, ensure that the NetDDE service and its dependent services are running by using the Services.msc MMC snap-in or the **Net Start** command.</span></span>

<span data-ttu-id="c0c55-185">Класс [**Win32 \_ депендентсервице**](win32-dependentservice.md) позволяет размещать зависимости службы с помощью [соединителей](/windows/desktop/WmiSdk/associators-of-statement) запроса.</span><span class="sxs-lookup"><span data-stu-id="c0c55-185">The [**Win32\_DependentService**](win32-dependentservice.md) class allows you to locate service dependencies through an [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a><span data-ttu-id="c0c55-186">Требования</span><span class="sxs-lookup"><span data-stu-id="c0c55-186">Requirements</span></span>



| <span data-ttu-id="c0c55-187">Требование</span><span class="sxs-lookup"><span data-stu-id="c0c55-187">Requirement</span></span> | <span data-ttu-id="c0c55-188">Значение</span><span class="sxs-lookup"><span data-stu-id="c0c55-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c55-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0c55-189">Minimum supported client</span></span><br/> | <span data-ttu-id="c0c55-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c55-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0c55-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0c55-191">Minimum supported server</span></span><br/> | <span data-ttu-id="c0c55-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0c55-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0c55-193">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0c55-193">Namespace</span></span><br/>                | <span data-ttu-id="c0c55-194">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c0c55-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0c55-195">Header</span><span class="sxs-lookup"><span data-stu-id="c0c55-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0c55-196"><dt>Сдоиас. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0c55-196"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="c0c55-197">MOF</span><span class="sxs-lookup"><span data-stu-id="c0c55-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0c55-198"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0c55-198"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0c55-199">DLL</span><span class="sxs-lookup"><span data-stu-id="c0c55-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0c55-200"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0c55-200"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0c55-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0c55-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0c55-202">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0c55-202">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c0c55-203">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="c0c55-203">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="c0c55-204">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="c0c55-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="c0c55-205">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="c0c55-205">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 

