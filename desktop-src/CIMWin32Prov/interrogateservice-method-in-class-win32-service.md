---
description: Запрашивает обновление состояния службы, на которую указывает ссылка, в Service Manager.
ms.assetid: a4ea8753-1859-4d97-b9ca-47598c7e7654
ms.tgt_platform: multiple
title: Метод Интеррогатесервице класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7ad1f56afcbe42ced19da823c454291a7b5282d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141303"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="d3c99-103">Метод Интеррогатесервице класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="d3c99-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d3c99-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) интеррогатесервице запрашивает у службы, на которую указывает ссылка, обновление своего состояния Service Manager.</span><span class="sxs-lookup"><span data-stu-id="d3c99-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="d3c99-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d3c99-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d3c99-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d3c99-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c99-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3c99-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="d3c99-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3c99-108">Parameters</span></span>

<span data-ttu-id="d3c99-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d3c99-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3c99-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3c99-110">Return value</span></span>

<span data-ttu-id="d3c99-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3c99-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="d3c99-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d3c99-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d3c99-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d3c99-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d3c99-114">**0**</span><span class="sxs-lookup"><span data-stu-id="d3c99-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-115">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="d3c99-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-116">**1**</span><span class="sxs-lookup"><span data-stu-id="d3c99-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-117">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d3c99-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-118">**2**</span><span class="sxs-lookup"><span data-stu-id="d3c99-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-119">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="d3c99-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-120">**3**</span><span class="sxs-lookup"><span data-stu-id="d3c99-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-121">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="d3c99-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-122">**4**</span><span class="sxs-lookup"><span data-stu-id="d3c99-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-123">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="d3c99-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-124">**5**</span><span class="sxs-lookup"><span data-stu-id="d3c99-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-125">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="d3c99-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-126">**6**</span><span class="sxs-lookup"><span data-stu-id="d3c99-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-127">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="d3c99-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-128">**7**</span><span class="sxs-lookup"><span data-stu-id="d3c99-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-129">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="d3c99-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-130">**8**</span><span class="sxs-lookup"><span data-stu-id="d3c99-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-131">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="d3c99-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-132">**9**</span><span class="sxs-lookup"><span data-stu-id="d3c99-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-133">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="d3c99-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-134">**10**</span><span class="sxs-lookup"><span data-stu-id="d3c99-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-135">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="d3c99-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-136">**11**</span><span class="sxs-lookup"><span data-stu-id="d3c99-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-137">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="d3c99-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-138">**12**</span><span class="sxs-lookup"><span data-stu-id="d3c99-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-139">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="d3c99-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-140">**13**</span><span class="sxs-lookup"><span data-stu-id="d3c99-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-141">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="d3c99-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-142">**14**</span><span class="sxs-lookup"><span data-stu-id="d3c99-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-143">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="d3c99-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-144">**15**</span><span class="sxs-lookup"><span data-stu-id="d3c99-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-145">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="d3c99-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-146">**16**</span><span class="sxs-lookup"><span data-stu-id="d3c99-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-147">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="d3c99-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-148">**17**</span><span class="sxs-lookup"><span data-stu-id="d3c99-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-149">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="d3c99-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-150">**стр**</span><span class="sxs-lookup"><span data-stu-id="d3c99-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-151">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="d3c99-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-152">**стр**</span><span class="sxs-lookup"><span data-stu-id="d3c99-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-153">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="d3c99-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-154">**20**</span><span class="sxs-lookup"><span data-stu-id="d3c99-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-155">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="d3c99-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-156">**открыт**</span><span class="sxs-lookup"><span data-stu-id="d3c99-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-157">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="d3c99-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-158">**22**</span><span class="sxs-lookup"><span data-stu-id="d3c99-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-159">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="d3c99-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-160">**23**</span><span class="sxs-lookup"><span data-stu-id="d3c99-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-161">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="d3c99-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d3c99-162">**24**</span><span class="sxs-lookup"><span data-stu-id="d3c99-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="d3c99-163">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="d3c99-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3c99-164">Требования</span><span class="sxs-lookup"><span data-stu-id="d3c99-164">Requirements</span></span>



| <span data-ttu-id="d3c99-165">Требование</span><span class="sxs-lookup"><span data-stu-id="d3c99-165">Requirement</span></span> | <span data-ttu-id="d3c99-166">Значение</span><span class="sxs-lookup"><span data-stu-id="d3c99-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c99-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3c99-167">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c99-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3c99-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3c99-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3c99-169">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c99-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3c99-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3c99-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d3c99-171">Namespace</span></span><br/>                | <span data-ttu-id="d3c99-172">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d3c99-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d3c99-173">MOF</span><span class="sxs-lookup"><span data-stu-id="d3c99-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3c99-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3c99-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3c99-175">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c99-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c99-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c99-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c99-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3c99-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c99-178">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="d3c99-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="d3c99-179">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3c99-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d3c99-180">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="d3c99-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="d3c99-181">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="d3c99-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

