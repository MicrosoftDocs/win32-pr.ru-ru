---
title: Метод PauseService класса Win32_Service (службы удаленных рабочих столов)
description: Пытается перевести службу в состояние приостановки.
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода PauseService
- Службы удаленных рабочих столов метода PauseService, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод PauseService
topic_type:
- apiref
api_name:
- Win32_Service.PauseService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69951a77530b3aff89148b08e19f3a7c4da8f5b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672567"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="ff2f3-106">Метод PauseService класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="ff2f3-106">PauseService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="ff2f3-107">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) PauseService пытается перевести службу в приостановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-107">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="ff2f3-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ff2f3-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ff2f3-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ff2f3-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff2f3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff2f3-110">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="ff2f3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff2f3-111">Parameters</span></span>

<span data-ttu-id="ff2f3-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff2f3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff2f3-113">Return value</span></span>

<span data-ttu-id="ff2f3-114">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="ff2f3-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ff2f3-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ff2f3-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ff2f3-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ff2f3-117">**0**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-118">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-119">**1**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-120">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-121">**2**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-123">**3**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-124">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-125">**4**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-127">**5**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-128">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-129">**6**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-130">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-131">**7**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-132">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-133">**8**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-135">**9**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-137">**10**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-139">**11**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-141">**12**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-143">**13**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-145">**14**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-147">**15**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-149">**16**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-151">**17**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-157">**20**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-159">**открыт**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-160">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-161">**22**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-162">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-163">**23**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-164">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ff2f3-165">**24**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ff2f3-166">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff2f3-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff2f3-167">Remarks</span></span>

<span data-ttu-id="ff2f3-168">Определив, какие службы могут быть остановлены или приостановлены, можно использовать [**методы "**](win32-terminalservice-stopservice.md) **PauseService** " и "приостановить" для остановки и приостановки служб.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-168">After you have determined which services can be stopped or paused, you can use the [**StopService**](win32-terminalservice-stopservice.md) and **PauseService** methods to stop and pause services.</span></span> <span data-ttu-id="ff2f3-169">Решение о прекращении работы службы, а не приостановке или наоборот, зависит от нескольких факторов, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="ff2f3-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="ff2f3-170">Может ли служба быть приостановлена?</span><span class="sxs-lookup"><span data-stu-id="ff2f3-170">Is the service capable of being paused?</span></span> <span data-ttu-id="ff2f3-171">В противном случае единственным вариантом будет «останавливает службу».</span><span class="sxs-lookup"><span data-stu-id="ff2f3-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="ff2f3-172">Нужно ли продолжать обработку запросов клиентов для всех, кто уже подключен к службе?</span><span class="sxs-lookup"><span data-stu-id="ff2f3-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="ff2f3-173">Если да, то приостановка службы обычно позволяет ей управлять существующими клиентами при запрете доступа к новым клиентам.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="ff2f3-174">Напротив, при прекращении службы все клиенты сразу же отключаются.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="ff2f3-175">Нужно ли перенастроить службу, чтобы изменения вступили в силу немедленно?</span><span class="sxs-lookup"><span data-stu-id="ff2f3-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="ff2f3-176">Несмотря на то, что свойства службы могут быть изменены, пока служба приостановлена, большинство из них не вступают в силу, пока служба не будет остановлена и перезапущена.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="ff2f3-177">Код скрипта, необходимый для остановки службы, почти идентичен коду, требуемому для приостановки службы.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="ff2f3-178">Примеры</span><span class="sxs-lookup"><span data-stu-id="ff2f3-178">Examples</span></span>

<span data-ttu-id="ff2f3-179">[Службы Pause, работающие под заданной учетной записью](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) , приостанавливают все службы, работающие под гипотетической учетной записью службы нетсвк.</span><span class="sxs-lookup"><span data-stu-id="ff2f3-179">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account Netsvc.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff2f3-180">Требования</span><span class="sxs-lookup"><span data-stu-id="ff2f3-180">Requirements</span></span>



| <span data-ttu-id="ff2f3-181">Требование</span><span class="sxs-lookup"><span data-stu-id="ff2f3-181">Requirement</span></span> | <span data-ttu-id="ff2f3-182">Значение</span><span class="sxs-lookup"><span data-stu-id="ff2f3-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff2f3-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff2f3-183">Minimum supported client</span></span><br/> | <span data-ttu-id="ff2f3-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff2f3-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff2f3-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff2f3-185">Minimum supported server</span></span><br/> | <span data-ttu-id="ff2f3-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff2f3-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff2f3-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ff2f3-187">Namespace</span></span><br/>                | <span data-ttu-id="ff2f3-188">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="ff2f3-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ff2f3-189">MOF</span><span class="sxs-lookup"><span data-stu-id="ff2f3-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff2f3-190"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff2f3-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff2f3-191">DLL</span><span class="sxs-lookup"><span data-stu-id="ff2f3-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff2f3-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff2f3-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff2f3-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff2f3-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff2f3-194">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="ff2f3-195">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="ff2f3-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="ff2f3-196">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="ff2f3-197">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="ff2f3-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="ff2f3-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="ff2f3-198">**StopService**</span></span>](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

