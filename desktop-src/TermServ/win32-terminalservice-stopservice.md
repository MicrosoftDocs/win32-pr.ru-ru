---
title: Метод работы класса Win32_Service (Сдоиас. h) (служба терминалов)
description: Помещает службу, представленную объектом Win32 \_ терминалсервице, в остановленном состоянии.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Метод "безслужбы удаленных рабочих столов"
- Метод службы удаленных рабочих столов, Win32_Service класс
- Win32_Service службы удаленных рабочих столов класса, метод "не применять"
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105680134"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a><span data-ttu-id="022ae-106">Метод работы класса Win32_Service (Сдоиас. h) для службы терминалов</span><span class="sxs-lookup"><span data-stu-id="022ae-106">StopService method of the Win32_Service class (Sdoias.h) for the Terminal service</span></span>

<span data-ttu-id="022ae-107">Метод **"** неработающий [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) " помещает службу, представленную объектом [**Win32 \_ терминалсервице**](win32-terminalservice.md) , в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="022ae-107">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_TerminalService**](win32-terminalservice.md) object, in the stopped state.</span></span>

<span data-ttu-id="022ae-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="022ae-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="022ae-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="022ae-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="022ae-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="022ae-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="022ae-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="022ae-111">Parameters</span></span>

<span data-ttu-id="022ae-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="022ae-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="022ae-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="022ae-113">Return value</span></span>

<span data-ttu-id="022ae-114">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="022ae-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="022ae-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="022ae-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="022ae-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="022ae-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="022ae-117">**0**</span><span class="sxs-lookup"><span data-stu-id="022ae-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-118">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="022ae-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-119">**1**</span><span class="sxs-lookup"><span data-stu-id="022ae-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-120">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="022ae-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-121">**2**</span><span class="sxs-lookup"><span data-stu-id="022ae-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="022ae-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-123">**3**</span><span class="sxs-lookup"><span data-stu-id="022ae-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-124">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="022ae-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-125">**4**</span><span class="sxs-lookup"><span data-stu-id="022ae-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="022ae-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-127">**5**</span><span class="sxs-lookup"><span data-stu-id="022ae-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-128">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="022ae-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-129">**6**</span><span class="sxs-lookup"><span data-stu-id="022ae-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-130">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="022ae-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-131">**7**</span><span class="sxs-lookup"><span data-stu-id="022ae-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-132">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="022ae-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-133">**8**</span><span class="sxs-lookup"><span data-stu-id="022ae-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="022ae-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-135">**9**</span><span class="sxs-lookup"><span data-stu-id="022ae-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="022ae-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-137">**10**</span><span class="sxs-lookup"><span data-stu-id="022ae-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="022ae-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-139">**11**</span><span class="sxs-lookup"><span data-stu-id="022ae-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="022ae-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-141">**12**</span><span class="sxs-lookup"><span data-stu-id="022ae-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="022ae-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-143">**13**</span><span class="sxs-lookup"><span data-stu-id="022ae-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="022ae-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-145">**14**</span><span class="sxs-lookup"><span data-stu-id="022ae-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="022ae-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-147">**15**</span><span class="sxs-lookup"><span data-stu-id="022ae-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="022ae-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-149">**16**</span><span class="sxs-lookup"><span data-stu-id="022ae-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="022ae-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-151">**17**</span><span class="sxs-lookup"><span data-stu-id="022ae-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="022ae-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="022ae-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="022ae-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="022ae-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="022ae-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-157">**20**</span><span class="sxs-lookup"><span data-stu-id="022ae-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="022ae-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-159">**открыт**</span><span class="sxs-lookup"><span data-stu-id="022ae-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-160">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="022ae-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-161">**22**</span><span class="sxs-lookup"><span data-stu-id="022ae-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-162">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="022ae-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-163">**23**</span><span class="sxs-lookup"><span data-stu-id="022ae-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-164">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="022ae-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="022ae-165">**24**</span><span class="sxs-lookup"><span data-stu-id="022ae-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="022ae-166">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="022ae-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="022ae-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="022ae-167">Remarks</span></span>

<span data-ttu-id="022ae-168">Определив, какие службы могут быть остановлены или приостановлены, можно использовать **методы "** [**PauseService**](win32-terminalservice-pauseservice.md) " и "приостановить" для остановки и приостановки служб.</span><span class="sxs-lookup"><span data-stu-id="022ae-168">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](win32-terminalservice-pauseservice.md) methods to stop and pause services.</span></span> <span data-ttu-id="022ae-169">Решение о прекращении работы службы, а не приостановке или наоборот, зависит от нескольких факторов, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="022ae-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="022ae-170">Может ли служба быть приостановлена?</span><span class="sxs-lookup"><span data-stu-id="022ae-170">Is the service capable of being paused?</span></span> <span data-ttu-id="022ae-171">В противном случае единственным вариантом будет «останавливает службу».</span><span class="sxs-lookup"><span data-stu-id="022ae-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="022ae-172">Нужно ли продолжать обработку запросов клиентов для всех, кто уже подключен к службе?</span><span class="sxs-lookup"><span data-stu-id="022ae-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="022ae-173">Если да, то приостановка службы обычно позволяет ей управлять существующими клиентами при запрете доступа к новым клиентам.</span><span class="sxs-lookup"><span data-stu-id="022ae-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="022ae-174">Напротив, при прекращении службы все клиенты сразу же отключаются.</span><span class="sxs-lookup"><span data-stu-id="022ae-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="022ae-175">Нужно ли перенастроить службу, чтобы изменения вступили в силу немедленно?</span><span class="sxs-lookup"><span data-stu-id="022ae-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="022ae-176">Несмотря на то, что свойства службы могут быть изменены, пока служба приостановлена, большинство из них не вступают в силу, пока служба не будет остановлена и перезапущена.</span><span class="sxs-lookup"><span data-stu-id="022ae-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="022ae-177">Код скрипта, необходимый для остановки службы, почти идентичен коду, требуемому для приостановки службы.</span><span class="sxs-lookup"><span data-stu-id="022ae-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="022ae-178">При попытке отключить службу, для которой выполняются зависимые службы **, метод «не работает» возвращает** значение 3.</span><span class="sxs-lookup"><span data-stu-id="022ae-178">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="022ae-179">Сначала необходимо остановить зависимые службы.</span><span class="sxs-lookup"><span data-stu-id="022ae-179">The dependent services must be stopped first.</span></span>

<span data-ttu-id="022ae-180">Если служба останавливается, сразу же проверьте [**\_ терминалсервице Win32**](win32-terminalservice.md).**State** , так как значение по-прежнему может отображать службу как выполняющуюся.</span><span class="sxs-lookup"><span data-stu-id="022ae-180">If you stop a service, then immediately check the [**Win32\_TerminalService**](win32-terminalservice.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="022ae-181">Примеры</span><span class="sxs-lookup"><span data-stu-id="022ae-181">Examples</span></span>

<span data-ttu-id="022ae-182">[Set-ремотесервице](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) Образец PowerShell задает состояние службы для удаленных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="022ae-182">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="022ae-183">При [остановке службы и ее зависимых](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) примеров VBScript останавливается служба и все зависимые службы.</span><span class="sxs-lookup"><span data-stu-id="022ae-183">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

## <a name="requirements"></a><span data-ttu-id="022ae-184">Требования</span><span class="sxs-lookup"><span data-stu-id="022ae-184">Requirements</span></span>



| <span data-ttu-id="022ae-185">Требование</span><span class="sxs-lookup"><span data-stu-id="022ae-185">Requirement</span></span> | <span data-ttu-id="022ae-186">Значение</span><span class="sxs-lookup"><span data-stu-id="022ae-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="022ae-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="022ae-187">Minimum supported client</span></span><br/> | <span data-ttu-id="022ae-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="022ae-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="022ae-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="022ae-189">Minimum supported server</span></span><br/> | <span data-ttu-id="022ae-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="022ae-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="022ae-191">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="022ae-191">Namespace</span></span><br/>                | <span data-ttu-id="022ae-192">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="022ae-192">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="022ae-193">Header</span><span class="sxs-lookup"><span data-stu-id="022ae-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="022ae-194"><dt>Сдоиас. h</dt></span><span class="sxs-lookup"><span data-stu-id="022ae-194"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="022ae-195">MOF</span><span class="sxs-lookup"><span data-stu-id="022ae-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="022ae-196"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="022ae-196"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="022ae-197">DLL</span><span class="sxs-lookup"><span data-stu-id="022ae-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="022ae-198"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="022ae-198"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="022ae-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="022ae-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022ae-200">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="022ae-200">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="022ae-201">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="022ae-201">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="022ae-202">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="022ae-202">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="022ae-203">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="022ae-203">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="022ae-204">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="022ae-204">**PauseService**</span></span>](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

