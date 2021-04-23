---
description: Пытается разместить службу, управляемую драйвером логической системы, в приостановленном состоянии.
ms.assetid: f5e960c1-868b-4b7b-9ea5-0fb8a9cfbafa
ms.tgt_platform: multiple
title: Метод PauseService класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a85c49a8ea81cc9af9a99f238bdafb473ca85050
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990808"
---
# <a name="pauseservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="47f4f-103">Метод PauseService \_ класса Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="47f4f-103">PauseService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="47f4f-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) PauseService пытается разместить службу, управляемую драйвером логической системы, в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="47f4f-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service managed by the logical system driver in the paused state.</span></span>

<span data-ttu-id="47f4f-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="47f4f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="47f4f-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="47f4f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="47f4f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47f4f-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="47f4f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="47f4f-108">Parameters</span></span>

<span data-ttu-id="47f4f-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="47f4f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47f4f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47f4f-110">Return value</span></span>

<span data-ttu-id="47f4f-111">Возвращает значение 0 (ноль), если запрос **PauseService** был принят, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="47f4f-111">Returns a value of 0 (zero) if the **PauseService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="47f4f-112">**0**</span><span class="sxs-lookup"><span data-stu-id="47f4f-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-113">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="47f4f-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-114">**1**</span><span class="sxs-lookup"><span data-stu-id="47f4f-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-115">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="47f4f-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-116">**2**</span><span class="sxs-lookup"><span data-stu-id="47f4f-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-117">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="47f4f-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-118">**3**</span><span class="sxs-lookup"><span data-stu-id="47f4f-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-119">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="47f4f-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-120">**4**</span><span class="sxs-lookup"><span data-stu-id="47f4f-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-121">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="47f4f-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-122">**5**</span><span class="sxs-lookup"><span data-stu-id="47f4f-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-123">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="47f4f-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-124">**6**</span><span class="sxs-lookup"><span data-stu-id="47f4f-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-125">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="47f4f-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-126">**7**</span><span class="sxs-lookup"><span data-stu-id="47f4f-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-127">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="47f4f-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-128">**8**</span><span class="sxs-lookup"><span data-stu-id="47f4f-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-129">При запуске службы произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="47f4f-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-130">**9**</span><span class="sxs-lookup"><span data-stu-id="47f4f-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-131">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="47f4f-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-132">**10**</span><span class="sxs-lookup"><span data-stu-id="47f4f-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-133">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="47f4f-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-134">**11**</span><span class="sxs-lookup"><span data-stu-id="47f4f-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-135">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="47f4f-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-136">**12**</span><span class="sxs-lookup"><span data-stu-id="47f4f-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-137">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="47f4f-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-138">**13**</span><span class="sxs-lookup"><span data-stu-id="47f4f-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-139">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="47f4f-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-140">**14**</span><span class="sxs-lookup"><span data-stu-id="47f4f-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-141">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="47f4f-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-142">**15**</span><span class="sxs-lookup"><span data-stu-id="47f4f-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-143">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="47f4f-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-144">**16**</span><span class="sxs-lookup"><span data-stu-id="47f4f-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-145">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="47f4f-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-146">**17**</span><span class="sxs-lookup"><span data-stu-id="47f4f-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-147">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="47f4f-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-148">**стр**</span><span class="sxs-lookup"><span data-stu-id="47f4f-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-149">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="47f4f-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-150">**стр**</span><span class="sxs-lookup"><span data-stu-id="47f4f-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-151">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="47f4f-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-152">**20**</span><span class="sxs-lookup"><span data-stu-id="47f4f-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-153">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="47f4f-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-154">**открыт**</span><span class="sxs-lookup"><span data-stu-id="47f4f-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-155">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="47f4f-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-156">**22**</span><span class="sxs-lookup"><span data-stu-id="47f4f-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-157">Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="47f4f-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-158">**23**</span><span class="sxs-lookup"><span data-stu-id="47f4f-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-159">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="47f4f-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="47f4f-160">**24**</span><span class="sxs-lookup"><span data-stu-id="47f4f-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="47f4f-161">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="47f4f-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="47f4f-162">Примеры</span><span class="sxs-lookup"><span data-stu-id="47f4f-162">Examples</span></span>

<span data-ttu-id="47f4f-163">Следующий код PowerShell пытается приостановить работу службы "класс принтера Microsoft USB".</span><span class="sxs-lookup"><span data-stu-id="47f4f-163">The following PowerShell code attempts to pause the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.PauseService()
"Pause Service called. The return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="47f4f-164">Требования</span><span class="sxs-lookup"><span data-stu-id="47f4f-164">Requirements</span></span>



| <span data-ttu-id="47f4f-165">Требование</span><span class="sxs-lookup"><span data-stu-id="47f4f-165">Requirement</span></span> | <span data-ttu-id="47f4f-166">Значение</span><span class="sxs-lookup"><span data-stu-id="47f4f-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47f4f-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47f4f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="47f4f-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47f4f-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47f4f-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47f4f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="47f4f-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47f4f-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47f4f-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="47f4f-171">Namespace</span></span><br/>                | <span data-ttu-id="47f4f-172">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="47f4f-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47f4f-173">MOF</span><span class="sxs-lookup"><span data-stu-id="47f4f-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47f4f-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47f4f-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47f4f-175">DLL</span><span class="sxs-lookup"><span data-stu-id="47f4f-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47f4f-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47f4f-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f4f-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47f4f-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="47f4f-178">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47f4f-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="47f4f-179">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="47f4f-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

