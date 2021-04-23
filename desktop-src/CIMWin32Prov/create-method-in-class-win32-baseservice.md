---
description: Создает новую службу.
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Метод Create класса Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8115ed3d9795720796b5f944c11a519ff366983
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141419"
---
# <a name="create-method-of-the-win32_baseservice-class"></a><span data-ttu-id="d6ec2-103">Метод Create \_ класса Win32 басесервице</span><span class="sxs-lookup"><span data-stu-id="d6ec2-103">Create method of the Win32\_BaseService class</span></span>

<span data-ttu-id="d6ec2-104">Метод **создания** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) создает новую службу.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service.</span></span> <span data-ttu-id="d6ec2-105">Параметр *лоадордерграуп* представляет группирование системных служб, определяющих зависимости выполнения.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-105">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="d6ec2-106">Службы должны запускаться в порядке, указанном в группе порядок загрузки, так как службы зависят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="d6ec2-107">Для правильной работы этих зависимых служб требуется наличие предшествующих служб.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="d6ec2-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d6ec2-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d6ec2-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d6ec2-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ec2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6ec2-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d6ec2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6ec2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6ec2-112">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-113">Имя службы, устанавливаемой в метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="d6ec2-114">Максимальная длина строки — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="d6ec2-115">База данных диспетчера управления службами сохраняет регистр символов, но сравнения имен служб всегда не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-115">The service control manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="d6ec2-116">Прямые косые черты (/) и двойные обратные косые черты ( \\ ) являются недопустимыми символами имени службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-117">*DisplayName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-118">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-118">Display name of the service.</span></span> <span data-ttu-id="d6ec2-119">Максимальная длина этой строки равна 256 символам.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="d6ec2-120">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-120">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="d6ec2-121">В сравнениях *DisplayName* всегда учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="d6ec2-122">Ограничения: принимает то же значение, что и параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="d6ec2-123">Пример: "Атдиск".</span><span class="sxs-lookup"><span data-stu-id="d6ec2-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-124">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-125">Полный путь к исполняемому файлу, реализующему службу.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="d6ec2-126">Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="d6ec2-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-127">*ServiceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-128">Тип служб, предоставляемых процессам, которые их вызывают.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-128">Type of services provided to processes that call them.</span></span> <span data-ttu-id="d6ec2-129">Значение является точечным рисунком.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-129">The value is a bitmap.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="d6ec2-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Драйвер ядра** (1)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="d6ec2-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Драйвер файловой системы** (2)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="d6ec2-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Адаптер** (4)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="d6ec2-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Драйвер распознавателя** (8)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="d6ec2-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Собственный процесс** (16)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="d6ec2-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Общий процесс** (32)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="d6ec2-136">256</span><span class="sxs-lookup"><span data-stu-id="d6ec2-136">256</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-137">Интерактивный процесс</span><span class="sxs-lookup"><span data-stu-id="d6ec2-137">Interactive Process</span></span>

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d6ec2-138">*ErrorControl* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-139">Серьезность ошибки, если не удается запустить метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-139">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="d6ec2-140">Значение указывает действие, предпринимаемое программой запуска, если происходит сбой.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="d6ec2-141">Все ошибки регистрируются системой.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="d6ec2-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** (0)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-143">Пользователь не получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="d6ec2-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (1)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-145">Пользователь получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-145">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="d6ec2-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** (2)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-147">Система перезапускается в последней известной рабочей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-147">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d6ec2-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-149">Система пытается начать с хорошей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-149">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d6ec2-150">*StartMode* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-150">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-151">Режим запуска базовой службы Windows.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-151">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="d6ec2-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки** ("Boot")</span><span class="sxs-lookup"><span data-stu-id="d6ec2-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-153">Драйвер устройства запущен загрузчиком операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-153">Device driver started by the operating system loader.</span></span> <span data-ttu-id="d6ec2-154">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-154">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="d6ec2-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Системный запуск** ("System")</span><span class="sxs-lookup"><span data-stu-id="d6ec2-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-156">Драйвер устройства запущен процессом инициализации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-156">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="d6ec2-157">Это значение допустимо только для служб драйверов.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-157">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="d6ec2-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Автоматический запуск** (автоматический)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-159">Служба запускается автоматически диспетчером управления службами во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-159">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="d6ec2-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Запуск по требованию** (вручную)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-161">Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-161">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d6ec2-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="d6ec2-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="d6ec2-163">Служба, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-163">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d6ec2-164">*Десктопинтеракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-164">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-165">Если задано **значение true**, служба может создавать окна на рабочем столе или взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-165">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-166">*StartName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-166">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-167">Имя учетной записи, под которой выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-167">Account name under which the service runs.</span></span> <span data-ttu-id="d6ec2-168">В зависимости от типа службы имя учетной записи может иметь форму "имя_домена \\ имя пользователя".</span><span class="sxs-lookup"><span data-stu-id="d6ec2-168">Depending on the service type, the account name may be in the form of "DomainName\\Username".</span></span> <span data-ttu-id="d6ec2-169">Процесс службы заносится в журнал с использованием одной из этих двух форм при запуске.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-169">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="d6ec2-170">Если учетная запись принадлежит к встроенному домену, ". \\ Можно указать имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-170">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="d6ec2-171">Если указано **значение NULL** , служба входит в систему как учетную запись LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-171">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="d6ec2-172">Для драйверов ядра или системного уровня *StartName* содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-172">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="d6ec2-173">Если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-173">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="d6ec2-174">Пример: ДВДОМ \\ Admin.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-174">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-175">*Стартпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-175">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-176">Пароль к имени учетной записи, заданному параметром *StartName* .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-176">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="d6ec2-177">Если пароль не изменяется, укажите **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-177">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="d6ec2-178">Если служба не имеет пароля, указывается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-178">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-179">*Лоадордерграуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-179">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-180">Имя группы, связанное с новой службой.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-180">Group name associated with the new service.</span></span> <span data-ttu-id="d6ec2-181">Группы порядка загрузки содержатся в реестре и определяют последовательность, в которой службы загружаются в операционную систему.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-181">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="d6ec2-182">Если указатель равен **null** или указывает на пустую строку, служба не принадлежит группе.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-182">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="d6ec2-183">Зависимости между группами должны быть перечислены в параметре *лоадордерграупдепенденЦиес* .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="d6ec2-184">Сначала запускаются службы в списке группы упорядочения нагрузки, а затем — службы в группах, которые не входят в список групп порядка загрузки, за которыми следуют службы, не входящие в группу.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="d6ec2-185">В реестре имеется список групп упорядочения нагрузки, расположенных по адресу:</span><span class="sxs-lookup"><span data-stu-id="d6ec2-185">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="d6ec2-186">**HKey \_ \_** \\  \\  \\  \\ **ServiceGroupOrder** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="d6ec2-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-187">*ЛоадордерграупдепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-188">Массив групп упорядочивания нагрузки, которые должны быть запущены перед этой службой.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-188">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="d6ec2-189">Каждый элемент массива отделяется **значением NULL** , а список завершается двумя значениями **null** .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-189">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d6ec2-190">В Visual Basic или скрипте можно передать массив vbArray.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-190">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d6ec2-191">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-191">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d6ec2-192">Имена групп должны иметь префикс в виде \_ идентификатора группы SC \_ (определенного в файле винсвк. h), чтобы отличать его от имени службы, так как службы и группы служб используют одно и то же пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-192">Group names must be prefixed by the SC\_GROUP\_IDENTIFIER (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="d6ec2-193">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-193">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-194">*СервицедепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6ec2-194">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-195">Массив, содержащий имена служб, которые должны запускаться перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-195">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="d6ec2-196">Каждый элемент массива отделяется **значением NULL** , а список завершается двумя значениями **null** .</span><span class="sxs-lookup"><span data-stu-id="d6ec2-196">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="d6ec2-197">В Visual Basic или скрипте можно передать массив vbArray.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-197">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="d6ec2-198">Если указатель имеет **значение NULL** или указывает на пустую строку, служба не имеет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-198">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="d6ec2-199">Зависимость от службы означает, что эта служба может выполняться, только если запущена служба, от которой она зависит.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-199">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6ec2-200">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6ec2-200">Return value</span></span>

<span data-ttu-id="d6ec2-201">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-201">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d6ec2-202">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-203">0</span><span class="sxs-lookup"><span data-stu-id="d6ec2-203">0</span></span>

<span data-ttu-id="d6ec2-204">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-205">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-206">1</span><span class="sxs-lookup"><span data-stu-id="d6ec2-206">1</span></span>

<span data-ttu-id="d6ec2-207">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-208">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-209">2</span><span class="sxs-lookup"><span data-stu-id="d6ec2-209">2</span></span>

<span data-ttu-id="d6ec2-210">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-211">**Работающие зависимые службы**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-212">3</span><span class="sxs-lookup"><span data-stu-id="d6ec2-212">3</span></span>

<span data-ttu-id="d6ec2-213">Службу нельзя остановить, так как от нее зависят другие работающие службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-214">**Недопустимый элемент управления службой**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-215">4</span><span class="sxs-lookup"><span data-stu-id="d6ec2-215">4</span></span>

<span data-ttu-id="d6ec2-216">Запрошенный управляющий код недопустим или неприемлем для данной службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-217">**Служба не может принять контроль**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-218">5</span><span class="sxs-lookup"><span data-stu-id="d6ec2-218">5</span></span>

<span data-ttu-id="d6ec2-219">Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-220">**Служба неактивна**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-221">6</span><span class="sxs-lookup"><span data-stu-id="d6ec2-221">6</span></span>

<span data-ttu-id="d6ec2-222">Служба не запущена.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-223">**Время ожидания запроса на обслуживание**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-224">7</span><span class="sxs-lookup"><span data-stu-id="d6ec2-224">7</span></span>

<span data-ttu-id="d6ec2-225">Служба не ответила на запрос запуска за отведенное время.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-226">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-227">8</span><span class="sxs-lookup"><span data-stu-id="d6ec2-227">8</span></span>

<span data-ttu-id="d6ec2-228">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-228">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-229">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-230">9</span><span class="sxs-lookup"><span data-stu-id="d6ec2-230">9</span></span>

<span data-ttu-id="d6ec2-231">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-232">**Служба уже запущена**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-233">10</span><span class="sxs-lookup"><span data-stu-id="d6ec2-233">10</span></span>

<span data-ttu-id="d6ec2-234">Служба уже запущена.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-235">**База данных службы заблокирована**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-236">11</span><span class="sxs-lookup"><span data-stu-id="d6ec2-236">11</span></span>

<span data-ttu-id="d6ec2-237">База данных для добавления новой службы заблокирована.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-238">**Зависимость службы удалена**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-239">12</span><span class="sxs-lookup"><span data-stu-id="d6ec2-239">12</span></span>

<span data-ttu-id="d6ec2-240">Служба, от которой зависит эта служба, была удалена из системы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-240">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-241">**Сбой зависимости службы**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-242">13</span><span class="sxs-lookup"><span data-stu-id="d6ec2-242">13</span></span>

<span data-ttu-id="d6ec2-243">Этой службе не удалось найти службу, которая необходима зависимой службе.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-244">**Служба отключена**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-245">14</span><span class="sxs-lookup"><span data-stu-id="d6ec2-245">14</span></span>

<span data-ttu-id="d6ec2-246">Эта служба была отключена в системе.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-247">**Сбой при входе в службу**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-248">15</span><span class="sxs-lookup"><span data-stu-id="d6ec2-248">15</span></span>

<span data-ttu-id="d6ec2-249">Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-250">**Служба помечена для удаления**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-251">16</span><span class="sxs-lookup"><span data-stu-id="d6ec2-251">16</span></span>

<span data-ttu-id="d6ec2-252">Эта служба удаляется из системы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-253">**Служба без потока**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-254">17</span><span class="sxs-lookup"><span data-stu-id="d6ec2-254">17</span></span>

<span data-ttu-id="d6ec2-255">Отсутствует поток исполнения для этой службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-255">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-256">**Состояние "циклическая зависимость"**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-257">18</span><span class="sxs-lookup"><span data-stu-id="d6ec2-257">18</span></span>

<span data-ttu-id="d6ec2-258">При запуске службы обнаружены циклические зависимости.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-258">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-259">**Состояние "повторяющееся имя"**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-260">19</span><span class="sxs-lookup"><span data-stu-id="d6ec2-260">19</span></span>

<span data-ttu-id="d6ec2-261">Служба с таким именем уже запущена.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-261">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-262">**Состояние "Недопустимое имя"**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-263">20</span><span class="sxs-lookup"><span data-stu-id="d6ec2-263">20</span></span>

<span data-ttu-id="d6ec2-264">В имени службы присутствуют недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-264">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-265">**Недопустимый параметр Status**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-266">21</span><span class="sxs-lookup"><span data-stu-id="d6ec2-266">21</span></span>

<span data-ttu-id="d6ec2-267">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-268">**Недопустимое состояние учетной записи службы**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-269">22</span><span class="sxs-lookup"><span data-stu-id="d6ec2-269">22</span></span>

<span data-ttu-id="d6ec2-270">Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-270">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-271">**Служба состояний существует**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-272">23</span><span class="sxs-lookup"><span data-stu-id="d6ec2-272">23</span></span>

<span data-ttu-id="d6ec2-273">Служба существует в базе данных доступных в системе служб.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-274">**Служба уже приостановлена**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-275">24</span><span class="sxs-lookup"><span data-stu-id="d6ec2-275">24</span></span>

<span data-ttu-id="d6ec2-276">Служба в данный момент приостановлена в системе.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="d6ec2-277">**Другое**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d6ec2-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="d6ec2-278">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6ec2-279">Требования</span><span class="sxs-lookup"><span data-stu-id="d6ec2-279">Requirements</span></span>



| <span data-ttu-id="d6ec2-280">Требование</span><span class="sxs-lookup"><span data-stu-id="d6ec2-280">Requirement</span></span> | <span data-ttu-id="d6ec2-281">Значение</span><span class="sxs-lookup"><span data-stu-id="d6ec2-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ec2-282">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6ec2-282">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ec2-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6ec2-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6ec2-284">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6ec2-284">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ec2-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6ec2-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6ec2-286">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d6ec2-286">Namespace</span></span><br/>                | <span data-ttu-id="d6ec2-287">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d6ec2-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6ec2-288">MOF</span><span class="sxs-lookup"><span data-stu-id="d6ec2-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6ec2-289"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6ec2-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6ec2-290">DLL</span><span class="sxs-lookup"><span data-stu-id="d6ec2-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6ec2-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6ec2-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6ec2-292">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6ec2-292">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6ec2-293">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6ec2-293">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d6ec2-294">**\_Басесервице Win32**</span><span class="sxs-lookup"><span data-stu-id="d6ec2-294">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

