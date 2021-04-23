---
description: Пытается поместить службу, на которую указывает ссылка, в состоянии возобновления.
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Метод ResumeService класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ed4141b02d6e08bd4b106d2c1f72ce3fe0620fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896438"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="9a231-103">Метод ResumeService класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9a231-103">ResumeService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9a231-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ResumeService пытается поместить службу, на которую указывает ссылка, в состоянии возобновления.</span><span class="sxs-lookup"><span data-stu-id="9a231-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="9a231-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="9a231-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9a231-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9a231-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a231-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a231-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="9a231-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a231-108">Parameters</span></span>

<span data-ttu-id="9a231-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9a231-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a231-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a231-110">Return value</span></span>

<span data-ttu-id="9a231-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="9a231-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="9a231-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9a231-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9a231-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9a231-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9a231-114">**0**</span><span class="sxs-lookup"><span data-stu-id="9a231-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-115">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="9a231-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-116">**1**</span><span class="sxs-lookup"><span data-stu-id="9a231-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9a231-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-118">**2**</span><span class="sxs-lookup"><span data-stu-id="9a231-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-119">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="9a231-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-120">**3**</span><span class="sxs-lookup"><span data-stu-id="9a231-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-121">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="9a231-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-122">**4**</span><span class="sxs-lookup"><span data-stu-id="9a231-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-123">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="9a231-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-124">**5**</span><span class="sxs-lookup"><span data-stu-id="9a231-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-125">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="9a231-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-126">**6**</span><span class="sxs-lookup"><span data-stu-id="9a231-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-127">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="9a231-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-128">**7**</span><span class="sxs-lookup"><span data-stu-id="9a231-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-129">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="9a231-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-130">**8**</span><span class="sxs-lookup"><span data-stu-id="9a231-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-131">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="9a231-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-132">**9**</span><span class="sxs-lookup"><span data-stu-id="9a231-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-133">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="9a231-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-134">**10**</span><span class="sxs-lookup"><span data-stu-id="9a231-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-135">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="9a231-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-136">**11**</span><span class="sxs-lookup"><span data-stu-id="9a231-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-137">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="9a231-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-138">**12**</span><span class="sxs-lookup"><span data-stu-id="9a231-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-139">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="9a231-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-140">**13**</span><span class="sxs-lookup"><span data-stu-id="9a231-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-141">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="9a231-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-142">**14**</span><span class="sxs-lookup"><span data-stu-id="9a231-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-143">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="9a231-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-144">**15**</span><span class="sxs-lookup"><span data-stu-id="9a231-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-145">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="9a231-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-146">**16**</span><span class="sxs-lookup"><span data-stu-id="9a231-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-147">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="9a231-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-148">**17**</span><span class="sxs-lookup"><span data-stu-id="9a231-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-149">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="9a231-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-150">**стр**</span><span class="sxs-lookup"><span data-stu-id="9a231-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-151">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="9a231-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-152">**стр**</span><span class="sxs-lookup"><span data-stu-id="9a231-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-153">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="9a231-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-154">**20**</span><span class="sxs-lookup"><span data-stu-id="9a231-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-155">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="9a231-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-156">**открыт**</span><span class="sxs-lookup"><span data-stu-id="9a231-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-157">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="9a231-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-158">**22**</span><span class="sxs-lookup"><span data-stu-id="9a231-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-159">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="9a231-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-160">**23**</span><span class="sxs-lookup"><span data-stu-id="9a231-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-161">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="9a231-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9a231-162">**24**</span><span class="sxs-lookup"><span data-stu-id="9a231-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="9a231-163">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="9a231-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a231-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a231-164">Remarks</span></span>

<span data-ttu-id="9a231-165">Хотя может показаться, что непрактичное различие между остановленной службой и приостановленной службой, два состояния по-разному отображаются в SCM.</span><span class="sxs-lookup"><span data-stu-id="9a231-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="9a231-166">Остановленная служба — это служба, которая не запущена и должна проходить всю процедуру запуска службы.</span><span class="sxs-lookup"><span data-stu-id="9a231-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="9a231-167">Однако Приостановленная служба все еще работает, но ее работа приостановлена.</span><span class="sxs-lookup"><span data-stu-id="9a231-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="9a231-168">По этой причине Приостановленная служба не обязана проходить всю процедуру запуска службы, но для ее возобновления требуется другая процедура.</span><span class="sxs-lookup"><span data-stu-id="9a231-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="9a231-169">Необходимо использовать правильный метод для запуска остановленной службы или возобновления работы приостановленной службы.</span><span class="sxs-lookup"><span data-stu-id="9a231-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="9a231-170">Методы [**\_ службы Win32**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) и **ResumeService** следует использовать в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="9a231-170">The [**Win32\_Service**](win32-service.md) methods [**StartService**](startservice-method-in-class-win32-service.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="9a231-171">Если служба в данный момент остановлена, для ее перезапуска необходимо использовать метод [**StartService**](startservice-method-in-class-win32-service.md) . **ResumeService** не может запустить службу, которая в данный момент остановлена.</span><span class="sxs-lookup"><span data-stu-id="9a231-171">If a service is currently stopped, you must use the [**StartService**](startservice-method-in-class-win32-service.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="9a231-172">Если служба приостановлена, необходимо использовать **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="9a231-172">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="9a231-173">При использовании метода [**StartService**](startservice-method-in-class-win32-service.md) в приостановленной службе появляется сообщение "служба уже запущена".</span><span class="sxs-lookup"><span data-stu-id="9a231-173">If you use the [**StartService**](startservice-method-in-class-win32-service.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="9a231-174">Однако служба остается приостановленной до тех пор, пока в нее не будет отправлен код управления службой возобновления.</span><span class="sxs-lookup"><span data-stu-id="9a231-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="9a231-175">Примеры</span><span class="sxs-lookup"><span data-stu-id="9a231-175">Examples</span></span>

<span data-ttu-id="9a231-176">В [службах возобновления работы, приостановленных](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) с помощью VBScript, перезапускаются все приостановленные службы автозапуска.</span><span class="sxs-lookup"><span data-stu-id="9a231-176">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

<span data-ttu-id="9a231-177">Следующий пример кода VBScript описывает, как возобновить приостановленную службу из экземпляров [**\_ службы Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="9a231-177">The following VBScript code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="9a231-178">Служба должна поддерживать приостановку и выполнение уже запущено.</span><span class="sxs-lookup"><span data-stu-id="9a231-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
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



<span data-ttu-id="9a231-179">В следующем образце кода Perl описывается, как возобновить приостановленную службу из экземпляров [**\_ службы Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="9a231-179">The following Perl code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="9a231-180">Служба должна поддерживать приостановку и выполнение уже запущено.</span><span class="sxs-lookup"><span data-stu-id="9a231-180">The service must support pausing and be running already.</span></span>

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
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
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="9a231-181">Требования</span><span class="sxs-lookup"><span data-stu-id="9a231-181">Requirements</span></span>



| <span data-ttu-id="9a231-182">Требование</span><span class="sxs-lookup"><span data-stu-id="9a231-182">Requirement</span></span> | <span data-ttu-id="9a231-183">Значение</span><span class="sxs-lookup"><span data-stu-id="9a231-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a231-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a231-184">Minimum supported client</span></span><br/> | <span data-ttu-id="9a231-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a231-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a231-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a231-186">Minimum supported server</span></span><br/> | <span data-ttu-id="9a231-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a231-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a231-188">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9a231-188">Namespace</span></span><br/>                | <span data-ttu-id="9a231-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9a231-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="9a231-190">MOF</span><span class="sxs-lookup"><span data-stu-id="9a231-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a231-191"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a231-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a231-192">DLL</span><span class="sxs-lookup"><span data-stu-id="9a231-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a231-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a231-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a231-194">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a231-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a231-195">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a231-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9a231-196">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="9a231-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="9a231-197">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="9a231-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

