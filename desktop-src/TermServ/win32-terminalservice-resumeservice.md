---
title: Метод ResumeService класса Win32_Service (службы удаленных рабочих столов)
description: Пытается поместить службу, на которую указывает ссылка, в состоянии возобновления.
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ResumeService
- Службы удаленных рабочих столов метода ResumeService, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод ResumeService
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7b446dea84e4320e9aa8972a88dc4fdd5a6eea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535207"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="5784a-106">Метод ResumeService класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="5784a-106">ResumeService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="5784a-107">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ResumeService пытается поместить службу, на которую указывает ссылка, в состоянии возобновления.</span><span class="sxs-lookup"><span data-stu-id="5784a-107">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="5784a-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="5784a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5784a-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5784a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5784a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5784a-110">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="5784a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5784a-111">Parameters</span></span>

<span data-ttu-id="5784a-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5784a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5784a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5784a-113">Return value</span></span>

<span data-ttu-id="5784a-114">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="5784a-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="5784a-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5784a-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5784a-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5784a-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5784a-117">**0**</span><span class="sxs-lookup"><span data-stu-id="5784a-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-118">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="5784a-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-119">**1**</span><span class="sxs-lookup"><span data-stu-id="5784a-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-120">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5784a-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-121">**2**</span><span class="sxs-lookup"><span data-stu-id="5784a-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="5784a-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-123">**3**</span><span class="sxs-lookup"><span data-stu-id="5784a-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-124">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="5784a-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-125">**4**</span><span class="sxs-lookup"><span data-stu-id="5784a-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="5784a-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-127">**5**</span><span class="sxs-lookup"><span data-stu-id="5784a-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-128">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="5784a-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-129">**6**</span><span class="sxs-lookup"><span data-stu-id="5784a-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-130">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="5784a-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-131">**7**</span><span class="sxs-lookup"><span data-stu-id="5784a-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-132">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="5784a-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-133">**8**</span><span class="sxs-lookup"><span data-stu-id="5784a-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="5784a-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-135">**9**</span><span class="sxs-lookup"><span data-stu-id="5784a-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="5784a-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-137">**10**</span><span class="sxs-lookup"><span data-stu-id="5784a-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="5784a-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-139">**11**</span><span class="sxs-lookup"><span data-stu-id="5784a-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="5784a-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-141">**12**</span><span class="sxs-lookup"><span data-stu-id="5784a-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="5784a-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-143">**13**</span><span class="sxs-lookup"><span data-stu-id="5784a-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="5784a-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-145">**14**</span><span class="sxs-lookup"><span data-stu-id="5784a-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="5784a-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-147">**15**</span><span class="sxs-lookup"><span data-stu-id="5784a-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="5784a-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-149">**16**</span><span class="sxs-lookup"><span data-stu-id="5784a-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="5784a-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-151">**17**</span><span class="sxs-lookup"><span data-stu-id="5784a-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="5784a-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="5784a-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="5784a-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="5784a-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="5784a-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-157">**20**</span><span class="sxs-lookup"><span data-stu-id="5784a-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="5784a-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-159">**открыт**</span><span class="sxs-lookup"><span data-stu-id="5784a-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-160">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="5784a-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-161">**22**</span><span class="sxs-lookup"><span data-stu-id="5784a-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-162">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="5784a-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-163">**23**</span><span class="sxs-lookup"><span data-stu-id="5784a-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-164">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="5784a-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5784a-165">**24**</span><span class="sxs-lookup"><span data-stu-id="5784a-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="5784a-166">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="5784a-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5784a-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5784a-167">Remarks</span></span>

<span data-ttu-id="5784a-168">Хотя может показаться, что непрактичное различие между остановленной службой и приостановленной службой, два состояния по-разному отображаются в SCM.</span><span class="sxs-lookup"><span data-stu-id="5784a-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="5784a-169">Остановленная служба — это служба, которая не запущена и должна проходить всю процедуру запуска службы.</span><span class="sxs-lookup"><span data-stu-id="5784a-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="5784a-170">Однако Приостановленная служба все еще работает, но ее работа приостановлена.</span><span class="sxs-lookup"><span data-stu-id="5784a-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="5784a-171">По этой причине Приостановленная служба не обязана проходить всю процедуру запуска службы, но для ее возобновления требуется другая процедура.</span><span class="sxs-lookup"><span data-stu-id="5784a-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="5784a-172">Необходимо использовать правильный метод для запуска остановленной службы или возобновления работы приостановленной службы.</span><span class="sxs-lookup"><span data-stu-id="5784a-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="5784a-173">Методы [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) [**StartService**](win32-terminalservice-startservice.md) и **ResumeService** следует использовать в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="5784a-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods [**StartService**](win32-terminalservice-startservice.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="5784a-174">Если служба в данный момент остановлена, для ее перезапуска необходимо использовать метод [**StartService**](win32-terminalservice-startservice.md) . **ResumeService** не может запустить службу, которая в данный момент остановлена.</span><span class="sxs-lookup"><span data-stu-id="5784a-174">If a service is currently stopped, you must use the [**StartService**](win32-terminalservice-startservice.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="5784a-175">Если служба приостановлена, необходимо использовать **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="5784a-175">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="5784a-176">При использовании метода [**StartService**](win32-terminalservice-startservice.md) в приостановленной службе появляется сообщение "служба уже запущена".</span><span class="sxs-lookup"><span data-stu-id="5784a-176">If you use the [**StartService**](win32-terminalservice-startservice.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="5784a-177">Однако служба остается приостановленной до тех пор, пока в нее не будет отправлен код управления службой возобновления.</span><span class="sxs-lookup"><span data-stu-id="5784a-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="5784a-178">Примеры</span><span class="sxs-lookup"><span data-stu-id="5784a-178">Examples</span></span>

<span data-ttu-id="5784a-179">В [службах возобновления работы, приостановленных](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) с помощью VBScript, перезапускаются все приостановленные службы автозапуска.</span><span class="sxs-lookup"><span data-stu-id="5784a-179">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

## <a name="requirements"></a><span data-ttu-id="5784a-180">Требования</span><span class="sxs-lookup"><span data-stu-id="5784a-180">Requirements</span></span>



| <span data-ttu-id="5784a-181">Требование</span><span class="sxs-lookup"><span data-stu-id="5784a-181">Requirement</span></span> | <span data-ttu-id="5784a-182">Значение</span><span class="sxs-lookup"><span data-stu-id="5784a-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5784a-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5784a-183">Minimum supported client</span></span><br/> | <span data-ttu-id="5784a-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5784a-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5784a-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5784a-185">Minimum supported server</span></span><br/> | <span data-ttu-id="5784a-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5784a-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5784a-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5784a-187">Namespace</span></span><br/>                | <span data-ttu-id="5784a-188">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="5784a-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5784a-189">MOF</span><span class="sxs-lookup"><span data-stu-id="5784a-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5784a-190"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5784a-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5784a-191">DLL</span><span class="sxs-lookup"><span data-stu-id="5784a-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5784a-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5784a-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5784a-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5784a-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5784a-194">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="5784a-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="5784a-195">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="5784a-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="5784a-196">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="5784a-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="5784a-197">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="5784a-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

