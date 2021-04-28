---
title: Метод StartService класса Win32_Service (службы удаленных рабочих столов)
description: Метод StartService класса Win32_Service (службы удаленных рабочих столов) — пытается поместить службу, на которую указывает ссылка, в состояние запуска.
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- Метод StartService службы удаленных рабочих столов
- Метод StartService службы удаленных рабочих столов, Win32_Service класс
- Класс Win32_Service службы удаленных рабочих столов, метод StartService
topic_type:
- apiref
api_name:
- Win32_Service.StartService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4bd12150223d7cdc1340b7557ba309a1e07da4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084202"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="0914f-106">Метод StartService класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="0914f-106">StartService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="0914f-107">Метод **StartService** пытается поместить указанную службу в свое состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="0914f-107">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="0914f-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="0914f-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0914f-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0914f-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0914f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0914f-110">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="0914f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="0914f-111">Parameters</span></span>

<span data-ttu-id="0914f-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0914f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0914f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0914f-113">Return value</span></span>

<span data-ttu-id="0914f-114">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="0914f-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="0914f-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0914f-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0914f-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0914f-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0914f-117">**0**</span><span class="sxs-lookup"><span data-stu-id="0914f-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-118">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="0914f-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-119">**1**</span><span class="sxs-lookup"><span data-stu-id="0914f-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-120">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0914f-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-121">**2**</span><span class="sxs-lookup"><span data-stu-id="0914f-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="0914f-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-123">**3**</span><span class="sxs-lookup"><span data-stu-id="0914f-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-124">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="0914f-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-125">**4**</span><span class="sxs-lookup"><span data-stu-id="0914f-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="0914f-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-127">**5**</span><span class="sxs-lookup"><span data-stu-id="0914f-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-128">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="0914f-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-129">**6**</span><span class="sxs-lookup"><span data-stu-id="0914f-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-130">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="0914f-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-131">**7**</span><span class="sxs-lookup"><span data-stu-id="0914f-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-132">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="0914f-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-133">**8**</span><span class="sxs-lookup"><span data-stu-id="0914f-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="0914f-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-135">**9**</span><span class="sxs-lookup"><span data-stu-id="0914f-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="0914f-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-137">**10**</span><span class="sxs-lookup"><span data-stu-id="0914f-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="0914f-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-139">**11**</span><span class="sxs-lookup"><span data-stu-id="0914f-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="0914f-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-141">**12**</span><span class="sxs-lookup"><span data-stu-id="0914f-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="0914f-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-143">**13**</span><span class="sxs-lookup"><span data-stu-id="0914f-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="0914f-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-145">**14**</span><span class="sxs-lookup"><span data-stu-id="0914f-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="0914f-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-147">**15**</span><span class="sxs-lookup"><span data-stu-id="0914f-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="0914f-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-149">**16**</span><span class="sxs-lookup"><span data-stu-id="0914f-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="0914f-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-151">**17**</span><span class="sxs-lookup"><span data-stu-id="0914f-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="0914f-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="0914f-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="0914f-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="0914f-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="0914f-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-157">**20**</span><span class="sxs-lookup"><span data-stu-id="0914f-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="0914f-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-159">**открыт**</span><span class="sxs-lookup"><span data-stu-id="0914f-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-160">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="0914f-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-161">**22**</span><span class="sxs-lookup"><span data-stu-id="0914f-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-162">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="0914f-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-163">**23**</span><span class="sxs-lookup"><span data-stu-id="0914f-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-164">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="0914f-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0914f-165">**24**</span><span class="sxs-lookup"><span data-stu-id="0914f-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0914f-166">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="0914f-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0914f-167">Remarks</span><span class="sxs-lookup"><span data-stu-id="0914f-167">Remarks</span></span>

<span data-ttu-id="0914f-168">Хотя может показаться, что непрактичное различие между остановленной службой и приостановленной службой, два состояния по-разному отображаются в SCM.</span><span class="sxs-lookup"><span data-stu-id="0914f-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="0914f-169">Остановленная служба — это служба, которая не запущена и должна проходить всю процедуру запуска службы.</span><span class="sxs-lookup"><span data-stu-id="0914f-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="0914f-170">Однако Приостановленная служба все еще работает, но ее работа приостановлена.</span><span class="sxs-lookup"><span data-stu-id="0914f-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="0914f-171">По этой причине Приостановленная служба не обязана проходить всю процедуру запуска службы, но для ее возобновления требуется другая процедура.</span><span class="sxs-lookup"><span data-stu-id="0914f-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="0914f-172">Необходимо использовать правильный метод для запуска остановленной службы или возобновления работы приостановленной службы.</span><span class="sxs-lookup"><span data-stu-id="0914f-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="0914f-173">Методы [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** и [**ResumeService**](win32-terminalservice-resumeservice.md) следует использовать в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="0914f-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods **StartService** and [**ResumeService**](win32-terminalservice-resumeservice.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="0914f-174">Если служба в данный момент остановлена, для ее перезапуска необходимо использовать метод **StartService** . [**ResumeService**](win32-terminalservice-resumeservice.md) не может запустить службу, которая в данный момент остановлена.</span><span class="sxs-lookup"><span data-stu-id="0914f-174">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](win32-terminalservice-resumeservice.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="0914f-175">Если служба приостановлена, необходимо использовать [**ResumeService**](win32-terminalservice-resumeservice.md).</span><span class="sxs-lookup"><span data-stu-id="0914f-175">If a service is paused, you must use [**ResumeService**](win32-terminalservice-resumeservice.md).</span></span> <span data-ttu-id="0914f-176">При использовании метода **StartService** в приостановленной службе появляется сообщение "служба уже запущена".</span><span class="sxs-lookup"><span data-stu-id="0914f-176">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="0914f-177">Однако служба остается приостановленной до тех пор, пока в нее не будет отправлен код управления службой возобновления.</span><span class="sxs-lookup"><span data-stu-id="0914f-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="0914f-178">При запуске остановленной службы, которая зависит от другой службы, запускаются обе службы.</span><span class="sxs-lookup"><span data-stu-id="0914f-178">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="0914f-179">При запуске службы с помощью этого метода все зависимые службы не запускаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="0914f-179">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="0914f-180">Для поиска зависимых объектов и их запуска по отдельности необходимо использовать класс ассоциации [**Win32 \_ Депендентсервице**](/windows/desktop/CIMWin32Prov/win32-dependentservice) и [соединители](/windows/desktop/WmiSdk/associators-of-statement) запроса.</span><span class="sxs-lookup"><span data-stu-id="0914f-180">You must use the association class [**Win32\_DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="requirements"></a><span data-ttu-id="0914f-181">Требования</span><span class="sxs-lookup"><span data-stu-id="0914f-181">Requirements</span></span>



| <span data-ttu-id="0914f-182">Требование</span><span class="sxs-lookup"><span data-stu-id="0914f-182">Requirement</span></span> | <span data-ttu-id="0914f-183">Значение</span><span class="sxs-lookup"><span data-stu-id="0914f-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0914f-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0914f-184">Minimum supported client</span></span><br/> | <span data-ttu-id="0914f-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0914f-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0914f-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0914f-186">Minimum supported server</span></span><br/> | <span data-ttu-id="0914f-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0914f-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0914f-188">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0914f-188">Namespace</span></span><br/>                | <span data-ttu-id="0914f-189">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0914f-189">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0914f-190">MOF</span><span class="sxs-lookup"><span data-stu-id="0914f-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0914f-191"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0914f-191"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0914f-192">DLL</span><span class="sxs-lookup"><span data-stu-id="0914f-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0914f-193"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0914f-193"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0914f-194">См. также</span><span class="sxs-lookup"><span data-stu-id="0914f-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0914f-195">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="0914f-195">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="0914f-196">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="0914f-196">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="0914f-197">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="0914f-197">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="0914f-198">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="0914f-198">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

