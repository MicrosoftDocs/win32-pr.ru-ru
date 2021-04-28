---
description: Метод Create класса Win32_Service (поставщики WMI CIMWin32) — создает новую системную службу.
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Метод Create класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71bc0f4edb879fc4a51a012bc53db67031056f47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089693"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="c0ad7-103">Метод Create класса Win32_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c0ad7-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c0ad7-104">Метод **создания** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) создает новую системную службу.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="c0ad7-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="c0ad7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c0ad7-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c0ad7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ad7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0ad7-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c0ad7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0ad7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0ad7-109">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-110">Имя службы, устанавливаемой в метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="c0ad7-111">Максимальная длина строки — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="c0ad7-112">База данных диспетчера управления службами сохраняет регистр символов, но сравнения имен служб всегда не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="c0ad7-113">Прямые косые черты (/) и двойные обратные косые черты ( \\ ) являются недопустимыми символами имени службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-114">*DisplayName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-115">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-115">Display name of the service.</span></span> <span data-ttu-id="c0ad7-116">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="c0ad7-117">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="c0ad7-118">В сравнениях *DisplayName* всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="c0ad7-119">Ограничения: принимает то же значение, что и параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="c0ad7-120">Пример: "Атдиск".</span><span class="sxs-lookup"><span data-stu-id="c0ad7-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-121">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-122">Полный путь к исполняемому файлу, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="c0ad7-123">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="c0ad7-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-124">*ServiceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-125">Тип служб, предоставляемых процессам, которые их вызывают.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="c0ad7-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c0ad7-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-127">Драйвер ядра</span><span class="sxs-lookup"><span data-stu-id="c0ad7-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-128">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="c0ad7-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-129">Драйвер файловой системы</span><span class="sxs-lookup"><span data-stu-id="c0ad7-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="c0ad7-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-131">Адаптер</span><span class="sxs-lookup"><span data-stu-id="c0ad7-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="c0ad7-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-133">Драйвер распознавателя</span><span class="sxs-lookup"><span data-stu-id="c0ad7-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="c0ad7-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-135">Собственный процесс</span><span class="sxs-lookup"><span data-stu-id="c0ad7-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="c0ad7-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-137">Общий процесс</span><span class="sxs-lookup"><span data-stu-id="c0ad7-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="c0ad7-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-139">Интерактивный процесс</span><span class="sxs-lookup"><span data-stu-id="c0ad7-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c0ad7-140">*ErrorControl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-141">Серьезность ошибки, если не удается запустить метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="c0ad7-142">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="c0ad7-143">Все ошибки регистрируются системой.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="c0ad7-144">0</span><span class="sxs-lookup"><span data-stu-id="c0ad7-144">0</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-145">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-146">1</span><span class="sxs-lookup"><span data-stu-id="c0ad7-146">1</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-147">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-148">2</span><span class="sxs-lookup"><span data-stu-id="c0ad7-148">2</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-149">Система перезапускается в последней известной рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-150">3</span><span class="sxs-lookup"><span data-stu-id="c0ad7-150">3</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-151">Система пытается начать с хорошей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c0ad7-152">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-153">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="c0ad7-154">Загрузка</span><span class="sxs-lookup"><span data-stu-id="c0ad7-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-155">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="c0ad7-156">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-157">Система</span><span class="sxs-lookup"><span data-stu-id="c0ad7-157">System</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-158">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="c0ad7-159">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-160">Автоматически</span><span class="sxs-lookup"><span data-stu-id="c0ad7-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-161">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-162">Вручную</span><span class="sxs-lookup"><span data-stu-id="c0ad7-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-163">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-164">Выключено</span><span class="sxs-lookup"><span data-stu-id="c0ad7-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-165">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c0ad7-166">*Десктопинтеракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-167">Если задано **значение true**, служба может создавать окна на рабочем столе или взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-168">*StartName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-169">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-169">Account name under which the service runs.</span></span> <span data-ttu-id="c0ad7-170">В зависимости от типа службы имя учетной записи может иметь \\ Формат имя_домена имя_пользователя или имя участника-пользователя (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="c0ad7-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="c0ad7-171">Процесс службы заносится в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="c0ad7-172">Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="c0ad7-173">Если указано **значение NULL** , служба входит в систему как учетную запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="c0ad7-174">Для драйверов ядра или системного уровня *StartName* содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="c0ad7-175">Если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="c0ad7-176">Пример: ДВДОМ \\ Admin.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-177">*Стартпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-178">Пароль к имени учетной записи, заданному параметром *StartName* .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="c0ad7-179">Если пароль не изменяется, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="c0ad7-180">Если служба не имеет пароля, указывается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-181">*Лоадордерграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-182">Имя группы, связанное с новой службой.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-182">Group name associated with the new service.</span></span> <span data-ttu-id="c0ad7-183">Группы порядка загрузки содержатся в реестре и определяют последовательность, в которой службы загружаются в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="c0ad7-184">Если указатель равен **null** или указывает на пустую строку, служба не принадлежит группе.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="c0ad7-185">Зависимости между группами должны быть перечислены в параметре *лоадордерграупдепенденЦиес* .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="c0ad7-186">Сначала запускаются службы в списке группы упорядочения нагрузки, а затем — службы в группах, которые не входят в список групп порядка загрузки, за которыми следуют службы, не входящие в группу.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="c0ad7-187">В реестре имеется список групп упорядочения нагрузки, расположенных по адресу:</span><span class="sxs-lookup"><span data-stu-id="c0ad7-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="c0ad7-188">**HKey \_ \_** \\  \\  \\  \\ **ServiceGroupOrder** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="c0ad7-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-189">*ЛоадордерграупдепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-190">Массив групп упорядочивания нагрузки, которые должны быть запущены перед этой службой.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="c0ad7-191">Каждый элемент массива отделяется **значением NULL** , а список завершается двумя значениями **null** .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="c0ad7-192">В Visual Basic или скрипте можно передать массив vbArray.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="c0ad7-193">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="c0ad7-194">Имена групп должны иметь префикс в виде **\_ \_ идентификатора группы SC** (определенного в файле винсвк. h), чтобы отличать его от имени службы, так как службы и группы служб используют одно и то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="c0ad7-195">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-196">*СервицедепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0ad7-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-197">Массив, содержащий имена служб, которые должны запускаться перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="c0ad7-198">Каждый элемент массива отделяется **значением NULL** , а список завершается двумя значениями **null** .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="c0ad7-199">В Visual Basic или скрипте можно передать массив vbArray.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="c0ad7-200">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="c0ad7-201">Зависимость от службы означает, что эта служба может выполняться, только если запущена служба, от которой она зависит.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0ad7-202">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0ad7-202">Return value</span></span>

<span data-ttu-id="c0ad7-203">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="c0ad7-204">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c0ad7-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c0ad7-205">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c0ad7-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c0ad7-206">**0**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-207">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-208">**1**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-209">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-210">**2**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-211">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-212">**3**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-213">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-214">**4**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-215">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-216">**5**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-217">Запрошенный управляющий код не может быть отправлен в службу, так как состояние службы (свойство **State** класса [**Win32 \_ басесервице**](win32-baseservice.md) ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-218">**6**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-219">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-220">**7**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-221">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-222">**8**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-223">Неизвестный сбой при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-224">**9**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-225">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-226">**10**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-227">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-228">**11**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-229">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-230">**12**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-231">Зависимость, от которой зависит эта служба, удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-232">**13**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-233">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-234">**14**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-235">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-236">**15**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-237">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-238">**16**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-239">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-240">**17**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-241">Служба не имеет потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-242">**стр**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-243">Служба имеет циклические зависимости при запуске.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-244">**стр**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-245">Служба выполняется с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-246">**20**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-247">Имя службы содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-248">**открыт**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-249">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-250">**22**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-251">Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-252">**23**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-253">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0ad7-254">**24**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c0ad7-255">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0ad7-256">Remarks</span><span class="sxs-lookup"><span data-stu-id="c0ad7-256">Remarks</span></span>

<span data-ttu-id="c0ad7-257">Службы обычно устанавливаются одним из двух способов: либо как часть установки операционной системы, либо с помощью программы установки, предоставляемой разработчиком службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="c0ad7-258">Однако некоторые службы, в частности созданные в Организации, могут не иметь программы установки.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="c0ad7-259">В этих случаях для программной установки служб можно использовать метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="c0ad7-260">Несмотря на имя, метод Create на самом деле не создает службу; Он просто устанавливает существующую службу.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="c0ad7-261">Чтобы использовать эту команду, необходимо скопировать исполняемый файл службы на компьютер, а затем воспользоваться командой **создать** для установки службы.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="c0ad7-262">Метод **CREATE** аналогичен методу [**Change**](change-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="c0ad7-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="c0ad7-263">В обоих случаях свойства службы передаются в качестве параметров в метод.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="c0ad7-264">Как и в случае с параметрами, используемыми в методе **Change** , порядок, в котором передаются эти параметры, очень важен.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="c0ad7-265">Параметр *лоадордерграуп* представляет группирование системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="c0ad7-266">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="c0ad7-267">Для правильной работы этих зависимых служб требуется наличие предшествующих служб.</span><span class="sxs-lookup"><span data-stu-id="c0ad7-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="c0ad7-268">Примеры</span><span class="sxs-lookup"><span data-stu-id="c0ad7-268">Examples</span></span>

<span data-ttu-id="c0ad7-269">Следующий сценарий VBScript устанавливает службу с именем Дбсервице</span><span class="sxs-lookup"><span data-stu-id="c0ad7-269">The following VBScript installs a service named DbService</span></span>


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a><span data-ttu-id="c0ad7-270">Требования</span><span class="sxs-lookup"><span data-stu-id="c0ad7-270">Requirements</span></span>



| <span data-ttu-id="c0ad7-271">Требование</span><span class="sxs-lookup"><span data-stu-id="c0ad7-271">Requirement</span></span> | <span data-ttu-id="c0ad7-272">Значение</span><span class="sxs-lookup"><span data-stu-id="c0ad7-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ad7-273">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0ad7-273">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ad7-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0ad7-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0ad7-275">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0ad7-275">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ad7-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0ad7-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0ad7-277">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0ad7-277">Namespace</span></span><br/>                | <span data-ttu-id="c0ad7-278">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c0ad7-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0ad7-279">MOF</span><span class="sxs-lookup"><span data-stu-id="c0ad7-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0ad7-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0ad7-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0ad7-281">DLL</span><span class="sxs-lookup"><span data-stu-id="c0ad7-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0ad7-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ad7-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ad7-283">См. также</span><span class="sxs-lookup"><span data-stu-id="c0ad7-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0ad7-284">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0ad7-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c0ad7-285">**\_Служба Win32**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="c0ad7-286">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="c0ad7-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

