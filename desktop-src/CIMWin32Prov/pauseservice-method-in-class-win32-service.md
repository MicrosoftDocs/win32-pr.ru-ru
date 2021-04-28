---
description: Метод PauseService класса Win32_Service (поставщики WMI CIMWin32) — пытается перевести службу в приостановленное состояние.
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: Метод PauseService класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7654feea410564137e98861c4c0b5de2b5e7192e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096952"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="dc569-103">Метод PauseService класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="dc569-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dc569-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) PauseService пытается перевести службу в приостановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="dc569-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="dc569-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="dc569-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dc569-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dc569-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc569-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc569-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="dc569-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc569-108">Parameters</span></span>

<span data-ttu-id="dc569-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dc569-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc569-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc569-110">Return value</span></span>

<span data-ttu-id="dc569-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="dc569-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="dc569-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="dc569-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="dc569-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="dc569-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="dc569-114">**0**</span><span class="sxs-lookup"><span data-stu-id="dc569-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-115">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="dc569-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-116">**1**</span><span class="sxs-lookup"><span data-stu-id="dc569-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc569-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-118">**2**</span><span class="sxs-lookup"><span data-stu-id="dc569-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-119">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="dc569-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-120">**3**</span><span class="sxs-lookup"><span data-stu-id="dc569-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-121">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="dc569-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-122">**4**</span><span class="sxs-lookup"><span data-stu-id="dc569-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-123">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="dc569-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-124">**5**</span><span class="sxs-lookup"><span data-stu-id="dc569-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-125">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="dc569-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-126">**6**</span><span class="sxs-lookup"><span data-stu-id="dc569-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-127">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="dc569-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-128">**7**</span><span class="sxs-lookup"><span data-stu-id="dc569-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-129">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="dc569-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-130">**8**</span><span class="sxs-lookup"><span data-stu-id="dc569-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-131">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="dc569-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-132">**9**</span><span class="sxs-lookup"><span data-stu-id="dc569-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-133">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="dc569-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-134">**10**</span><span class="sxs-lookup"><span data-stu-id="dc569-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-135">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="dc569-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-136">**11**</span><span class="sxs-lookup"><span data-stu-id="dc569-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-137">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="dc569-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-138">**12**</span><span class="sxs-lookup"><span data-stu-id="dc569-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-139">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="dc569-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-140">**13**</span><span class="sxs-lookup"><span data-stu-id="dc569-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-141">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="dc569-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-142">**14**</span><span class="sxs-lookup"><span data-stu-id="dc569-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-143">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="dc569-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-144">**15**</span><span class="sxs-lookup"><span data-stu-id="dc569-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-145">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="dc569-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-146">**16**</span><span class="sxs-lookup"><span data-stu-id="dc569-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-147">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="dc569-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-148">**17**</span><span class="sxs-lookup"><span data-stu-id="dc569-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-149">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="dc569-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-150">**стр**</span><span class="sxs-lookup"><span data-stu-id="dc569-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-151">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="dc569-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-152">**стр**</span><span class="sxs-lookup"><span data-stu-id="dc569-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-153">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="dc569-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-154">**20**</span><span class="sxs-lookup"><span data-stu-id="dc569-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-155">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="dc569-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-156">**открыт**</span><span class="sxs-lookup"><span data-stu-id="dc569-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-157">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="dc569-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-158">**22**</span><span class="sxs-lookup"><span data-stu-id="dc569-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-159">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="dc569-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-160">**23**</span><span class="sxs-lookup"><span data-stu-id="dc569-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-161">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="dc569-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="dc569-162">**24**</span><span class="sxs-lookup"><span data-stu-id="dc569-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="dc569-163">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="dc569-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc569-164">Remarks</span><span class="sxs-lookup"><span data-stu-id="dc569-164">Remarks</span></span>

<span data-ttu-id="dc569-165">Определив, какие службы могут быть остановлены или приостановлены, можно использовать [**методы "**](stopservice-method-in-class-win32-service.md) [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) " и "приостановить" для остановки и приостановки служб.</span><span class="sxs-lookup"><span data-stu-id="dc569-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="dc569-166">Решение о прекращении работы службы, а не приостановке или наоборот, зависит от нескольких факторов, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="dc569-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="dc569-167">Может ли служба быть приостановлена?</span><span class="sxs-lookup"><span data-stu-id="dc569-167">Is the service capable of being paused?</span></span> <span data-ttu-id="dc569-168">В противном случае единственным вариантом будет «останавливает службу».</span><span class="sxs-lookup"><span data-stu-id="dc569-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="dc569-169">Нужно ли продолжать обработку запросов клиентов для всех, кто уже подключен к службе?</span><span class="sxs-lookup"><span data-stu-id="dc569-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="dc569-170">Если да, то приостановка службы обычно позволяет ей управлять существующими клиентами при запрете доступа к новым клиентам.</span><span class="sxs-lookup"><span data-stu-id="dc569-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="dc569-171">Напротив, при прекращении службы все клиенты сразу же отключаются.</span><span class="sxs-lookup"><span data-stu-id="dc569-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="dc569-172">Нужно ли перенастроить службу, чтобы изменения вступили в силу немедленно?</span><span class="sxs-lookup"><span data-stu-id="dc569-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="dc569-173">Несмотря на то, что свойства службы могут быть изменены, пока служба приостановлена, большинство из них не вступают в силу, пока служба не будет остановлена и перезапущена.</span><span class="sxs-lookup"><span data-stu-id="dc569-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="dc569-174">Код скрипта, необходимый для остановки службы, почти идентичен коду, требуемому для приостановки службы.</span><span class="sxs-lookup"><span data-stu-id="dc569-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="dc569-175">Примеры</span><span class="sxs-lookup"><span data-stu-id="dc569-175">Examples</span></span>

<span data-ttu-id="dc569-176">[Службы Pause, работающие под конкретной учетной записью,](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) заостанавливают все службы, работающие под гипотетической учетной записью службы "нетсвк".</span><span class="sxs-lookup"><span data-stu-id="dc569-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="dc569-177">В следующем примере кода VBScript показано, как приостановить определенную службу из экземпляров [**\_ службы Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="dc569-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="dc569-178">Служба должна поддерживать приостановку и выполнение уже запущено.</span><span class="sxs-lookup"><span data-stu-id="dc569-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



<span data-ttu-id="dc569-179">В следующем образце кода Perl показано, как приостановить определенную службу из [**экземпляров \_ службы Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="dc569-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="dc569-180">Служба должна поддерживать приостановку и выполнение уже запущено.</span><span class="sxs-lookup"><span data-stu-id="dc569-180">The service must support pausing and be running already.</span></span>

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
    }
   } 
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="dc569-181">Требования</span><span class="sxs-lookup"><span data-stu-id="dc569-181">Requirements</span></span>



| <span data-ttu-id="dc569-182">Требование</span><span class="sxs-lookup"><span data-stu-id="dc569-182">Requirement</span></span> | <span data-ttu-id="dc569-183">Значение</span><span class="sxs-lookup"><span data-stu-id="dc569-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc569-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc569-184">Minimum supported client</span></span><br/> | <span data-ttu-id="dc569-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc569-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc569-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc569-186">Minimum supported server</span></span><br/> | <span data-ttu-id="dc569-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc569-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc569-188">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dc569-188">Namespace</span></span><br/>                | <span data-ttu-id="dc569-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="dc569-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="dc569-190">MOF</span><span class="sxs-lookup"><span data-stu-id="dc569-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc569-191"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc569-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc569-192">DLL</span><span class="sxs-lookup"><span data-stu-id="dc569-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc569-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc569-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc569-194">См. также</span><span class="sxs-lookup"><span data-stu-id="dc569-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc569-195">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dc569-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dc569-196">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="dc569-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="dc569-197">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="dc569-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="dc569-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="dc569-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

