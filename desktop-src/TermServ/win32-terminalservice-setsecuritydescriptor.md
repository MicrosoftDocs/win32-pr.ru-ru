---
title: Метод Сетсекуритидескриптор класса Win32_Service (службы удаленных рабочих столов)
description: Записывает обновленную версию дескриптора безопасности, которая управляет доступом к службе.
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- инструментарий управления Windows (WMI) сценариев, безопасность
- инструментарий управления Windows (WMI) безопасности, написание сценариев
- службы удаленных рабочих столов метода Сетсекуритидескриптор
- Службы удаленных рабочих столов метода Сетсекуритидескриптор, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод Сетсекуритидескриптор
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a21f9730b4c1c0ab7b3ccf662ddb2d95da2ee2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803766"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="d8259-108">Метод Сетсекуритидескриптор класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="d8259-108">SetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="d8259-109">Метод **сетсекуритидескриптор** записывает обновленную версию дескриптора безопасности, которая управляет доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="d8259-109">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8259-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8259-110">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="d8259-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8259-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8259-112">*Дескриптор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8259-112">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8259-113">Дескриптор безопасности, связанный со службой.</span><span class="sxs-lookup"><span data-stu-id="d8259-113">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8259-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8259-114">Return value</span></span>

<span data-ttu-id="d8259-115">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="d8259-115">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="d8259-116">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d8259-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d8259-117">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d8259-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d8259-118">**0**</span><span class="sxs-lookup"><span data-stu-id="d8259-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-119">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="d8259-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-120">**1**</span><span class="sxs-lookup"><span data-stu-id="d8259-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-121">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d8259-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-122">**2**</span><span class="sxs-lookup"><span data-stu-id="d8259-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-123">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="d8259-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-124">**3**</span><span class="sxs-lookup"><span data-stu-id="d8259-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-125">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="d8259-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-126">**4**</span><span class="sxs-lookup"><span data-stu-id="d8259-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-127">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="d8259-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-128">**5**</span><span class="sxs-lookup"><span data-stu-id="d8259-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-129">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="d8259-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-130">**6**</span><span class="sxs-lookup"><span data-stu-id="d8259-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-131">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="d8259-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-132">**7**</span><span class="sxs-lookup"><span data-stu-id="d8259-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-133">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="d8259-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-134">**8**</span><span class="sxs-lookup"><span data-stu-id="d8259-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-135">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="d8259-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-136">**9**</span><span class="sxs-lookup"><span data-stu-id="d8259-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-137">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="d8259-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-138">**10**</span><span class="sxs-lookup"><span data-stu-id="d8259-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-139">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="d8259-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-140">**11**</span><span class="sxs-lookup"><span data-stu-id="d8259-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-141">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="d8259-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-142">**12**</span><span class="sxs-lookup"><span data-stu-id="d8259-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-143">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="d8259-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-144">**13**</span><span class="sxs-lookup"><span data-stu-id="d8259-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-145">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="d8259-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-146">**14**</span><span class="sxs-lookup"><span data-stu-id="d8259-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-147">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="d8259-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-148">**15**</span><span class="sxs-lookup"><span data-stu-id="d8259-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-149">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="d8259-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-150">**16**</span><span class="sxs-lookup"><span data-stu-id="d8259-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-151">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="d8259-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-152">**17**</span><span class="sxs-lookup"><span data-stu-id="d8259-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-153">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="d8259-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-154">**стр**</span><span class="sxs-lookup"><span data-stu-id="d8259-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-155">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="d8259-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-156">**стр**</span><span class="sxs-lookup"><span data-stu-id="d8259-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-157">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="d8259-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-158">**20**</span><span class="sxs-lookup"><span data-stu-id="d8259-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-159">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="d8259-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-160">**открыт**</span><span class="sxs-lookup"><span data-stu-id="d8259-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-161">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="d8259-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-162">**22**</span><span class="sxs-lookup"><span data-stu-id="d8259-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-163">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="d8259-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-164">**23**</span><span class="sxs-lookup"><span data-stu-id="d8259-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-165">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="d8259-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d8259-166">**24**</span><span class="sxs-lookup"><span data-stu-id="d8259-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="d8259-167">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="d8259-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8259-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8259-168">Remarks</span></span>

<span data-ttu-id="d8259-169">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="d8259-169">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="d8259-170">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="d8259-170">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="d8259-171">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="d8259-171">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="d8259-172">Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="d8259-172">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="d8259-173">При вызове этого метода можно обновить списки DACL и SACL в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , но вы также можете обновить только список DACL или только список SACL.</span><span class="sxs-lookup"><span data-stu-id="d8259-173">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="d8259-174">Следующие значения в [**\_ \_ элементе управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) определяют, обновляются ли списки DACL, SACL или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="d8259-174">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="d8259-175">**\_присутствие DACL \_ SE**</span><span class="sxs-lookup"><span data-stu-id="d8259-175">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="d8259-176">Указывает, что список DACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="d8259-176">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="d8259-177">Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение DACL.</span><span class="sxs-lookup"><span data-stu-id="d8259-177">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="d8259-178">**\_имеется список SACL для SE \_**</span><span class="sxs-lookup"><span data-stu-id="d8259-178">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="d8259-179">Указывает, что список SACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="d8259-179">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="d8259-180">Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение списка SACL.</span><span class="sxs-lookup"><span data-stu-id="d8259-180">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="d8259-181">Для обновления списка SACL учетная запись должна иметь права **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="d8259-181">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="d8259-182">Для сценариев имя привилегии — **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="d8259-182">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="d8259-183">Дополнительные сведения см. в разделе [**константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="d8259-183">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="d8259-184">Если доверенное лицо группы и свойства доверенного лица владельца не равны **null**, они обновляются.</span><span class="sxs-lookup"><span data-stu-id="d8259-184">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="d8259-185">В противном случае Инструментарий WMI сохраняет исходные значения.</span><span class="sxs-lookup"><span data-stu-id="d8259-185">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="d8259-186">Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="d8259-186">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="d8259-187">Если в вызове этого метода новый список SACL имеет **значение NULL** , то список SACL дескриптора безопасности на целевом защищаемом объекте остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="d8259-187">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8259-188">Требования</span><span class="sxs-lookup"><span data-stu-id="d8259-188">Requirements</span></span>



| <span data-ttu-id="d8259-189">Требование</span><span class="sxs-lookup"><span data-stu-id="d8259-189">Requirement</span></span> | <span data-ttu-id="d8259-190">Значение</span><span class="sxs-lookup"><span data-stu-id="d8259-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8259-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8259-191">Minimum supported client</span></span><br/> | <span data-ttu-id="d8259-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8259-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8259-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8259-193">Minimum supported server</span></span><br/> | <span data-ttu-id="d8259-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8259-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8259-195">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d8259-195">Namespace</span></span><br/>                | <span data-ttu-id="d8259-196">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d8259-196">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d8259-197">MOF</span><span class="sxs-lookup"><span data-stu-id="d8259-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8259-198"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8259-198"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8259-199">DLL</span><span class="sxs-lookup"><span data-stu-id="d8259-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8259-200"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8259-200"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8259-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8259-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8259-202">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="d8259-202">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="d8259-203">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="d8259-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="d8259-204">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="d8259-204">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="d8259-205">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="d8259-205">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="d8259-206">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="d8259-206">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="d8259-207">Управление учетными записями пользователей и WMI</span><span class="sxs-lookup"><span data-stu-id="d8259-207">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

