---
title: Метод Жетсекуритидескриптор класса Win32_Service (службы удаленных рабочих столов)
description: Возвращает дескриптор безопасности, управляющий доступом к службе.
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- инструментарий управления Windows (WMI) сценариев, безопасность
- инструментарий управления Windows (WMI) безопасности, написание сценариев
- службы удаленных рабочих столов метода Жетсекуритидескриптор
- Службы удаленных рабочих столов метода Жетсекуритидескриптор, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод Жетсекуритидескриптор
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8dc271d5498163352af10bcb0b9c55e2e81fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988513"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="c2874-108">Метод Жетсекуритидескриптор класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="c2874-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="c2874-109">Метод **жетсекуритидескриптор** возвращает дескриптор безопасности, который управляет доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="c2874-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="c2874-110">Дескриптор возвращается в виде экземпляра [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="c2874-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2874-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2874-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="c2874-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2874-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2874-113">*Дескриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c2874-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2874-114">Дескриптор безопасности, связанный со службой.</span><span class="sxs-lookup"><span data-stu-id="c2874-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2874-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2874-115">Return value</span></span>

<span data-ttu-id="c2874-116">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c2874-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="c2874-117">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c2874-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c2874-118">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c2874-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c2874-119">**0**</span><span class="sxs-lookup"><span data-stu-id="c2874-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-120">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="c2874-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-121">**1**</span><span class="sxs-lookup"><span data-stu-id="c2874-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-122">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c2874-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-123">**2**</span><span class="sxs-lookup"><span data-stu-id="c2874-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-124">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c2874-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-125">**3**</span><span class="sxs-lookup"><span data-stu-id="c2874-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-126">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="c2874-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-127">**4**</span><span class="sxs-lookup"><span data-stu-id="c2874-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-128">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="c2874-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-129">**5**</span><span class="sxs-lookup"><span data-stu-id="c2874-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-130">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="c2874-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-131">**6**</span><span class="sxs-lookup"><span data-stu-id="c2874-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-132">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="c2874-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-133">**7**</span><span class="sxs-lookup"><span data-stu-id="c2874-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-134">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="c2874-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-135">**8**</span><span class="sxs-lookup"><span data-stu-id="c2874-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-136">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="c2874-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-137">**9**</span><span class="sxs-lookup"><span data-stu-id="c2874-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-138">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="c2874-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-139">**10**</span><span class="sxs-lookup"><span data-stu-id="c2874-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-140">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="c2874-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-141">**11**</span><span class="sxs-lookup"><span data-stu-id="c2874-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-142">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="c2874-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-143">**12**</span><span class="sxs-lookup"><span data-stu-id="c2874-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-144">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="c2874-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-145">**13**</span><span class="sxs-lookup"><span data-stu-id="c2874-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-146">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="c2874-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-147">**14**</span><span class="sxs-lookup"><span data-stu-id="c2874-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-148">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="c2874-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-149">**15**</span><span class="sxs-lookup"><span data-stu-id="c2874-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-150">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="c2874-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-151">**16**</span><span class="sxs-lookup"><span data-stu-id="c2874-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-152">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="c2874-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-153">**17**</span><span class="sxs-lookup"><span data-stu-id="c2874-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-154">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="c2874-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="c2874-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-156">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="c2874-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-157">**стр**</span><span class="sxs-lookup"><span data-stu-id="c2874-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-158">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="c2874-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-159">**20**</span><span class="sxs-lookup"><span data-stu-id="c2874-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-160">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="c2874-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-161">**открыт**</span><span class="sxs-lookup"><span data-stu-id="c2874-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-162">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="c2874-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-163">**22**</span><span class="sxs-lookup"><span data-stu-id="c2874-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-164">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="c2874-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-165">**23**</span><span class="sxs-lookup"><span data-stu-id="c2874-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-166">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="c2874-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c2874-167">**24**</span><span class="sxs-lookup"><span data-stu-id="c2874-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c2874-168">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="c2874-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2874-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2874-169">Remarks</span></span>

<span data-ttu-id="c2874-170">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="c2874-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="c2874-171">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="c2874-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="c2874-172">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="c2874-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="c2874-173">Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="c2874-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="c2874-174">Примеры</span><span class="sxs-lookup"><span data-stu-id="c2874-174">Examples</span></span>

<span data-ttu-id="c2874-175">При получении дескриптора безопасности в VBScript обязательно выполните команду "безопасность" и запустите от имени администратора, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="c2874-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="c2874-176">В противном случае код может вызвать ошибку разрешений.</span><span class="sxs-lookup"><span data-stu-id="c2874-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="c2874-177">Аналогичным образом в VB.NET обязательно установите значение "Енаблепривилежес = true" и запустите приложение от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="c2874-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="c2874-178">Требования</span><span class="sxs-lookup"><span data-stu-id="c2874-178">Requirements</span></span>



| <span data-ttu-id="c2874-179">Требование</span><span class="sxs-lookup"><span data-stu-id="c2874-179">Requirement</span></span> | <span data-ttu-id="c2874-180">Значение</span><span class="sxs-lookup"><span data-stu-id="c2874-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2874-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2874-181">Minimum supported client</span></span><br/> | <span data-ttu-id="c2874-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2874-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2874-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2874-183">Minimum supported server</span></span><br/> | <span data-ttu-id="c2874-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2874-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2874-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c2874-185">Namespace</span></span><br/>                | <span data-ttu-id="c2874-186">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c2874-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c2874-187">MOF</span><span class="sxs-lookup"><span data-stu-id="c2874-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2874-188"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2874-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2874-189">DLL</span><span class="sxs-lookup"><span data-stu-id="c2874-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2874-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2874-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2874-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2874-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2874-192">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="c2874-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="c2874-193">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="c2874-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="c2874-194">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="c2874-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="c2874-195">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="c2874-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="c2874-196">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="c2874-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="c2874-197">Управление учетными записями пользователей и WMI</span><span class="sxs-lookup"><span data-stu-id="c2874-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

