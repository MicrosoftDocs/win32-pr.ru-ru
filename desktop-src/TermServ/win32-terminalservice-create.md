---
title: Метод Create класса Win32_Service (службы удаленных рабочих столов)
description: Создает новую системную службу.
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Create
- Создание службы удаленных рабочих столов метода, Win32_Service класса
- Класс Win32_Service службы удаленных рабочих столов, метод Create
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44d6c67e0d5bd6333f57c44cc44c25dc64e04a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491601"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="a9e0c-106">Метод Create класса Win32_Service (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="a9e0c-106">Create method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="a9e0c-107">Метод **создания** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) создает новую системную службу.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-107">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="a9e0c-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a9e0c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a9e0c-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a9e0c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9e0c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9e0c-110">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="a9e0c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9e0c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9e0c-112">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-113">Имя службы, устанавливаемой в метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="a9e0c-114">Максимальная длина строки — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="a9e0c-115">База данных диспетчера управления службами сохраняет регистр символов, но сравнения имен служб всегда не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="a9e0c-116">Прямые косые черты (/) и двойные обратные косые черты ( \) являются недопустимыми символами имени службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-116">Forward-slashes (/) and double back-slashes (\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-117">*DisplayName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-118">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-118">Display name of the service.</span></span> <span data-ttu-id="a9e0c-119">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="a9e0c-120">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="a9e0c-121">В сравнениях *DisplayName* всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="a9e0c-122">Ограничения: принимает то же значение, что и параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="a9e0c-123">Пример: "Атдиск".</span><span class="sxs-lookup"><span data-stu-id="a9e0c-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-124">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-125">Полный путь к исполняемому файлу, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="a9e0c-126">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="a9e0c-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-127">*ServiceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-128">Тип служб, предоставляемых процессам, которые их вызывают.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-128">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="a9e0c-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a9e0c-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-130">Драйвер ядра</span><span class="sxs-lookup"><span data-stu-id="a9e0c-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="a9e0c-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-132">Драйвер файловой системы</span><span class="sxs-lookup"><span data-stu-id="a9e0c-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="a9e0c-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-134">Адаптер</span><span class="sxs-lookup"><span data-stu-id="a9e0c-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="a9e0c-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-136">Драйвер распознавателя</span><span class="sxs-lookup"><span data-stu-id="a9e0c-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="a9e0c-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-138">Собственный процесс</span><span class="sxs-lookup"><span data-stu-id="a9e0c-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="a9e0c-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-140">Общий процесс</span><span class="sxs-lookup"><span data-stu-id="a9e0c-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="a9e0c-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-142">Интерактивный процесс</span><span class="sxs-lookup"><span data-stu-id="a9e0c-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a9e0c-143">*ErrorControl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-144">Серьезность ошибки, если не удается запустить метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="a9e0c-145">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-145">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="a9e0c-146">Все ошибки регистрируются системой.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="a9e0c-147">0</span><span class="sxs-lookup"><span data-stu-id="a9e0c-147">0</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-148">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-148">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-149">1</span><span class="sxs-lookup"><span data-stu-id="a9e0c-149">1</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-150">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-150">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-151">2</span><span class="sxs-lookup"><span data-stu-id="a9e0c-151">2</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-152">Система перезапускается в последней известной рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-152">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-153">3</span><span class="sxs-lookup"><span data-stu-id="a9e0c-153">3</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-154">Система пытается начать с хорошей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-154">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a9e0c-155">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-155">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-156">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-156">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="a9e0c-157">Загрузка</span><span class="sxs-lookup"><span data-stu-id="a9e0c-157">Boot</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-158">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-158">Device driver started by the operating system loader.</span></span> <span data-ttu-id="a9e0c-159">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-160">Система</span><span class="sxs-lookup"><span data-stu-id="a9e0c-160">System</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-161">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-161">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="a9e0c-162">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-162">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-163">Автоматически</span><span class="sxs-lookup"><span data-stu-id="a9e0c-163">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-164">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-164">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-165">Вручную</span><span class="sxs-lookup"><span data-stu-id="a9e0c-165">Manual</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-166">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-166">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-167">Выключено</span><span class="sxs-lookup"><span data-stu-id="a9e0c-167">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-168">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-168">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a9e0c-169">*Десктопинтеракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-169">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-170">Если задано **значение true**, служба может создавать окна на рабочем столе или взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-170">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-171">*StartName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-171">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-172">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-172">Account name under which the service runs.</span></span> <span data-ttu-id="a9e0c-173">В зависимости от типа службы имя учетной записи может иметь \\ Формат имя_домена имя_пользователя или имя участника-пользователя (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="a9e0c-173">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="a9e0c-174">Процесс службы заносится в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-174">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="a9e0c-175">Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-175">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="a9e0c-176">Если указано **значение NULL** , служба входит в систему как учетную запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-176">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="a9e0c-177">Для драйверов ядра или системного уровня *StartName* содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-177">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="a9e0c-178">Если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-178">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="a9e0c-179">Пример: ДВДОМ \\ Admin.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-179">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-180">*Стартпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-180">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-181">Пароль к имени учетной записи, заданному параметром *StartName* .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-181">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="a9e0c-182">Если пароль не изменяется, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-182">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="a9e0c-183">Если служба не имеет пароля, указывается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-183">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-184">*Лоадордерграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-184">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-185">Имя группы, связанное с новой службой.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-185">Group name associated with the new service.</span></span> <span data-ttu-id="a9e0c-186">Группы порядка загрузки содержатся в реестре и определяют последовательность, в которой службы загружаются в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-186">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="a9e0c-187">Если указатель равен **null** или указывает на пустую строку, служба не принадлежит группе.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-187">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="a9e0c-188">Зависимости между группами должны быть перечислены в параметре *лоадордерграупдепенденЦиес* .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-188">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="a9e0c-189">Сначала запускаются службы в списке группы упорядочения нагрузки, а затем — службы в группах, которые не входят в список групп порядка загрузки, за которыми следуют службы, не входящие в группу.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-189">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="a9e0c-190">В реестре имеется список групп упорядочения нагрузки, расположенных по адресу:</span><span class="sxs-lookup"><span data-stu-id="a9e0c-190">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="a9e0c-191">**HKey \_ \_** \\  \\  \\  \\ **ServiceGroupOrder** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="a9e0c-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-192">*ЛоадордерграупдепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-192">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-193">Массив групп упорядочивания нагрузки, которые должны быть запущены перед этой службой.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-193">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="a9e0c-194">Каждый элемент массива отделяется **значением NULL** , а список завершается двумя значениями **null** .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-194">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="a9e0c-195">В Visual Basic или скрипте можно передать массив vbArray.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-195">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="a9e0c-196">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-196">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="a9e0c-197">Имена групп должны иметь префикс в виде **\_ \_ идентификатора группы SC** (определенного в файле винсвк. h), чтобы отличать его от имени службы, так как службы и группы служб используют одно и то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-197">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="a9e0c-198">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-198">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-199">*СервицедепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a9e0c-199">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-200">Массив, содержащий имена служб, которые должны запускаться перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-200">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="a9e0c-201">Каждый элемент массива отделяется **значением NULL** , а список завершается двумя значениями **null** .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-201">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="a9e0c-202">В Visual Basic или скрипте можно передать массив vbArray.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-202">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="a9e0c-203">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="a9e0c-204">Зависимость от службы означает, что эта служба может выполняться, только если запущена служба, от которой она зависит.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-204">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9e0c-205">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9e0c-205">Return value</span></span>

<span data-ttu-id="a9e0c-206">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-206">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="a9e0c-207">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a9e0c-207">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a9e0c-208">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a9e0c-208">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a9e0c-209">**0**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-209">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-210">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-210">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-211">**1**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-211">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-212">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-212">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-213">**2**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-213">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-214">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-214">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-215">**3**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-215">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-216">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-216">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-217">**4**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-217">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-218">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-218">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-219">**5**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-219">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-220">Запрошенный управляющий код не может быть отправлен в службу, так как состояние службы (свойство **State** класса [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice) ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-220">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-221">**6**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-221">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-222">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-223">**7**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-223">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-224">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-224">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-225">**8**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-225">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-226">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-226">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-227">**9**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-227">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-228">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-228">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-229">**10**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-229">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-230">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-230">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-231">**11**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-231">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-232">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-232">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-233">**12**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-233">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-234">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-234">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-235">**13**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-235">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-236">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-236">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-237">**14**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-237">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-238">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-238">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-239">**15**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-239">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-240">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-240">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-241">**16**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-241">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-242">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-242">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-243">**17**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-243">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-244">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-244">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-245">**стр**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-245">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-246">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-246">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-247">**стр**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-247">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-248">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-248">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-249">**20**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-249">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-250">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-250">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-251">**открыт**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-251">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-252">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-252">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-253">**22**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-253">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-254">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-254">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-255">**23**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-255">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-256">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-256">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a9e0c-257">**24**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-257">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a9e0c-258">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-258">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9e0c-259">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9e0c-259">Remarks</span></span>

<span data-ttu-id="a9e0c-260">Службы обычно устанавливаются одним из двух способов: либо как часть установки операционной системы, либо с помощью программы установки, предоставляемой разработчиком службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-260">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="a9e0c-261">Однако некоторые службы, в частности созданные в Организации, могут не иметь программы установки.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-261">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="a9e0c-262">В этих случаях для программной установки служб можно использовать метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-262">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="a9e0c-263">Несмотря на имя, метод Create на самом деле не создает службу; Он просто устанавливает существующую службу.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-263">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="a9e0c-264">Чтобы использовать эту команду, необходимо скопировать исполняемый файл службы на компьютер, а затем воспользоваться командой **создать** для установки службы.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-264">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="a9e0c-265">Метод **CREATE** аналогичен методу [**Change**](win32-terminalservice-change.md) .</span><span class="sxs-lookup"><span data-stu-id="a9e0c-265">The **Create** method is similar to the [**Change**](win32-terminalservice-change.md) method.</span></span> <span data-ttu-id="a9e0c-266">В обоих случаях свойства службы передаются в качестве параметров в метод.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-266">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="a9e0c-267">Как и в случае с параметрами, используемыми в методе **Change** , порядок, в котором передаются эти параметры, очень важен.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-267">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="a9e0c-268">Параметр *лоадордерграуп* представляет группирование системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-268">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="a9e0c-269">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-269">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="a9e0c-270">Для правильной работы этих зависимых служб требуется наличие предшествующих служб.</span><span class="sxs-lookup"><span data-stu-id="a9e0c-270">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9e0c-271">Требования</span><span class="sxs-lookup"><span data-stu-id="a9e0c-271">Requirements</span></span>



| <span data-ttu-id="a9e0c-272">Требование</span><span class="sxs-lookup"><span data-stu-id="a9e0c-272">Requirement</span></span> | <span data-ttu-id="a9e0c-273">Значение</span><span class="sxs-lookup"><span data-stu-id="a9e0c-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e0c-274">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9e0c-274">Minimum supported client</span></span><br/> | <span data-ttu-id="a9e0c-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9e0c-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9e0c-276">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9e0c-276">Minimum supported server</span></span><br/> | <span data-ttu-id="a9e0c-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9e0c-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9e0c-278">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a9e0c-278">Namespace</span></span><br/>                | <span data-ttu-id="a9e0c-279">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a9e0c-279">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a9e0c-280">MOF</span><span class="sxs-lookup"><span data-stu-id="a9e0c-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9e0c-281"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9e0c-281"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9e0c-282">DLL</span><span class="sxs-lookup"><span data-stu-id="a9e0c-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9e0c-283"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9e0c-283"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9e0c-284">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9e0c-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9e0c-285">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-285">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="a9e0c-286">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="a9e0c-286">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="a9e0c-287">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="a9e0c-287">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="a9e0c-288">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="a9e0c-288">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

