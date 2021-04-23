---
description: Записывает обновленную версию дескриптора безопасности, которая управляет доступом к службе.
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: Метод Сетсекуритидескриптор класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82c08f9c560a1d8e419d9a8f6474f8ea9db4e541
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656066"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="1dfdf-103">Метод Сетсекуритидескриптор класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="1dfdf-103">SetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1dfdf-104">Метод **сетсекуритидескриптор** записывает обновленную версию дескриптора безопасности, которая управляет доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dfdf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dfdf-105">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="1dfdf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1dfdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfdf-107">*Дескриптор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1dfdf-107">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-108">Дескриптор безопасности, связанный со службой.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-108">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfdf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1dfdf-109">Return value</span></span>

<span data-ttu-id="1dfdf-110">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-110">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="1dfdf-111">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1dfdf-111">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1dfdf-112">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1dfdf-112">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1dfdf-113">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-113">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-114">0</span><span class="sxs-lookup"><span data-stu-id="1dfdf-114">0</span></span>

<span data-ttu-id="1dfdf-115">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-116">**1**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-118">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-118">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-119">2</span><span class="sxs-lookup"><span data-stu-id="1dfdf-119">2</span></span>

<span data-ttu-id="1dfdf-120">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-121">**3**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-122">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-123">**4**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-124">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-125">**5**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-126">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-127">**6**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-128">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-129">**7**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-130">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-131">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-132">8</span><span class="sxs-lookup"><span data-stu-id="1dfdf-132">8</span></span>

<span data-ttu-id="1dfdf-133">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-133">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-134">**Отсутствует привилегия**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-134">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-135">9</span><span class="sxs-lookup"><span data-stu-id="1dfdf-135">9</span></span>

<span data-ttu-id="1dfdf-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-137">**10**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-139">**11**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-141">**12**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-143">**13**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-145">**14**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-147">**15**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-149">**16**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-151">**17**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-157">**20**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-159">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-159">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-160">21</span><span class="sxs-lookup"><span data-stu-id="1dfdf-160">21</span></span>

<span data-ttu-id="1dfdf-161">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-162">**22**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-163">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-164">**23**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-165">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-166">**24**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-167">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-167">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="1dfdf-168">**Другое**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-168">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1dfdf-169">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="1dfdf-169">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1dfdf-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1dfdf-170">Remarks</span></span>

<span data-ttu-id="1dfdf-171">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="1dfdf-171">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="1dfdf-172">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="1dfdf-172">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="1dfdf-173">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-173">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="1dfdf-174">Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="1dfdf-174">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="1dfdf-175">При вызове этого метода можно обновить списки DACL и SACL в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , но вы также можете обновить только список DACL или только список SACL.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-175">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="1dfdf-176">Следующие значения в [**\_ \_ элементе управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) определяют, обновляются ли списки DACL, SACL или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-176">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="1dfdf-177">**\_присутствие DACL \_ SE**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-177">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="1dfdf-178">Указывает, что список DACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-178">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="1dfdf-179">Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение DACL.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-179">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="1dfdf-180">**\_имеется список SACL для SE \_**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-180">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="1dfdf-181">Указывает, что список SACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-181">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="1dfdf-182">Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение списка SACL.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-182">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="1dfdf-183">Для обновления списка SACL учетная запись должна иметь права **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="1dfdf-183">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="1dfdf-184">Для сценариев имя привилегии — **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-184">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="1dfdf-185">Дополнительные сведения см. в разделе [**константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="1dfdf-185">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="1dfdf-186">Если доверенное лицо группы и свойства доверенного лица владельца не равны **null**, они обновляются.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-186">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="1dfdf-187">В противном случае Инструментарий WMI сохраняет исходные значения.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-187">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="1dfdf-188">Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="1dfdf-188">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="1dfdf-189">Если в вызове этого метода новый список SACL имеет **значение NULL** , то список SACL дескриптора безопасности на целевом защищаемом объекте остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="1dfdf-189">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfdf-190">Требования</span><span class="sxs-lookup"><span data-stu-id="1dfdf-190">Requirements</span></span>



| <span data-ttu-id="1dfdf-191">Требование</span><span class="sxs-lookup"><span data-stu-id="1dfdf-191">Requirement</span></span> | <span data-ttu-id="1dfdf-192">Значение</span><span class="sxs-lookup"><span data-stu-id="1dfdf-192">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfdf-193">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1dfdf-193">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfdf-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1dfdf-194">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1dfdf-195">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1dfdf-195">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfdf-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dfdf-196">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1dfdf-197">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1dfdf-197">Namespace</span></span><br/>                | <span data-ttu-id="1dfdf-198">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1dfdf-198">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1dfdf-199">MOF</span><span class="sxs-lookup"><span data-stu-id="1dfdf-199">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dfdf-200"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1dfdf-200"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dfdf-201">DLL</span><span class="sxs-lookup"><span data-stu-id="1dfdf-201">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dfdf-202"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dfdf-202"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfdf-203">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dfdf-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfdf-204">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-204">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="1dfdf-205">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="1dfdf-205">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="1dfdf-206">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="1dfdf-206">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="1dfdf-207">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="1dfdf-207">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="1dfdf-208">Управление учетными записями пользователей и WMI</span><span class="sxs-lookup"><span data-stu-id="1dfdf-208">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

