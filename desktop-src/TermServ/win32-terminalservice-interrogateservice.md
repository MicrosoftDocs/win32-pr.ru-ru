---
title: Метод Интеррогатесервице класса Win32_Service (службы удаленных рабочих столов)
description: Метод Интеррогатесервице класса Win32_Service (службы удаленных рабочих столов) — запрашивает обновление состояния службы, на которую указывает ссылка, в Service Manager.
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Интеррогатесервице
- Службы удаленных рабочих столов метода Интеррогатесервице, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод Интеррогатесервице
topic_type:
- apiref
api_name:
- Win32_Service.InterrogateService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850953b210ea11b9dd1000326d6793e3651ce538
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090662"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="f9252-106">Метод Интеррогатесервице класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="f9252-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="f9252-107">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) интеррогатесервице запрашивает у службы, на которую указывает ссылка, обновление своего состояния Service Manager.</span><span class="sxs-lookup"><span data-stu-id="f9252-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="f9252-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="f9252-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f9252-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f9252-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9252-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9252-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="f9252-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9252-111">Parameters</span></span>

<span data-ttu-id="f9252-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f9252-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9252-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9252-113">Return value</span></span>

<span data-ttu-id="f9252-114">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="f9252-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="f9252-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f9252-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f9252-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f9252-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f9252-117">**0**</span><span class="sxs-lookup"><span data-stu-id="f9252-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-118">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="f9252-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-119">**1**</span><span class="sxs-lookup"><span data-stu-id="f9252-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-120">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f9252-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-121">**2**</span><span class="sxs-lookup"><span data-stu-id="f9252-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="f9252-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-123">**3**</span><span class="sxs-lookup"><span data-stu-id="f9252-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-124">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="f9252-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-125">**4**</span><span class="sxs-lookup"><span data-stu-id="f9252-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="f9252-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-127">**5**</span><span class="sxs-lookup"><span data-stu-id="f9252-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-128">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="f9252-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-129">**6**</span><span class="sxs-lookup"><span data-stu-id="f9252-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-130">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="f9252-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-131">**7**</span><span class="sxs-lookup"><span data-stu-id="f9252-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-132">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="f9252-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-133">**8**</span><span class="sxs-lookup"><span data-stu-id="f9252-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="f9252-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-135">**9**</span><span class="sxs-lookup"><span data-stu-id="f9252-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="f9252-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-137">**10**</span><span class="sxs-lookup"><span data-stu-id="f9252-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="f9252-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-139">**11**</span><span class="sxs-lookup"><span data-stu-id="f9252-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="f9252-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-141">**12**</span><span class="sxs-lookup"><span data-stu-id="f9252-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="f9252-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-143">**13**</span><span class="sxs-lookup"><span data-stu-id="f9252-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="f9252-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-145">**14**</span><span class="sxs-lookup"><span data-stu-id="f9252-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="f9252-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-147">**15**</span><span class="sxs-lookup"><span data-stu-id="f9252-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="f9252-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-149">**16**</span><span class="sxs-lookup"><span data-stu-id="f9252-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="f9252-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-151">**17**</span><span class="sxs-lookup"><span data-stu-id="f9252-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="f9252-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="f9252-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="f9252-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="f9252-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="f9252-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-157">**20**</span><span class="sxs-lookup"><span data-stu-id="f9252-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="f9252-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-159">**открыт**</span><span class="sxs-lookup"><span data-stu-id="f9252-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-160">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="f9252-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-161">**22**</span><span class="sxs-lookup"><span data-stu-id="f9252-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-162">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="f9252-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-163">**23**</span><span class="sxs-lookup"><span data-stu-id="f9252-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-164">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="f9252-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f9252-165">**24**</span><span class="sxs-lookup"><span data-stu-id="f9252-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="f9252-166">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="f9252-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9252-167">Требования</span><span class="sxs-lookup"><span data-stu-id="f9252-167">Requirements</span></span>



| <span data-ttu-id="f9252-168">Требование</span><span class="sxs-lookup"><span data-stu-id="f9252-168">Requirement</span></span> | <span data-ttu-id="f9252-169">Значение</span><span class="sxs-lookup"><span data-stu-id="f9252-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9252-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9252-170">Minimum supported client</span></span><br/> | <span data-ttu-id="f9252-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9252-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9252-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9252-172">Minimum supported server</span></span><br/> | <span data-ttu-id="f9252-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9252-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9252-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f9252-174">Namespace</span></span><br/>                | <span data-ttu-id="f9252-175">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f9252-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f9252-176">MOF</span><span class="sxs-lookup"><span data-stu-id="f9252-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9252-177"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9252-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9252-178">DLL</span><span class="sxs-lookup"><span data-stu-id="f9252-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9252-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9252-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9252-180">См. также</span><span class="sxs-lookup"><span data-stu-id="f9252-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9252-181">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="f9252-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="f9252-182">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="f9252-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="f9252-183">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="f9252-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f9252-184">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="f9252-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

