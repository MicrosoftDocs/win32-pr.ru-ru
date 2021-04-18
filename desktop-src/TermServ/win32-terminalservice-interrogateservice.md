---
title: Метод Интеррогатесервице класса Win32_Service (службы удаленных рабочих столов)
description: Запрашивает обновление состояния службы, на которую указывает ссылка, в Service Manager.
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
ms.openlocfilehash: 6f53b3d5e1cced6b6820f9b7334551de47f333be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681880"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="fc623-106">Метод Интеррогатесервице класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="fc623-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="fc623-107">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) интеррогатесервице запрашивает у службы, на которую указывает ссылка, обновление своего состояния Service Manager.</span><span class="sxs-lookup"><span data-stu-id="fc623-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="fc623-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="fc623-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fc623-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fc623-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc623-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc623-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="fc623-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc623-111">Parameters</span></span>

<span data-ttu-id="fc623-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fc623-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc623-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc623-113">Return value</span></span>

<span data-ttu-id="fc623-114">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="fc623-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="fc623-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fc623-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fc623-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fc623-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fc623-117">**0**</span><span class="sxs-lookup"><span data-stu-id="fc623-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-118">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="fc623-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-119">**1**</span><span class="sxs-lookup"><span data-stu-id="fc623-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-120">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc623-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-121">**2**</span><span class="sxs-lookup"><span data-stu-id="fc623-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="fc623-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-123">**3**</span><span class="sxs-lookup"><span data-stu-id="fc623-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-124">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="fc623-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-125">**4**</span><span class="sxs-lookup"><span data-stu-id="fc623-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-126">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="fc623-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-127">**5**</span><span class="sxs-lookup"><span data-stu-id="fc623-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-128">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="fc623-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-129">**6**</span><span class="sxs-lookup"><span data-stu-id="fc623-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-130">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="fc623-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-131">**7**</span><span class="sxs-lookup"><span data-stu-id="fc623-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-132">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="fc623-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-133">**8**</span><span class="sxs-lookup"><span data-stu-id="fc623-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-134">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="fc623-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-135">**9**</span><span class="sxs-lookup"><span data-stu-id="fc623-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-136">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="fc623-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-137">**10**</span><span class="sxs-lookup"><span data-stu-id="fc623-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-138">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="fc623-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-139">**11**</span><span class="sxs-lookup"><span data-stu-id="fc623-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-140">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="fc623-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-141">**12**</span><span class="sxs-lookup"><span data-stu-id="fc623-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-142">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="fc623-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-143">**13**</span><span class="sxs-lookup"><span data-stu-id="fc623-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-144">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="fc623-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-145">**14**</span><span class="sxs-lookup"><span data-stu-id="fc623-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-146">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="fc623-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-147">**15**</span><span class="sxs-lookup"><span data-stu-id="fc623-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-148">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="fc623-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-149">**16**</span><span class="sxs-lookup"><span data-stu-id="fc623-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-150">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="fc623-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-151">**17**</span><span class="sxs-lookup"><span data-stu-id="fc623-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-152">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="fc623-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="fc623-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-154">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="fc623-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-155">**стр**</span><span class="sxs-lookup"><span data-stu-id="fc623-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-156">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="fc623-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-157">**20**</span><span class="sxs-lookup"><span data-stu-id="fc623-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-158">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="fc623-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-159">**открыт**</span><span class="sxs-lookup"><span data-stu-id="fc623-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-160">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="fc623-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-161">**22**</span><span class="sxs-lookup"><span data-stu-id="fc623-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-162">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="fc623-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-163">**23**</span><span class="sxs-lookup"><span data-stu-id="fc623-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-164">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="fc623-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fc623-165">**24**</span><span class="sxs-lookup"><span data-stu-id="fc623-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="fc623-166">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="fc623-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc623-167">Требования</span><span class="sxs-lookup"><span data-stu-id="fc623-167">Requirements</span></span>



| <span data-ttu-id="fc623-168">Требование</span><span class="sxs-lookup"><span data-stu-id="fc623-168">Requirement</span></span> | <span data-ttu-id="fc623-169">Значение</span><span class="sxs-lookup"><span data-stu-id="fc623-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc623-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc623-170">Minimum supported client</span></span><br/> | <span data-ttu-id="fc623-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc623-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc623-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc623-172">Minimum supported server</span></span><br/> | <span data-ttu-id="fc623-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc623-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc623-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fc623-174">Namespace</span></span><br/>                | <span data-ttu-id="fc623-175">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="fc623-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fc623-176">MOF</span><span class="sxs-lookup"><span data-stu-id="fc623-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc623-177"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc623-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc623-178">DLL</span><span class="sxs-lookup"><span data-stu-id="fc623-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc623-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc623-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc623-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc623-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc623-181">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="fc623-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="fc623-182">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="fc623-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="fc623-183">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="fc623-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="fc623-184">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="fc623-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

