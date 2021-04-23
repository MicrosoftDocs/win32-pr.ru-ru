---
title: Метод Усерконтролсервице класса Win32_Service (службы удаленных рабочих столов)
description: Пытается отправить определяемый пользователем код элемента управления в указанную службу.
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Усерконтролсервице
- Службы удаленных рабочих столов метода Усерконтролсервице, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод Усерконтролсервице
topic_type:
- apiref
api_name:
- Win32_Service.UserControlService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b1ea4f5e82814aad7549085070b0583993024b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492738"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="e0f9d-106">Метод Усерконтролсервице класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="e0f9d-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="e0f9d-107">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) усерконтролсервице пытается отправить определяемый пользователем код элемента управления в указанную службу.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="e0f9d-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e0f9d-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e0f9d-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e0f9d-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f9d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0f9d-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="e0f9d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0f9d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f9d-112">*Контролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0f9d-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-113">Задает определенные значения (от 128 до 255), которые предоставляют управляющие команды, характерные для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f9d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0f9d-114">Return value</span></span>

<span data-ttu-id="e0f9d-115">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="e0f9d-116">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e0f9d-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e0f9d-117">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e0f9d-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e0f9d-118">**0**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-119">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-120">**1**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-121">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-122">**2**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-123">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-124">**3**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-125">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-126">**4**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-127">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-128">**5**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-129">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-130">**6**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-131">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-132">**7**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-133">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-134">**8**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-135">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-136">**9**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-137">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-138">**10**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-139">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-140">**11**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-141">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-142">**12**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-143">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-144">**13**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-145">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-146">**14**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-147">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-148">**15**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-149">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-150">**16**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-151">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-152">**17**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-153">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-154">**стр**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-155">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-156">**стр**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-157">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-158">**20**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-159">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-160">**открыт**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-161">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-162">**22**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-163">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-164">**23**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-165">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e0f9d-166">**24**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="e0f9d-167">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="e0f9d-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0f9d-168">Требования</span><span class="sxs-lookup"><span data-stu-id="e0f9d-168">Requirements</span></span>



| <span data-ttu-id="e0f9d-169">Требование</span><span class="sxs-lookup"><span data-stu-id="e0f9d-169">Requirement</span></span> | <span data-ttu-id="e0f9d-170">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f9d-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f9d-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0f9d-171">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f9d-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0f9d-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0f9d-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0f9d-173">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f9d-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0f9d-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0f9d-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e0f9d-175">Namespace</span></span><br/>                | <span data-ttu-id="e0f9d-176">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e0f9d-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e0f9d-177">MOF</span><span class="sxs-lookup"><span data-stu-id="e0f9d-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0f9d-178"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9d-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0f9d-179">DLL</span><span class="sxs-lookup"><span data-stu-id="e0f9d-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0f9d-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0f9d-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f9d-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0f9d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f9d-182">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="e0f9d-183">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="e0f9d-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="e0f9d-184">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="e0f9d-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 

