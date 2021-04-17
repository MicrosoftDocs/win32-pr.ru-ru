---
title: Метод Чанжестартмоде класса Win32_Service (службы удаленных рабочих столов)
description: Изменяет режим запуска Win32 \_ терминалсервице.
ms.assetid: 4F4B8CFC-B38C-47C6-A2BA-D498EC2B7F55
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Чанжестартмоде
- Службы удаленных рабочих столов метода Чанжестартмоде, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод Чанжестартмоде
topic_type:
- apiref
api_name:
- Win32_Service.ChangeStartMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a46c6b72fbb070dac32b2b6990a217068c77da9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681870"
---
# <a name="changestartmode-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="474bc-106">Метод Чанжестартмоде класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="474bc-106">ChangeStartMode method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="474bc-107">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) Чанжестартмоде изменяет режим запуска [**Win32 \_ терминалсервице**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="474bc-107">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="474bc-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="474bc-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="474bc-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="474bc-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="474bc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="474bc-110">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode
);
```



## <a name="parameters"></a><span data-ttu-id="474bc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="474bc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="474bc-112">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="474bc-112">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="474bc-113">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="474bc-113">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="474bc-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Файле**</span><span class="sxs-lookup"><span data-stu-id="474bc-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="474bc-115">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="474bc-115">Device driver started by the operating system loader.</span></span> <span data-ttu-id="474bc-116">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="474bc-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="474bc-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Системой**</span><span class="sxs-lookup"><span data-stu-id="474bc-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="474bc-118">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="474bc-118">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="474bc-119">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="474bc-119">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="474bc-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Автоматически**</span><span class="sxs-lookup"><span data-stu-id="474bc-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="474bc-121">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="474bc-121">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="474bc-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную**</span><span class="sxs-lookup"><span data-stu-id="474bc-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="474bc-123">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="474bc-123">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="474bc-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Доступ**</span><span class="sxs-lookup"><span data-stu-id="474bc-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="474bc-125">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="474bc-125">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="474bc-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="474bc-126">Return value</span></span>

<span data-ttu-id="474bc-127">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="474bc-127">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="474bc-128">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="474bc-128">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="474bc-129">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="474bc-129">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="474bc-130">**0**</span><span class="sxs-lookup"><span data-stu-id="474bc-130">**0**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-131">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="474bc-131">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-132">**1**</span><span class="sxs-lookup"><span data-stu-id="474bc-132">**1**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-133">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="474bc-133">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-134">**2**</span><span class="sxs-lookup"><span data-stu-id="474bc-134">**2**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-135">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="474bc-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-136">**3**</span><span class="sxs-lookup"><span data-stu-id="474bc-136">**3**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-137">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="474bc-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-138">**4**</span><span class="sxs-lookup"><span data-stu-id="474bc-138">**4**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-139">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="474bc-139">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-140">**5**</span><span class="sxs-lookup"><span data-stu-id="474bc-140">**5**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-141">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="474bc-141">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-142">**6**</span><span class="sxs-lookup"><span data-stu-id="474bc-142">**6**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-143">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="474bc-143">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-144">**7**</span><span class="sxs-lookup"><span data-stu-id="474bc-144">**7**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-145">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="474bc-145">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-146">**8**</span><span class="sxs-lookup"><span data-stu-id="474bc-146">**8**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-147">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="474bc-147">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-148">**9**</span><span class="sxs-lookup"><span data-stu-id="474bc-148">**9**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-149">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="474bc-149">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-150">**10**</span><span class="sxs-lookup"><span data-stu-id="474bc-150">**10**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-151">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="474bc-151">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-152">**11**</span><span class="sxs-lookup"><span data-stu-id="474bc-152">**11**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-153">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="474bc-153">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-154">**12**</span><span class="sxs-lookup"><span data-stu-id="474bc-154">**12**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-155">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="474bc-155">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-156">**13**</span><span class="sxs-lookup"><span data-stu-id="474bc-156">**13**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-157">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="474bc-157">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-158">**14**</span><span class="sxs-lookup"><span data-stu-id="474bc-158">**14**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-159">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="474bc-159">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-160">**15**</span><span class="sxs-lookup"><span data-stu-id="474bc-160">**15**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-161">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="474bc-161">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-162">**16**</span><span class="sxs-lookup"><span data-stu-id="474bc-162">**16**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-163">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="474bc-163">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-164">**17**</span><span class="sxs-lookup"><span data-stu-id="474bc-164">**17**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-165">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="474bc-165">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-166">**стр**</span><span class="sxs-lookup"><span data-stu-id="474bc-166">**18**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-167">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="474bc-167">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-168">**стр**</span><span class="sxs-lookup"><span data-stu-id="474bc-168">**19**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-169">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="474bc-169">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-170">**20**</span><span class="sxs-lookup"><span data-stu-id="474bc-170">**20**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-171">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="474bc-171">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-172">**открыт**</span><span class="sxs-lookup"><span data-stu-id="474bc-172">**21**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-173">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="474bc-173">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-174">**22**</span><span class="sxs-lookup"><span data-stu-id="474bc-174">**22**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-175">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="474bc-175">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-176">**23**</span><span class="sxs-lookup"><span data-stu-id="474bc-176">**23**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-177">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="474bc-177">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="474bc-178">**24**</span><span class="sxs-lookup"><span data-stu-id="474bc-178">**24**</span></span>
</dt> <dd>

<span data-ttu-id="474bc-179">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="474bc-179">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="474bc-180">Примеры</span><span class="sxs-lookup"><span data-stu-id="474bc-180">Examples</span></span>

<span data-ttu-id="474bc-181">Следующее [изменение StartMode примера службы](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell, извлеченного из коллекции TechNet, изменяет режим запуска службы.</span><span class="sxs-lookup"><span data-stu-id="474bc-181">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="474bc-182">Требования</span><span class="sxs-lookup"><span data-stu-id="474bc-182">Requirements</span></span>



| <span data-ttu-id="474bc-183">Требование</span><span class="sxs-lookup"><span data-stu-id="474bc-183">Requirement</span></span> | <span data-ttu-id="474bc-184">Значение</span><span class="sxs-lookup"><span data-stu-id="474bc-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="474bc-185">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="474bc-185">Minimum supported client</span></span><br/> | <span data-ttu-id="474bc-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="474bc-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="474bc-187">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="474bc-187">Minimum supported server</span></span><br/> | <span data-ttu-id="474bc-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="474bc-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="474bc-189">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="474bc-189">Namespace</span></span><br/>                | <span data-ttu-id="474bc-190">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="474bc-190">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="474bc-191">MOF</span><span class="sxs-lookup"><span data-stu-id="474bc-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="474bc-192"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="474bc-192"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="474bc-193">DLL</span><span class="sxs-lookup"><span data-stu-id="474bc-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="474bc-194"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="474bc-194"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="474bc-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="474bc-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="474bc-196">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="474bc-196">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="474bc-197">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="474bc-197">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="474bc-198">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="474bc-198">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="474bc-199">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="474bc-199">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

