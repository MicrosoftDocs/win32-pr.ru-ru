---
description: Создает новую службу, управляемую драйвером системы.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Метод Create класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142922"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="46727-103">Метод Create \_ класса Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="46727-103">Create method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="46727-104">Метод **создания** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) создает новую службу, управляемую драйвером системы.</span><span class="sxs-lookup"><span data-stu-id="46727-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service managed by the system driver.</span></span> <span data-ttu-id="46727-105">Параметр *Win32 \_ лоадордерграуп* представляет группу системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="46727-105">The *Win32\_LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="46727-106">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="46727-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="46727-107">Для правильной работы этих зависимых служб требуется наличие предшествующих служб.</span><span class="sxs-lookup"><span data-stu-id="46727-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="46727-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="46727-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="46727-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="46727-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="46727-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46727-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="46727-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="46727-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46727-112">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-113">Имя службы, устанавливаемой в метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="46727-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="46727-114">Максимальная длина строки — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="46727-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="46727-115">База данных диспетчера управления службами сохраняет регистр символов, но сравнения имен служб всегда не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="46727-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="46727-116">Прямые косые черты (/) и двойные обратные косые черты ( \\ ) являются недопустимыми символами имени службы.</span><span class="sxs-lookup"><span data-stu-id="46727-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="46727-117">*DisplayName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-118">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="46727-118">Display name of the service.</span></span> <span data-ttu-id="46727-119">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="46727-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="46727-120">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="46727-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="46727-121">В сравнениях *DisplayName* всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="46727-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="46727-122">Ограничения: принимает то же значение, что и параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="46727-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="46727-123">Пример: "Атдиск".</span><span class="sxs-lookup"><span data-stu-id="46727-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="46727-124">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-125">Полный путь к исполняемому файлу, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="46727-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="46727-126">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="46727-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="46727-127">*ServiceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-128">Тип служб, предоставляемых процессам, которые их вызывают.</span><span class="sxs-lookup"><span data-stu-id="46727-128">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="46727-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46727-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="46727-130">Драйвер ядра</span><span class="sxs-lookup"><span data-stu-id="46727-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="46727-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="46727-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="46727-132">Драйвер файловой системы</span><span class="sxs-lookup"><span data-stu-id="46727-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="46727-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="46727-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="46727-134">Адаптер</span><span class="sxs-lookup"><span data-stu-id="46727-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="46727-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="46727-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="46727-136">Драйвер распознавателя</span><span class="sxs-lookup"><span data-stu-id="46727-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="46727-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="46727-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="46727-138">Собственный процесс</span><span class="sxs-lookup"><span data-stu-id="46727-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="46727-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="46727-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="46727-140">Общий процесс</span><span class="sxs-lookup"><span data-stu-id="46727-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="46727-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="46727-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="46727-142">Интерактивный процесс</span><span class="sxs-lookup"><span data-stu-id="46727-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="46727-143">*ErrorControl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-144">Серьезность ошибки, если не удается запустить метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="46727-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="46727-145">Это значение указывает на действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="46727-145">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="46727-146">Все ошибки регистрируются системой.</span><span class="sxs-lookup"><span data-stu-id="46727-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="46727-147">0</span><span class="sxs-lookup"><span data-stu-id="46727-147">0</span></span>
</dt> <dd>

<span data-ttu-id="46727-148">Обращать</span><span class="sxs-lookup"><span data-stu-id="46727-148">"Ignore"</span></span>

<span data-ttu-id="46727-149">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="46727-149">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="46727-150">1</span><span class="sxs-lookup"><span data-stu-id="46727-150">1</span></span>
</dt> <dd>

<span data-ttu-id="46727-151">"Normal"</span><span class="sxs-lookup"><span data-stu-id="46727-151">"Normal"</span></span>

<span data-ttu-id="46727-152">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="46727-152">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="46727-153">2</span><span class="sxs-lookup"><span data-stu-id="46727-153">2</span></span>
</dt> <dd>

<span data-ttu-id="46727-154">Серьезные</span><span class="sxs-lookup"><span data-stu-id="46727-154">"Severe"</span></span>

<span data-ttu-id="46727-155">Система перезапускается в последней известной рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="46727-155">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="46727-156">3</span><span class="sxs-lookup"><span data-stu-id="46727-156">3</span></span>
</dt> <dd>

<span data-ttu-id="46727-157">Критическое</span><span class="sxs-lookup"><span data-stu-id="46727-157">"Critical"</span></span>

<span data-ttu-id="46727-158">Система пытается начать с хорошей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="46727-158">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="46727-159">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-159">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-160">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="46727-160">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="46727-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Файле**</span><span class="sxs-lookup"><span data-stu-id="46727-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="46727-162">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="46727-162">Device driver started by the operating system loader.</span></span> <span data-ttu-id="46727-163">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="46727-163">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="46727-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Системой**</span><span class="sxs-lookup"><span data-stu-id="46727-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="46727-165">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="46727-165">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="46727-166">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="46727-166">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="46727-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Автоматически**</span><span class="sxs-lookup"><span data-stu-id="46727-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="46727-168">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="46727-168">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="46727-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную**</span><span class="sxs-lookup"><span data-stu-id="46727-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="46727-170">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="46727-170">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="46727-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Доступ**</span><span class="sxs-lookup"><span data-stu-id="46727-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="46727-172">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="46727-172">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="46727-173">*Десктопинтеракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-173">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-174">Если **значение — true**, служба может создавать окна на рабочем столе или взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="46727-174">If **true**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="46727-175">*StartName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-175">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-176">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="46727-176">Account name under which the service runs.</span></span> <span data-ttu-id="46727-177">В зависимости от типа службы имя учетной записи может иметь \\ Формат имя_домена имя_пользователя или имя участника-пользователя (UPN) ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="46727-177">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="46727-178">Процесс службы заносится в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="46727-178">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="46727-179">Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="46727-179">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="46727-180">Если указано **значение NULL** , служба входит в систему как учетную запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="46727-180">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="46727-181">Для драйверов ядра или системного уровня *StartName* содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="46727-181">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="46727-182">Если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.</span><span class="sxs-lookup"><span data-stu-id="46727-182">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="46727-183">Пример: ДВДОМ \\ Admin</span><span class="sxs-lookup"><span data-stu-id="46727-183">Example: DWDOM\\Admin</span></span>

</dd> <dt>

<span data-ttu-id="46727-184">*Стартпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-184">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-185">Пароль к имени учетной записи, заданному параметром *StartName* .</span><span class="sxs-lookup"><span data-stu-id="46727-185">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="46727-186">Если пароль не изменяется, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="46727-186">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="46727-187">Если служба не имеет пароля, указывается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="46727-187">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="46727-188">*Лоадордерграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-188">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-189">Имя группы, связанное с новой службой.</span><span class="sxs-lookup"><span data-stu-id="46727-189">Group name associated with the new service.</span></span> <span data-ttu-id="46727-190">Группы порядка загрузки содержатся в реестре и определяют последовательность, в которой службы загружаются в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="46727-190">Load order groups are contained in the registry and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="46727-191">Если указатель равен **null** или указывает на пустую строку, служба не принадлежит группе.</span><span class="sxs-lookup"><span data-stu-id="46727-191">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="46727-192">Зависимости между группами должны быть перечислены в параметре *лоадордерграупдепенденЦиес* .</span><span class="sxs-lookup"><span data-stu-id="46727-192">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="46727-193">Сначала запускаются службы в списке группы упорядочения нагрузки, а затем — службы в группах, которые не входят в список групп порядка загрузки, за которыми следуют службы, не входящие в группу.</span><span class="sxs-lookup"><span data-stu-id="46727-193">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="46727-194">В реестре имеется список групп упорядочения нагрузки, расположенных по адресу:</span><span class="sxs-lookup"><span data-stu-id="46727-194">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="46727-195">**HKey \_ \_** \\  \\  \\  \\ **ServiceGroupOrder** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="46727-195">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="46727-196">*ЛоадордерграупдепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-196">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-197">Массив групп упорядочивания нагрузки, которые должны быть запущены перед этой службой.</span><span class="sxs-lookup"><span data-stu-id="46727-197">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="46727-198">Каждый элемент массива отделяется **значением NULL** , а список завершается двумя значениями **null** .</span><span class="sxs-lookup"><span data-stu-id="46727-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="46727-199">В Visual Basic или скрипте можно передать массив vbArray.</span><span class="sxs-lookup"><span data-stu-id="46727-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="46727-200">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="46727-200">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="46727-201">Имена групп должны иметь префикс в виде **\_ \_ идентификатора группы SC** (определенного в файле винсвк. h), чтобы отличать его от имени службы, так как службы и группы служб используют одно и то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="46727-201">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="46727-202">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="46727-202">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="46727-203">*СервицедепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46727-203">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46727-204">Массив, содержащий имена служб, которые должны запускаться перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="46727-204">An array that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="46727-205">Каждый элемент массива отделяется **значением NULL** , а список завершается двумя значениями **null** .</span><span class="sxs-lookup"><span data-stu-id="46727-205">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="46727-206">В Visual Basic или скрипте можно передать массив vbArray.</span><span class="sxs-lookup"><span data-stu-id="46727-206">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="46727-207">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="46727-207">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="46727-208">Зависимость от службы означает, что эта служба может выполняться, только если запущена служба, от которой она зависит.</span><span class="sxs-lookup"><span data-stu-id="46727-208">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46727-209">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46727-209">Return value</span></span>

<span data-ttu-id="46727-210">Возвращает значение 0 (нуль), если служба была успешно создана, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="46727-210">Returns a value of 0 (zero) if the service was successfully created, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="46727-211">Требования</span><span class="sxs-lookup"><span data-stu-id="46727-211">Requirements</span></span>



| <span data-ttu-id="46727-212">Требование</span><span class="sxs-lookup"><span data-stu-id="46727-212">Requirement</span></span> | <span data-ttu-id="46727-213">Значение</span><span class="sxs-lookup"><span data-stu-id="46727-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46727-214">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46727-214">Minimum supported client</span></span><br/> | <span data-ttu-id="46727-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46727-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46727-216">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46727-216">Minimum supported server</span></span><br/> | <span data-ttu-id="46727-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46727-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46727-218">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="46727-218">Namespace</span></span><br/>                | <span data-ttu-id="46727-219">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46727-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46727-220">MOF</span><span class="sxs-lookup"><span data-stu-id="46727-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46727-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46727-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46727-222">DLL</span><span class="sxs-lookup"><span data-stu-id="46727-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46727-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46727-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46727-224">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46727-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="46727-225">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46727-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="46727-226">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="46727-226">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

