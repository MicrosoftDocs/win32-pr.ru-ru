---
description: Метод Усерконтролсервице класса Win32_Service (поставщики WMI CIMWin32) — пытается отправить определяемый пользователем код элемента управления в указанную службу.
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: Метод Усерконтролсервице класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 455128b35c2645c6aa6ea10f64d12dff392fecca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100007"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="8d8de-103">Метод Усерконтролсервице класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="8d8de-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8d8de-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) усерконтролсервице пытается отправить определяемый пользователем код элемента управления в указанную службу.</span><span class="sxs-lookup"><span data-stu-id="8d8de-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="8d8de-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="8d8de-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8d8de-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8d8de-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8de-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d8de-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="8d8de-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d8de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8de-109">*Контролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d8de-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-110">Задает определенные значения (от 128 до 255), которые предоставляют управляющие команды, характерные для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d8de-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8de-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d8de-111">Return value</span></span>

<span data-ttu-id="8d8de-112">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="8d8de-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="8d8de-113">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8d8de-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8d8de-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8d8de-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8d8de-115">**0**</span><span class="sxs-lookup"><span data-stu-id="8d8de-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-116">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="8d8de-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-117">**1**</span><span class="sxs-lookup"><span data-stu-id="8d8de-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-118">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8d8de-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-119">**2**</span><span class="sxs-lookup"><span data-stu-id="8d8de-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-120">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="8d8de-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-121">**3**</span><span class="sxs-lookup"><span data-stu-id="8d8de-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-122">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="8d8de-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-123">**4**</span><span class="sxs-lookup"><span data-stu-id="8d8de-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-124">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="8d8de-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-125">**5**</span><span class="sxs-lookup"><span data-stu-id="8d8de-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-126">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="8d8de-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-127">**6**</span><span class="sxs-lookup"><span data-stu-id="8d8de-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-128">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="8d8de-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-129">**7**</span><span class="sxs-lookup"><span data-stu-id="8d8de-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-130">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="8d8de-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-131">**8**</span><span class="sxs-lookup"><span data-stu-id="8d8de-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-132">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="8d8de-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-133">**9**</span><span class="sxs-lookup"><span data-stu-id="8d8de-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-134">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="8d8de-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-135">**10**</span><span class="sxs-lookup"><span data-stu-id="8d8de-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-136">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="8d8de-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-137">**11**</span><span class="sxs-lookup"><span data-stu-id="8d8de-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-138">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="8d8de-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-139">**12**</span><span class="sxs-lookup"><span data-stu-id="8d8de-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-140">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="8d8de-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-141">**13**</span><span class="sxs-lookup"><span data-stu-id="8d8de-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-142">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="8d8de-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-143">**14**</span><span class="sxs-lookup"><span data-stu-id="8d8de-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-144">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="8d8de-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-145">**15**</span><span class="sxs-lookup"><span data-stu-id="8d8de-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-146">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="8d8de-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-147">**16**</span><span class="sxs-lookup"><span data-stu-id="8d8de-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-148">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="8d8de-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-149">**17**</span><span class="sxs-lookup"><span data-stu-id="8d8de-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-150">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="8d8de-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-151">**стр**</span><span class="sxs-lookup"><span data-stu-id="8d8de-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-152">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="8d8de-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="8d8de-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-154">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="8d8de-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-155">**20**</span><span class="sxs-lookup"><span data-stu-id="8d8de-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-156">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="8d8de-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-157">**открыт**</span><span class="sxs-lookup"><span data-stu-id="8d8de-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-158">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="8d8de-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-159">**22**</span><span class="sxs-lookup"><span data-stu-id="8d8de-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-160">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="8d8de-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-161">**23**</span><span class="sxs-lookup"><span data-stu-id="8d8de-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-162">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="8d8de-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8d8de-163">**24**</span><span class="sxs-lookup"><span data-stu-id="8d8de-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="8d8de-164">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="8d8de-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d8de-165">Требования</span><span class="sxs-lookup"><span data-stu-id="8d8de-165">Requirements</span></span>



| <span data-ttu-id="8d8de-166">Требование</span><span class="sxs-lookup"><span data-stu-id="8d8de-166">Requirement</span></span> | <span data-ttu-id="8d8de-167">Значение</span><span class="sxs-lookup"><span data-stu-id="8d8de-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8de-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d8de-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8de-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d8de-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d8de-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d8de-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8de-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d8de-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d8de-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8d8de-172">Namespace</span></span><br/>                | <span data-ttu-id="8d8de-173">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8d8de-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d8de-174">MOF</span><span class="sxs-lookup"><span data-stu-id="8d8de-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d8de-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d8de-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d8de-176">DLL</span><span class="sxs-lookup"><span data-stu-id="8d8de-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d8de-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d8de-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d8de-178">См. также</span><span class="sxs-lookup"><span data-stu-id="8d8de-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d8de-179">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d8de-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8d8de-180">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="8d8de-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

