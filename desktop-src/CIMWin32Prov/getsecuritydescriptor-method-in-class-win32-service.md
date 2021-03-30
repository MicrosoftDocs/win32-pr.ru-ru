---
description: Возвращает дескриптор безопасности, управляющий доступом к службе.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Метод Жетсекуритидескриптор класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072411"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="3df10-103">Метод Жетсекуритидескриптор класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3df10-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3df10-104">Метод **жетсекуритидескриптор** возвращает дескриптор безопасности, который управляет доступом к службе.</span><span class="sxs-lookup"><span data-stu-id="3df10-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="3df10-105">Дескриптор возвращается в виде экземпляра [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="3df10-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="3df10-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3df10-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="3df10-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3df10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df10-108">*Дескриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3df10-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3df10-109">Дескриптор безопасности, связанный со службой.</span><span class="sxs-lookup"><span data-stu-id="3df10-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df10-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3df10-110">Return value</span></span>

<span data-ttu-id="3df10-111">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="3df10-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="3df10-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3df10-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3df10-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3df10-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3df10-114">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="3df10-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3df10-115">0</span><span class="sxs-lookup"><span data-stu-id="3df10-115">0</span></span>

<span data-ttu-id="3df10-116">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="3df10-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-117">1</span><span class="sxs-lookup"><span data-stu-id="3df10-117">1</span></span>

<span data-ttu-id="3df10-118">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3df10-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3df10-119">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="3df10-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3df10-120">2</span><span class="sxs-lookup"><span data-stu-id="3df10-120">2</span></span>

<span data-ttu-id="3df10-121">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="3df10-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-122">3</span><span class="sxs-lookup"><span data-stu-id="3df10-122">3</span></span>

<span data-ttu-id="3df10-123">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="3df10-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-124">4</span><span class="sxs-lookup"><span data-stu-id="3df10-124">4</span></span>

<span data-ttu-id="3df10-125">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="3df10-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-126">5</span><span class="sxs-lookup"><span data-stu-id="3df10-126">5</span></span>

<span data-ttu-id="3df10-127">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="3df10-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-128">6</span><span class="sxs-lookup"><span data-stu-id="3df10-128">6</span></span>

<span data-ttu-id="3df10-129">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="3df10-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-130">7</span><span class="sxs-lookup"><span data-stu-id="3df10-130">7</span></span>

<span data-ttu-id="3df10-131">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="3df10-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3df10-132">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="3df10-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3df10-133">8</span><span class="sxs-lookup"><span data-stu-id="3df10-133">8</span></span>

<span data-ttu-id="3df10-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="3df10-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3df10-135">**Отсутствует привилегия**</span><span class="sxs-lookup"><span data-stu-id="3df10-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="3df10-136">9</span><span class="sxs-lookup"><span data-stu-id="3df10-136">9</span></span>

<span data-ttu-id="3df10-137">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="3df10-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-138">10</span><span class="sxs-lookup"><span data-stu-id="3df10-138">10</span></span>

<span data-ttu-id="3df10-139">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="3df10-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-140">11</span><span class="sxs-lookup"><span data-stu-id="3df10-140">11</span></span>

<span data-ttu-id="3df10-141">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="3df10-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-142">12</span><span class="sxs-lookup"><span data-stu-id="3df10-142">12</span></span>

<span data-ttu-id="3df10-143">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="3df10-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-144">13</span><span class="sxs-lookup"><span data-stu-id="3df10-144">13</span></span>

<span data-ttu-id="3df10-145">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="3df10-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-146">14</span><span class="sxs-lookup"><span data-stu-id="3df10-146">14</span></span>

<span data-ttu-id="3df10-147">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="3df10-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-148">15</span><span class="sxs-lookup"><span data-stu-id="3df10-148">15</span></span>

<span data-ttu-id="3df10-149">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="3df10-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-150">16</span><span class="sxs-lookup"><span data-stu-id="3df10-150">16</span></span>

<span data-ttu-id="3df10-151">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="3df10-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-152">17</span><span class="sxs-lookup"><span data-stu-id="3df10-152">17</span></span>

<span data-ttu-id="3df10-153">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="3df10-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-154">18</span><span class="sxs-lookup"><span data-stu-id="3df10-154">18</span></span>

<span data-ttu-id="3df10-155">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="3df10-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-156">19</span><span class="sxs-lookup"><span data-stu-id="3df10-156">19</span></span>

<span data-ttu-id="3df10-157">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="3df10-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-158">20</span><span class="sxs-lookup"><span data-stu-id="3df10-158">20</span></span>

<span data-ttu-id="3df10-159">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="3df10-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3df10-160">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="3df10-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3df10-161">21</span><span class="sxs-lookup"><span data-stu-id="3df10-161">21</span></span>

<span data-ttu-id="3df10-162">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="3df10-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-163">22</span><span class="sxs-lookup"><span data-stu-id="3df10-163">22</span></span>

<span data-ttu-id="3df10-164">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="3df10-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-165">23</span><span class="sxs-lookup"><span data-stu-id="3df10-165">23</span></span>

<span data-ttu-id="3df10-166">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="3df10-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3df10-167">24</span><span class="sxs-lookup"><span data-stu-id="3df10-167">24</span></span>

<span data-ttu-id="3df10-168">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="3df10-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="3df10-169">**Другое**</span><span class="sxs-lookup"><span data-stu-id="3df10-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3df10-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="3df10-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3df10-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3df10-171">Remarks</span></span>

<span data-ttu-id="3df10-172">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="3df10-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="3df10-173">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="3df10-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="3df10-174">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="3df10-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="3df10-175">Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="3df10-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="3df10-176">Примеры</span><span class="sxs-lookup"><span data-stu-id="3df10-176">Examples</span></span>

<span data-ttu-id="3df10-177">При получении дескриптора безопасности в VBScript обязательно выполните команду "безопасность" и запустите от имени администратора, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="3df10-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="3df10-178">В противном случае код может вызвать ошибку разрешений.</span><span class="sxs-lookup"><span data-stu-id="3df10-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="3df10-179">Аналогичным образом в VB.NET обязательно установите значение "Енаблепривилежес = true" и запустите приложение от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="3df10-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="3df10-180">Требования</span><span class="sxs-lookup"><span data-stu-id="3df10-180">Requirements</span></span>



| <span data-ttu-id="3df10-181">Требование</span><span class="sxs-lookup"><span data-stu-id="3df10-181">Requirement</span></span> | <span data-ttu-id="3df10-182">Значение</span><span class="sxs-lookup"><span data-stu-id="3df10-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3df10-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3df10-183">Minimum supported client</span></span><br/> | <span data-ttu-id="3df10-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3df10-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3df10-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3df10-185">Minimum supported server</span></span><br/> | <span data-ttu-id="3df10-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3df10-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3df10-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3df10-187">Namespace</span></span><br/>                | <span data-ttu-id="3df10-188">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3df10-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3df10-189">MOF</span><span class="sxs-lookup"><span data-stu-id="3df10-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3df10-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3df10-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3df10-191">DLL</span><span class="sxs-lookup"><span data-stu-id="3df10-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df10-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df10-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df10-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3df10-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df10-194">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="3df10-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="3df10-195">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="3df10-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="3df10-196">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="3df10-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="3df10-197">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="3df10-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="3df10-198">Управление учетными записями пользователей и WMI</span><span class="sxs-lookup"><span data-stu-id="3df10-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

