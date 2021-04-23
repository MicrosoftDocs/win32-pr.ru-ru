---
description: Пытается отправить определяемый пользователем код элемента управления в указанную службу.
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
ms.openlocfilehash: 8c523617826bd5d608b8c6b1ee242863f7591a61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990737"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="f472a-103">Метод Усерконтролсервице класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f472a-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f472a-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) усерконтролсервице пытается отправить определяемый пользователем код элемента управления в указанную службу.</span><span class="sxs-lookup"><span data-stu-id="f472a-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="f472a-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="f472a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f472a-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f472a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f472a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f472a-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="f472a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f472a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f472a-109">*Контролкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f472a-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f472a-110">Задает определенные значения (от 128 до 255), которые предоставляют управляющие команды, характерные для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f472a-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f472a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f472a-111">Return value</span></span>

<span data-ttu-id="f472a-112">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="f472a-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="f472a-113">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f472a-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f472a-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f472a-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f472a-115">**0**</span><span class="sxs-lookup"><span data-stu-id="f472a-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-116">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="f472a-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-117">**1**</span><span class="sxs-lookup"><span data-stu-id="f472a-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-118">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f472a-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-119">**2**</span><span class="sxs-lookup"><span data-stu-id="f472a-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-120">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="f472a-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-121">**3**</span><span class="sxs-lookup"><span data-stu-id="f472a-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-122">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="f472a-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-123">**4**</span><span class="sxs-lookup"><span data-stu-id="f472a-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-124">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="f472a-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-125">**5**</span><span class="sxs-lookup"><span data-stu-id="f472a-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-126">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="f472a-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-127">**6**</span><span class="sxs-lookup"><span data-stu-id="f472a-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-128">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="f472a-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-129">**7**</span><span class="sxs-lookup"><span data-stu-id="f472a-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-130">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="f472a-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-131">**8**</span><span class="sxs-lookup"><span data-stu-id="f472a-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-132">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="f472a-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-133">**9**</span><span class="sxs-lookup"><span data-stu-id="f472a-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-134">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="f472a-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-135">**10**</span><span class="sxs-lookup"><span data-stu-id="f472a-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-136">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="f472a-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-137">**11**</span><span class="sxs-lookup"><span data-stu-id="f472a-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-138">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="f472a-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-139">**12**</span><span class="sxs-lookup"><span data-stu-id="f472a-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-140">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="f472a-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-141">**13**</span><span class="sxs-lookup"><span data-stu-id="f472a-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-142">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="f472a-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-143">**14**</span><span class="sxs-lookup"><span data-stu-id="f472a-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-144">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="f472a-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-145">**15**</span><span class="sxs-lookup"><span data-stu-id="f472a-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-146">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="f472a-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-147">**16**</span><span class="sxs-lookup"><span data-stu-id="f472a-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-148">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="f472a-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-149">**17**</span><span class="sxs-lookup"><span data-stu-id="f472a-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-150">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="f472a-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-151">**стр**</span><span class="sxs-lookup"><span data-stu-id="f472a-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-152">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="f472a-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-153">**стр**</span><span class="sxs-lookup"><span data-stu-id="f472a-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-154">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="f472a-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-155">**20**</span><span class="sxs-lookup"><span data-stu-id="f472a-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-156">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="f472a-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-157">**открыт**</span><span class="sxs-lookup"><span data-stu-id="f472a-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-158">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="f472a-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-159">**22**</span><span class="sxs-lookup"><span data-stu-id="f472a-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-160">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="f472a-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-161">**23**</span><span class="sxs-lookup"><span data-stu-id="f472a-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-162">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="f472a-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f472a-163">**24**</span><span class="sxs-lookup"><span data-stu-id="f472a-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="f472a-164">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="f472a-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f472a-165">Требования</span><span class="sxs-lookup"><span data-stu-id="f472a-165">Requirements</span></span>



| <span data-ttu-id="f472a-166">Требование</span><span class="sxs-lookup"><span data-stu-id="f472a-166">Requirement</span></span> | <span data-ttu-id="f472a-167">Значение</span><span class="sxs-lookup"><span data-stu-id="f472a-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f472a-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f472a-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f472a-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f472a-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f472a-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f472a-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f472a-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f472a-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f472a-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f472a-172">Namespace</span></span><br/>                | <span data-ttu-id="f472a-173">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f472a-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f472a-174">MOF</span><span class="sxs-lookup"><span data-stu-id="f472a-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f472a-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f472a-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f472a-176">DLL</span><span class="sxs-lookup"><span data-stu-id="f472a-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f472a-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f472a-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f472a-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f472a-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="f472a-179">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f472a-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f472a-180">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="f472a-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

