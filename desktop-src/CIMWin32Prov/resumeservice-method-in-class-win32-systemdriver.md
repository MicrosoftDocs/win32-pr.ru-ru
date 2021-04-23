---
description: Пытается поместить службу, управляемую драйвером системы, в состояние возобновления.
ms.assetid: 16bacf06-4236-4d58-9b09-cb86bb73d78a
ms.tgt_platform: multiple
title: Метод ResumeService класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d326fcd0a3bc9801f5e214cdc8740170cf1f1cf8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990422"
---
# <a name="resumeservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="7ea8d-103">Метод ResumeService \_ класса Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="7ea8d-103">ResumeService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="7ea8d-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ResumeService пытается поместить службу, управляемую драйвером системы, в состояние возобновления.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service managed by the system driver in the resumed state.</span></span>

<span data-ttu-id="7ea8d-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="7ea8d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7ea8d-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7ea8d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea8d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ea8d-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="7ea8d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ea8d-108">Parameters</span></span>

<span data-ttu-id="7ea8d-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ea8d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ea8d-110">Return value</span></span>

<span data-ttu-id="7ea8d-111">Возвращает значение 0 (ноль), если запрос **ResumeService** был принят, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-111">Returns a value of 0 (zero) if the **ResumeService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7ea8d-112">**0**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-113">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-114">**1**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-115">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-116">**2**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-117">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-118">**3**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-119">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-120">**4**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-121">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-122">**5**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-123">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-124">**6**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-125">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-126">**7**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-127">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-128">**8**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-129">При запуске службы произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-130">**9**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-131">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-132">**10**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-133">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-134">**11**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-135">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-136">**12**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-137">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-138">**13**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-139">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-140">**14**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-141">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-142">**15**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-143">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-144">**16**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-145">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-146">**17**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-147">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-148">**стр**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-149">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-150">**стр**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-151">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-152">**20**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-153">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-154">**открыт**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-155">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-156">**22**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-157">Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-158">**23**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-159">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7ea8d-160">**24**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="7ea8d-161">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="7ea8d-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7ea8d-162">Примеры</span><span class="sxs-lookup"><span data-stu-id="7ea8d-162">Examples</span></span>

<span data-ttu-id="7ea8d-163">Следующий код PowerShell пытается возобновить работу службы "класс принтера Microsoft USB".</span><span class="sxs-lookup"><span data-stu-id="7ea8d-163">The following PowerShell code attempts to resume the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.ResumeService()
"Resume Service Called. The return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="7ea8d-164">Требования</span><span class="sxs-lookup"><span data-stu-id="7ea8d-164">Requirements</span></span>



| <span data-ttu-id="7ea8d-165">Требование</span><span class="sxs-lookup"><span data-stu-id="7ea8d-165">Requirement</span></span> | <span data-ttu-id="7ea8d-166">Значение</span><span class="sxs-lookup"><span data-stu-id="7ea8d-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea8d-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ea8d-167">Minimum supported client</span></span><br/> | <span data-ttu-id="7ea8d-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ea8d-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ea8d-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ea8d-169">Minimum supported server</span></span><br/> | <span data-ttu-id="7ea8d-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ea8d-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ea8d-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7ea8d-171">Namespace</span></span><br/>                | <span data-ttu-id="7ea8d-172">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7ea8d-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7ea8d-173">MOF</span><span class="sxs-lookup"><span data-stu-id="7ea8d-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ea8d-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ea8d-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ea8d-175">DLL</span><span class="sxs-lookup"><span data-stu-id="7ea8d-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ea8d-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ea8d-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ea8d-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ea8d-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ea8d-178">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ea8d-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7ea8d-179">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="7ea8d-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

