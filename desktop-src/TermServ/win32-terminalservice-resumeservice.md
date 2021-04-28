---
title: Метод ResumeService класса Win32_Service (службы удаленных рабочих столов)
description: Метод ResumeService класса Win32_Service (службы удаленных рабочих столов) — пытается поместить службу, на которую указывает ссылка, в состоянии возобновления.
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
ms.openlocfilehash: 94f8e7dcfc9b9bd5b408e36d8a909aa10c84519c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090592"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="68197-106">Метод ResumeService класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="68197-106">ResumeService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="68197-107">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ResumeService пытается поместить службу, на которую указывает ссылка, в состоянии возобновления.</span><span class="sxs-lookup"><span data-stu-id="68197-107">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="68197-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="68197-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="68197-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="68197-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="68197-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68197-110">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="68197-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="68197-111">Parameters</span></span>

<span data-ttu-id="68197-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="68197-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68197-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68197-113">Return value</span></span>

<span data-ttu-id="68197-114">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="68197-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="68197-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="68197-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="68197-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="68197-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="68197-117">**0**</span><span class="sxs-lookup"><span data-stu-id="68197-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="68197-118">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="68197-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="68197-119">**1**</span><span class="sxs-lookup"><span data-stu-id="68197-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="68197-120">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="68197-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="68197-121">**2**</span><span class="sxs-lookup"><span data-stu-id="68197-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="68197-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="68197-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="68197-123">**3**</span><span class="sxs-lookup"><span data-stu-id="68197-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="68197-124">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="68197-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="68197-125">**4**</span><span class="sxs-lookup"><span data-stu-id="68197-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="68197-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="68197-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="68197-127">**5**</span><span class="sxs-lookup"><span data-stu-id="68197-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="68197-128">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="68197-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="68197-129">**6**</span><span class="sxs-lookup"><span data-stu-id="68197-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="68197-130">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="68197-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="68197-131">**7**</span><span class="sxs-lookup"><span data-stu-id="68197-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="68197-132">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="68197-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="68197-133">**8**</span><span class="sxs-lookup"><span data-stu-id="68197-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="68197-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="68197-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="68197-135">**9**</span><span class="sxs-lookup"><span data-stu-id="68197-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="68197-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="68197-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="68197-137">**10**</span><span class="sxs-lookup"><span data-stu-id="68197-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="68197-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="68197-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="68197-139">**11**</span><span class="sxs-lookup"><span data-stu-id="68197-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="68197-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="68197-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="68197-141">**12**</span><span class="sxs-lookup"><span data-stu-id="68197-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="68197-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="68197-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="68197-143">**13**</span><span class="sxs-lookup"><span data-stu-id="68197-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="68197-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="68197-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="68197-145">**14**</span><span class="sxs-lookup"><span data-stu-id="68197-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="68197-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="68197-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="68197-147">**15**</span><span class="sxs-lookup"><span data-stu-id="68197-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="68197-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="68197-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="68197-149">**16**</span><span class="sxs-lookup"><span data-stu-id="68197-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="68197-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="68197-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="68197-151">**17**</span><span class="sxs-lookup"><span data-stu-id="68197-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="68197-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="68197-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="68197-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="68197-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="68197-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="68197-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="68197-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="68197-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="68197-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="68197-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="68197-157">**20**</span><span class="sxs-lookup"><span data-stu-id="68197-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="68197-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="68197-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="68197-159">**открыт**</span><span class="sxs-lookup"><span data-stu-id="68197-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="68197-160">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="68197-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="68197-161">**22**</span><span class="sxs-lookup"><span data-stu-id="68197-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="68197-162">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="68197-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="68197-163">**23**</span><span class="sxs-lookup"><span data-stu-id="68197-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="68197-164">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="68197-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="68197-165">**24**</span><span class="sxs-lookup"><span data-stu-id="68197-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="68197-166">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="68197-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68197-167">Remarks</span><span class="sxs-lookup"><span data-stu-id="68197-167">Remarks</span></span>

<span data-ttu-id="68197-168">Хотя может показаться, что непрактичное различие между остановленной службой и приостановленной службой, два состояния по-разному отображаются в SCM.</span><span class="sxs-lookup"><span data-stu-id="68197-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="68197-169">Остановленная служба — это служба, которая не запущена и должна проходить всю процедуру запуска службы.</span><span class="sxs-lookup"><span data-stu-id="68197-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="68197-170">Однако Приостановленная служба все еще работает, но ее работа приостановлена.</span><span class="sxs-lookup"><span data-stu-id="68197-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="68197-171">По этой причине Приостановленная служба не обязана проходить всю процедуру запуска службы, но для ее возобновления требуется другая процедура.</span><span class="sxs-lookup"><span data-stu-id="68197-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="68197-172">Необходимо использовать правильный метод для запуска остановленной службы или возобновления работы приостановленной службы.</span><span class="sxs-lookup"><span data-stu-id="68197-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="68197-173">Методы [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) [**StartService**](win32-terminalservice-startservice.md) и **ResumeService** следует использовать в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="68197-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods [**StartService**](win32-terminalservice-startservice.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="68197-174">Если служба в данный момент остановлена, для ее перезапуска необходимо использовать метод [**StartService**](win32-terminalservice-startservice.md) . **ResumeService** не может запустить службу, которая в данный момент остановлена.</span><span class="sxs-lookup"><span data-stu-id="68197-174">If a service is currently stopped, you must use the [**StartService**](win32-terminalservice-startservice.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="68197-175">Если служба приостановлена, необходимо использовать **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="68197-175">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="68197-176">При использовании метода [**StartService**](win32-terminalservice-startservice.md) в приостановленной службе появляется сообщение "служба уже запущена".</span><span class="sxs-lookup"><span data-stu-id="68197-176">If you use the [**StartService**](win32-terminalservice-startservice.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="68197-177">Однако служба остается приостановленной до тех пор, пока в нее не будет отправлен код управления службой возобновления.</span><span class="sxs-lookup"><span data-stu-id="68197-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="68197-178">Примеры</span><span class="sxs-lookup"><span data-stu-id="68197-178">Examples</span></span>

<span data-ttu-id="68197-179">В [службах возобновления работы, приостановленных](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) с помощью VBScript, перезапускаются все приостановленные службы автозапуска.</span><span class="sxs-lookup"><span data-stu-id="68197-179">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

## <a name="requirements"></a><span data-ttu-id="68197-180">Требования</span><span class="sxs-lookup"><span data-stu-id="68197-180">Requirements</span></span>



| <span data-ttu-id="68197-181">Требование</span><span class="sxs-lookup"><span data-stu-id="68197-181">Requirement</span></span> | <span data-ttu-id="68197-182">Значение</span><span class="sxs-lookup"><span data-stu-id="68197-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68197-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68197-183">Minimum supported client</span></span><br/> | <span data-ttu-id="68197-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68197-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68197-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68197-185">Minimum supported server</span></span><br/> | <span data-ttu-id="68197-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68197-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68197-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="68197-187">Namespace</span></span><br/>                | <span data-ttu-id="68197-188">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="68197-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="68197-189">MOF</span><span class="sxs-lookup"><span data-stu-id="68197-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68197-190"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68197-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="68197-191">DLL</span><span class="sxs-lookup"><span data-stu-id="68197-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68197-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68197-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68197-193">См. также</span><span class="sxs-lookup"><span data-stu-id="68197-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68197-194">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="68197-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="68197-195">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="68197-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="68197-196">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="68197-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="68197-197">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="68197-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

