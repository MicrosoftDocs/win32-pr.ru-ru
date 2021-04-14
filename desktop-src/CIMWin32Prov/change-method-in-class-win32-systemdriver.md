---
description: Изменяет \_ службу Win32 SystemDriver.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Метод Change класса Win32_SystemDriver (Мбнапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496425"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="5904f-103">Метод Change \_ класса Win32 SystemDriver</span><span class="sxs-lookup"><span data-stu-id="5904f-103">Change method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="5904f-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) Change изменяет службу [**Win32 \_ SystemDriver**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="5904f-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span> <span data-ttu-id="5904f-105">Параметр [**Win32 \_ лоадордерграуп**](win32-loadordergroup.md) представляет группу системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="5904f-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="5904f-106">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="5904f-106">The services must be initiated in the order specified by the Load Order Group as the services are dependent on each other.</span></span> <span data-ttu-id="5904f-107">Для правильной работы этих зависимых служб требуется наличие предшествующих служб.</span><span class="sxs-lookup"><span data-stu-id="5904f-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="5904f-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="5904f-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5904f-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5904f-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5904f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5904f-110">Syntax</span></span>


```mof
uint32 Change(
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



## <a name="parameters"></a><span data-ttu-id="5904f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5904f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5904f-112">*DisplayName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-113">Отображаемое имя для службы.</span><span class="sxs-lookup"><span data-stu-id="5904f-113">The display name of the service.</span></span> <span data-ttu-id="5904f-114">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="5904f-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="5904f-115">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="5904f-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="5904f-116">В сравнениях *DisplayName* всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="5904f-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="5904f-117">Ограничения: принимает то же значение, что и параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="5904f-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="5904f-118">Пример: "Атдиск"</span><span class="sxs-lookup"><span data-stu-id="5904f-118">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="5904f-119">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-120">Полный путь к исполняемому файлу, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="5904f-120">The fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="5904f-121">Пример: *\\ СистемныйКорневойКаталог \\ System32 \\ Drivers \\afd.sys*</span><span class="sxs-lookup"><span data-stu-id="5904f-121">Example: *\\SystemRoot\\System32\\drivers\\afd.sys*</span></span>

</dd> <dt>

<span data-ttu-id="5904f-122">*ServiceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-123">Тип служб, предоставляемых процессам, которые их вызывают.</span><span class="sxs-lookup"><span data-stu-id="5904f-123">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="5904f-124">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5904f-124">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="5904f-125">Драйвер ядра</span><span class="sxs-lookup"><span data-stu-id="5904f-125">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="5904f-126">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="5904f-126">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="5904f-127">Драйвер файловой системы</span><span class="sxs-lookup"><span data-stu-id="5904f-127">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="5904f-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="5904f-128">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="5904f-129">Адаптер</span><span class="sxs-lookup"><span data-stu-id="5904f-129">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="5904f-130">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="5904f-130">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="5904f-131">Драйвер распознавателя</span><span class="sxs-lookup"><span data-stu-id="5904f-131">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="5904f-132">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="5904f-132">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="5904f-133">Собственный процесс</span><span class="sxs-lookup"><span data-stu-id="5904f-133">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="5904f-134">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="5904f-134">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="5904f-135">Общий процесс</span><span class="sxs-lookup"><span data-stu-id="5904f-135">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="5904f-136">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="5904f-136">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="5904f-137">Интерактивный процесс</span><span class="sxs-lookup"><span data-stu-id="5904f-137">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5904f-138">*ErrorControl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-139">Серьезность ошибки, если не удается запустить службу во время запуска.</span><span class="sxs-lookup"><span data-stu-id="5904f-139">The severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="5904f-140">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="5904f-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="5904f-141">Все ошибки регистрируются системой.</span><span class="sxs-lookup"><span data-stu-id="5904f-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="5904f-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** (0)</span><span class="sxs-lookup"><span data-stu-id="5904f-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5904f-143">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="5904f-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="5904f-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (1)</span><span class="sxs-lookup"><span data-stu-id="5904f-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5904f-145">Нормальный.</span><span class="sxs-lookup"><span data-stu-id="5904f-145">Normal.</span></span> <span data-ttu-id="5904f-146">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="5904f-146">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="5904f-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** (2)</span><span class="sxs-lookup"><span data-stu-id="5904f-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5904f-148">Система перезапускается с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="5904f-148">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="5904f-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="5904f-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5904f-150">Попытка перезапустить систему в рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5904f-150">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5904f-151">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-151">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-152">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="5904f-152">The start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="5904f-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки**</span><span class="sxs-lookup"><span data-stu-id="5904f-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="5904f-154">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5904f-154">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="5904f-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки**</span><span class="sxs-lookup"><span data-stu-id="5904f-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="5904f-156">Драйвер устройства, с которого запускается загрузчик операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5904f-156">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="5904f-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Системный запуск**</span><span class="sxs-lookup"><span data-stu-id="5904f-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start**</span></span>


</dt> <dd>

<span data-ttu-id="5904f-158">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5904f-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="5904f-159">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="5904f-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="5904f-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Автоматический запуск**</span><span class="sxs-lookup"><span data-stu-id="5904f-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start**</span></span>


</dt> <dd>

<span data-ttu-id="5904f-161">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="5904f-161">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="5904f-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Запуск по требованию**</span><span class="sxs-lookup"><span data-stu-id="5904f-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start**</span></span>


</dt> <dd>

<span data-ttu-id="5904f-163">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="5904f-163">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5904f-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Доступ**</span><span class="sxs-lookup"><span data-stu-id="5904f-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="5904f-165">Служба, которая не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="5904f-165">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5904f-166">*Десктопинтеракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-167">Значение, которое, если **значение true**, служба может создавать окна на рабочем столе или взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="5904f-167">A value that, if **True**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="5904f-168">*StartName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-169">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="5904f-169">The account name the service runs under.</span></span> <span data-ttu-id="5904f-170">В зависимости от типа службы имя учетной записи может быть в формате имя_домена \\ имя пользователя или. \\ Имен.</span><span class="sxs-lookup"><span data-stu-id="5904f-170">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="5904f-171">При запуске процесс службы заносится в журнал с использованием одной из этих двух форм.</span><span class="sxs-lookup"><span data-stu-id="5904f-171">When it runs, the service process is logged using one of these two forms.</span></span> <span data-ttu-id="5904f-172">Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="5904f-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="5904f-173">Если указана пустая строка, служба входит в систему как учетную запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="5904f-173">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="5904f-174">Для драйверов ядра или системного уровня *StartName* содержит имя объекта драйвера, например \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="5904f-174">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns), which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="5904f-175">Если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы, например \\ администратора двдом.</span><span class="sxs-lookup"><span data-stu-id="5904f-175">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="5904f-176">Можно также использовать формат имени участника-пользователя (UPN) для указания **StartName**, например *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="5904f-176">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="5904f-177">*Стартпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-178">Пароль к имени учетной записи, заданному параметром *StartName* .</span><span class="sxs-lookup"><span data-stu-id="5904f-178">The password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="5904f-179">Если пароль не изменяется, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="5904f-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="5904f-180">Если служба не имеет пароля, указывается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="5904f-180">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="5904f-181">При изменении службы с локальной системы на сеть или из сети в локальную систему *стартпассворд* должен быть пустой строкой (""), а не **null**.</span><span class="sxs-lookup"><span data-stu-id="5904f-181">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="5904f-182">*Лоадордерграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-182">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-183">Имя группы, с которой она связана.</span><span class="sxs-lookup"><span data-stu-id="5904f-183">The group name that it is associated with.</span></span> <span data-ttu-id="5904f-184">Группы порядка загрузки содержатся в системном реестре и определяют последовательность, в которой службы загружаются в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="5904f-184">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="5904f-185">Если указатель равен **null** или указывает на пустую строку, служба не принадлежит группе.</span><span class="sxs-lookup"><span data-stu-id="5904f-185">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="5904f-186">Зависимости между группами должны быть перечислены в параметре *лоадордерграупдепенденЦиес* .</span><span class="sxs-lookup"><span data-stu-id="5904f-186">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="5904f-187">Сначала запускаются службы в списке группы упорядочения нагрузки, а затем — службы в группах, которые не входят в список групп порядка загрузки, за которыми следуют службы, не входящие в группу.</span><span class="sxs-lookup"><span data-stu-id="5904f-187">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="5904f-188">Системный реестр содержит список групп упорядочения нагрузки, расположенных по адресу:</span><span class="sxs-lookup"><span data-stu-id="5904f-188">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="5904f-189">**HKey \_ \_** \\  \\  \\  \\ **ServiceGroupOrder** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="5904f-189">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="5904f-190">*ЛоадордерграупдепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-190">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-191">Список групп упорядочивания нагрузки, которые должны быть запущены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="5904f-191">The list of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="5904f-192">Массив завершается двойным **нулем.**</span><span class="sxs-lookup"><span data-stu-id="5904f-192">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="5904f-193">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="5904f-193">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5904f-194">Имена групп должны иметь префикс в виде **\_ \_ идентификатора группы SC** (определенного в файле винсвк. h), чтобы отличать их от имен служб, так как службы и группы служб используют одно и то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="5904f-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the WinSvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="5904f-195">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="5904f-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="5904f-196">*СервицедепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5904f-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5904f-197">Список, содержащий имена служб, которые должны быть запущены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="5904f-197">The list that contains the names of the services that must start before this service starts.</span></span> <span data-ttu-id="5904f-198">Массив завершается двойным **нулем.**</span><span class="sxs-lookup"><span data-stu-id="5904f-198">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="5904f-199">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="5904f-199">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5904f-200">Зависимость от службы означает, что эта служба может выполняться, только если запущена служба, от которой она зависит.</span><span class="sxs-lookup"><span data-stu-id="5904f-200">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5904f-201">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5904f-201">Return value</span></span>

<span data-ttu-id="5904f-202">Возвращает нулевое значение (0), если служба была успешно изменена, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="5904f-202">Returns a value of zero (0) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5904f-203">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="5904f-203">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-204">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="5904f-204">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-205">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="5904f-205">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-206">**Запуск зависимых служб** (3)</span><span class="sxs-lookup"><span data-stu-id="5904f-206">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-207">**Недопустимый элемент управления службой** (4)</span><span class="sxs-lookup"><span data-stu-id="5904f-207">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-208">**Служба не может принять управление** (5)</span><span class="sxs-lookup"><span data-stu-id="5904f-208">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-209">**Служба неактивна** (6)</span><span class="sxs-lookup"><span data-stu-id="5904f-209">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-210">**Время ожидания запроса на обслуживание** (7)</span><span class="sxs-lookup"><span data-stu-id="5904f-210">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-211">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="5904f-211">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-212">**Путь не найден** (9)</span><span class="sxs-lookup"><span data-stu-id="5904f-212">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-213">**Служба уже запущена** (10)</span><span class="sxs-lookup"><span data-stu-id="5904f-213">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-214">**База данных службы заблокирована** (11)</span><span class="sxs-lookup"><span data-stu-id="5904f-214">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-215">**Удалена зависимость службы** (12)</span><span class="sxs-lookup"><span data-stu-id="5904f-215">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-216">**Сбой зависимости службы** (13)</span><span class="sxs-lookup"><span data-stu-id="5904f-216">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-217">**Служба отключена** (14)</span><span class="sxs-lookup"><span data-stu-id="5904f-217">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-218">**Сбой входа службы** (15)</span><span class="sxs-lookup"><span data-stu-id="5904f-218">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-219">**Служба помечена для удаления** (16)</span><span class="sxs-lookup"><span data-stu-id="5904f-219">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-220">**Служба без потока** (17)</span><span class="sxs-lookup"><span data-stu-id="5904f-220">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-221">**Состояние "циклическая зависимость** " (18)</span><span class="sxs-lookup"><span data-stu-id="5904f-221">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-222">**Состояние "повторяющееся имя** " (19)</span><span class="sxs-lookup"><span data-stu-id="5904f-222">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-223">**Состояние недопустимое имя** (20)</span><span class="sxs-lookup"><span data-stu-id="5904f-223">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-224">**Недопустимый параметр Status** (21)</span><span class="sxs-lookup"><span data-stu-id="5904f-224">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-225">**Недопустимое состояние учетной записи службы** (22)</span><span class="sxs-lookup"><span data-stu-id="5904f-225">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-226">**Служба состояния существует** (23)</span><span class="sxs-lookup"><span data-stu-id="5904f-226">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-227">**Служба уже приостановлена** (24)</span><span class="sxs-lookup"><span data-stu-id="5904f-227">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="5904f-228">**Другие** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="5904f-228">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5904f-229">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5904f-229">Remarks</span></span>

<span data-ttu-id="5904f-230">Чтобы изменить службу с сетевой службы на локальную систему, используйте следующие значения параметров *StartName* и *стартпассворд* :</span><span class="sxs-lookup"><span data-stu-id="5904f-230">To change a service from a network service to the local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="5904f-231">Чтобы изменить службу с локальной системной службы на сетевую службу, используйте следующие значения параметров *StartName* и *стартпассворд* :</span><span class="sxs-lookup"><span data-stu-id="5904f-231">To change a service from a local system service to network service, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="5904f-232">Требования</span><span class="sxs-lookup"><span data-stu-id="5904f-232">Requirements</span></span>



| <span data-ttu-id="5904f-233">Требование</span><span class="sxs-lookup"><span data-stu-id="5904f-233">Requirement</span></span> | <span data-ttu-id="5904f-234">Значение</span><span class="sxs-lookup"><span data-stu-id="5904f-234">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5904f-235">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5904f-235">Minimum supported client</span></span><br/> | <span data-ttu-id="5904f-236">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5904f-236">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5904f-237">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5904f-237">Minimum supported server</span></span><br/> | <span data-ttu-id="5904f-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5904f-238">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5904f-239">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5904f-239">Namespace</span></span><br/>                | <span data-ttu-id="5904f-240">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5904f-240">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5904f-241">Header</span><span class="sxs-lookup"><span data-stu-id="5904f-241">Header</span></span><br/>                   | <dl> <span data-ttu-id="5904f-242"><dt>Мбнапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5904f-242"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="5904f-243">MOF</span><span class="sxs-lookup"><span data-stu-id="5904f-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5904f-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5904f-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5904f-245">DLL</span><span class="sxs-lookup"><span data-stu-id="5904f-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5904f-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5904f-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5904f-247">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5904f-247">See also</span></span>

<dl> <dt>

<span data-ttu-id="5904f-248">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5904f-248">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5904f-249">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="5904f-249">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

